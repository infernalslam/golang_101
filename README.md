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



