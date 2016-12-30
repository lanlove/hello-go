# hello-go
[learning go lang](https://golang.org/doc/install)

### install in linux
$ wget https://storage.googleapis.com/golang/go1.7.4.linux-amd64.tar.gz <br>
$ tar zxvf go1.7.4.linux-amd64.tar.gz <br>
$ vim .bash_profile <br>
加入以下個人化設定：

    # set go lang
    export GOROOT=$HOME/go
    export GOPATH=$HOME/{filename}
    export PATH=$PATH:$GOPATH/bin

$ source .bash_profile

這樣就完成基本安裝，直接下 go 應該會出現說明

###go 專案的基本目錄架構如下：
<pre>
bin/
    hello                          # command executable
    outyet                         # command executable
pkg/
    linux_amd64/
        github.com/golang/example/
            stringutil.a           # package object
src/
    github.com/golang/example/
        .git/                      # Git repository metadata
 hello/
     hello.go               # command source
 outyet/
     main.go                # command source
     main_test.go           # test source
 stringutil/
     reverse.go             # package source
     reverse_test.go        # test source
    golang.org/x/image/
        .git/                      # Git repository metadata
 bmp/
     reader.go              # package source
     writer.go              # package source
    ... (many more repositories and packages omitted) ...
</pre>

接下來就是要開自己的專案目錄
<pre>
$ mkdir {filename}/src/github.com/{user}/hello
</pre>
開好後在這目錄下新增一隻 hello.go
<pre>
package main

import "fmt"

func main() {
 fmt.Printf("Hello, world.\n")
}
</pre>
<pre>
$ go install github.com/lanlove/hello
<pre>
這樣會 compile 一隻 hello 執行檔到 {filename}/bin/ 裡

第一步就完成惹～恭喜恭喜

### 跟 github 做連結
<pre>
$ cd work/
$ git init
$ git commit -a -m "initial commit"
$ git remote add origin git@github.com:lanlove/hello-go.git
$ git push -u origin master
</pre>
