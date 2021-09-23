# 在Ubuntu環境下連接台灣杉X號

## 連接一號

方法有兩種

### 法一

​	開啟終端機，並在指令行輸入`$ ssh 使用者名稱@140.110.148.11`

### 法二(推薦)：設定快速指令

​	1.修改.bashrc

```
$ vim .bashrc
```

​	2.定義指令

```
$ alias NAR='ssh 使用者名稱@140.110.148.11'
```

​	3.寫入並儲存後，使用`$ source .bashrc`，讓.bashrc重新啟動

​	4.輸入`$ NAR`及可連接上一號機

## 連接二號

方法有兩種

### 法一

​	開啟終端機，並在指令行輸入`$ ssh 使用者名稱@ln01.twcc.ai`

### 法二(推薦)：設定快速指令

​	1.修改.bashrc

```
$ vim .bashrc
```

​	2.定義指令

```
$ alias TWCC='ssh 使用者名稱@ln01.twcc.ai'
```

​	3.寫入並儲存後，使用`$ source .bashrc`，讓.bashrc重新啟動

​	4.輸入`$ TWCC`及可連接上一號機

## 資料夾連接

## 一號機-> Local computer

1.先在local computer的家目錄建立一個用於掛載的資料夾(也就是要將一號機上的檔案同步到local computer的那個資料夾)，名為NAR

```
$ mkdir NAR
```

2.利用`$ vim .bashrc`修改.bashrc

3.加入快速指令

```
alias SSHFS_NAR='sshfs 國網主機名稱@140.110.148.11:/home/國網主機名稱/ NAR/'
```

**注意：NAR前面的空格一定要打，因為前半段是一號機的路徑，後半段是local computer的路徑**

4.寫入並退出.bashrc之後，用`$ source .bashrc`重新run一次.bashrc

5.執行該快速指令即可連接

```
$ SSHFS_NAR
```

## 二號機->Local computer

1.先在local computer的家目錄建立一個用於掛載的資料夾(也就是要將二號機上的檔案同步到local computer的那個資料夾)，名為TWCC

```
$ mkdir TWCC
```

2.利用`$ vim .bashrc`修改.bashrc

3.加入快速指令

```
alias SSHFS_TWCC='sshfs 國網主機名稱@ln01.twcc.ai:/home/國網主機名稱/ TWCC/'
```

**注意：TWCC前面的空格一定要打，因為前半段是二號機的路徑，後半段是local computer的路徑**

4.寫入並退出.bashrc之後，用`$ source .bashrc`重新run一次.bashrc

5.執行該快速指令即可連接

```
$ SSHFS_TWCC
```

