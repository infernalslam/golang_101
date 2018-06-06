# golang_101
Let's try golang
First time to set PATH Golang

Bash
___

Edit your `~/.bash_profile` to add the following line:

```
export GOPATH=$HOME/go
```
Save and exit your editor. Then, source your `~/.bash_profile.`
```
 source ~/.zshrc
```

Note: Set the GOBIN path to generate a binary file when go install is run.

```
export GOBIN=$HOME/go/bin
```

Zsh
___

Edit your `~/.zshrc` file to add the following line:

```
export GOPATH=$HOME/go
```
Save and exit your editor. Then, source your `~/.zshrc.`

```
source ~/.zshrc
```

window (Windows 10)
___

Left click on "Search" and type `env` or `environment`. select `Edit environment variables` for your account

* Create folder at `C:\go-work`.
* Right click on "Start" and click on "Control Panel". Select "System and Security", then click on "System".
* From the menu on the left, select the "Advanced systems settings".
* Click the "Environment Variables" button at the bottom.
* Click "New" from the "User variables" section.
* Type GOPATH into the "Variable name" field.
* Type C:\go-work into the "Variable value" field.
* Click OK.


Import paths
An import path is a string that uniquely identifies a package. A package's import path corresponds to its location inside a workspace or in a remote repository (explained below).

The packages from the standard library are given short import paths such as "fmt" and "net/http". For your own packages, you must choose a base path that is unlikely to collide with future additions to the standard library or other external libraries.

If you keep your code in a source repository somewhere, then you should use the root of that source repository as your base path. For instance, if you have a GitHub account at github.com/user, that should be your base path.

Note that you don't need to publish your code to a remote repository before you can build it. It's just a good habit to organize your code as if you will publish it someday. In practice you can choose any arbitrary path name, as long as it is unique to the standard library and greater Go ecosystem.

We'll use github.com/user as our base path. Create a directory inside your workspace in which to keep source code:

```
 mkdir -p $GOPATH/src/github.com/user
```

Your first program

```
mkdir $GOPATH/src/github.com/user/hello
```
Next, create a file named hello.go inside that directory, containing the following Go code.
```golang
package main

import "fmt"

func main() {
	fmt.Printf("Hello, world.\n")
}
```

Now you can build and install that program with the go tool:
```
$ go install github.com/user/hello
```

Note that you can run this command from anywhere on your system. The go tool finds the source code by looking for the github.com/user/hello package inside the workspace specified by GOPATH.

You can also omit the package path if you run go install from the package directory:
```
$ cd $GOPATH/src/github.com/user/hello
$ go install
```

etc, https://golang.org/doc/code.html


