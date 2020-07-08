# Functions

## Modules

### fs

Used to read/write from a file.

``` js
const fs = require('fs')

// Write text to a file
fs.writeFileSync('notes.txt', 'text to add to notes.txt.')

// Read text from a file
fs.readFileSync('notes.txt')

// Writes datato the file specified by filename, appending to its contents. Creates a new file if the filename does not exist. If an error occurs, error is passed to the callback function
fs.appendFile(filename, data, “utf8”, callback)

fs.appendFile(“file.txt”, “added contents”, “utf8”,
 (err) => { ... }
);

```

### path

Used to get the path to the current working directory of the app

``` js
const path = require('path')

// Path to where the script currently is
console.log(__dirname)
// output: /Users/raph/git/scriptFolder

// Combining to add/create a path
console.log(path.join(__dirname, '../this'))
// output /Users/raph/git/this

// Get the file name/folder from a full path (last value basically)
console.log(path.basename('/Users/raph/git/udemy/playground/this.txt'))
// output: this.txt
console.log(path.basename('/Users/raph/git/udemy/playground'))
//output: playground

// Get extension from a file name
console.log(path.extname('index.html'))
// output: .html

```

### bcrypt

Hashing a password

``` js
const bcrypt = require('bcryptjs')

const passhashingcheck = async () => {
    const password = 'thisisapassword!'
    const hashedPassword = await bcrypt.hash(password, 8)
    console.log(password)
    console.log(hashedPassword)
    const isMatch = await bcrypt.compare('thisisapassword', hashedPassword)
    console.log(isMatch)
}

passhashingcheck()
```

### jsonwebtoken

Signing/verifying a hash

``` js
// sign the text 'foobar' using the secret key 'secret' and signature expires in 1h
const jwt = require('jsonwebtoken')
const token = jwt.sign({data: 'foobar'}, 'secret', { expiresIn: '1h' })
console.log(token)
const decoded = jwt.verify(token, 'secret')
console.log(decoded.data)
```
