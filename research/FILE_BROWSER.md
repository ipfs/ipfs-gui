# Ipfs File Explorer

A nice graphical filesystem explorer for viewing the ipfs files api.
I'm personally a fan of the windows 10 explorer UI:
![explorer](https://mspoweruser.com/wp-content/uploads/2016/03/Windows-File-Explorer.jpg)
I would argue its the most successful file explorer UI, and much of what makes windows user friendly and pleasant to use.

Notably, grid OR row layout, the 'location' bar up top, an 'up' button to go up a directory in the hierarchy.
A 'quick bar' on the side might be nice, we may have some directories in the files api that are prefilled
with things in the future.

Use the [js-ipfs-api](https://github.com/ipfs/js-ipfs-api) to interact with the go-ipfs daemon.
The files api calls are all in [here](https://github.com/ipfs/js-ipfs-api/blob/master/src/api/files.js)
## Operations

### Adding a file
Either through dragging a file in or otherwise adding a file to the explorer,
first make a call to 'ipfs.add()', grab the hash that is returned, and then
call 'ipfs.files.cp' with the first argument being `/ipfs/$THAT_HASH` and the
second argument being the path within the filesystem of the explorer that the
new file will go (current directory/name_of_file_being_added).

It may be worth checking if the destination path exists before the operation
and if it does, either automatically rename the file something like
`original_file_name (1).ext` or pop up a notice to the user asking them to
select a name for the file.

```js
ipfs.add(stream, function (err, res) {
    if (err) { /* oh jeeze */ }
    api.files.cp([res[0].Hash, '/path/to/me'], (err) => {
        if (err) { /* do the javascripts */ }
    })
})
```

### Creating a directory
To create a directory, call `ipfs.files.mkdir(absolute_path)`

```js
ipfs.files.mkdir('/path/to/dir', (err) => {
    if (err) { /* oh jeeze */ }
})
```

### Listing a directory (for populating the view)
To get the items in a directory, call `ipfs.files.ls` with the `l` option set
to true.  In the output you'll get an array of directory entry objects with
names, types, and hashes.  The type field is current `0` for a file, and `1`
for a directory, more types may be added later for things like symlinks.

```js
ipfs.files.ls('/path/to/list', (err, res) => {
  if (err) { /* error */ }
  res.Entries.forEach((e) => {
    console.log(e)
  })
})
```

### Displaying information about an item
To get information such as the size and hash of an item, call `ipfs.files.stat`. 
The hash can be used to create a 'share' link to any given item: 'https://ipfs.io/ipfs/$HASH'

```js
ipfs.files.stat('/path/to/the/thing',  (err, res) => {
    if (err) { /* bad things */ }
    console.log(res)
})
```

### Downloading an item
To get the contents of a file, call `ipfs.files.read`.

```js
api.files.read('/the/path/to/the/thing', function (err, stream) {
    if (err) { }
    console.log("A stream: ", stream)
})
```

!! For now, let's *not* support downloading of directories. The js-ipfs api

!! currently doesnt provide good support for downloading an archive of a directory

!! via `ipfs.get`.

### Deleting an item
To remove a file, call `ipfs.files.rm`, for a directory, pass the `recursive=true` option.
Note that deleting an item from this view does not necessarily remove it from
the user's system. That only happens when `ipfs.repo.gc` gets run. It may be
worthwhile to have a UI element (like a trash bin on windows) that contains
deleted files, and you can 'clean it out' which runs a gc.


### Renaming an item
To rename (or otherwise move) an item, call `ipfs.files.mv` with the files current name, and its new name.
Note that renaming a file to have the same name as an already existing file
will delete the existing file (replacing it with the one being renamed).

```js
// Rename 'foo' to 'bar'
api.files.mv(['/foo', '/bar'], (err) => {
    if (err) { /* handle */ }
})
```

### Copying an item
To implement the traditional 'right click+Copy, right click+Paste', the copy
option should call `ipfs.files.stat` to get the items hash, and then paste
should run `ipfs.files.cp` as in the 'Adding a file' operation.

```js
// On Copy
api.files.stat('/path/to/the/thing', function (err, res) {
    if (err) { /* bad things */ }
    clipboardHash = res.Hash
})

// On Paste
api.files.cp('/ipfs/' + clipboardHash, (err) => {
    if (err) { }
})
```

## Playing with the files API
We have a short example tutorial for interacting with the files API on the command line [here](https://github.com/ipfs/examples/tree/master/examples/files).

You'll probably want to put a few files in there manually to make working on the UI a little
easier. That guide should cover it pretty well.
## Previous work
I wrote a very early version of this a long time ago: https://github.com/ipfs/file-browser
(I'm not expecting this to be reused at all)

And more recently, @dignifiedquire worked on a version of this in react/redux: https://github.com/ipfs/webui/tree/5ef3c3edaf59964ef324fe22eb28adeb039875d7/app/scripts/components/files
