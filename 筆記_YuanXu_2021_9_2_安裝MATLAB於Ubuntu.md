# 安裝MATLAB於Ubuntu

1.依照「MATLAB全系所授權單機版安裝說明登入官網下載.pdf」指示操作，依序創帳號並下載matlab

2.將matlab下載到「`Download`（下載）」資料夾內

3.開啟terminal，確認`matlab_R20XXX_glnxa64.zip`是否位於`~/Download`目錄

```
$ ls ~/Downloads/
```

4.創建matlab安裝5目錄

```
$ sudo mkdir -p /usr/local/MATLAB/R2021a/
```

5.回到`Downloads`目錄，創建一個臨時的目錄`matlab`，用於儲存`matlab_R20XXX_glnxa64.zip`解壓縮出來的東西

```
$ cd Downloads
$ mkdir matlab
```

6.解壓縮`matlab_R20XXX_glnxa64.zip`到剛才的`~/Downloads/matlab`當中

```
$ unzip -q matlab_R2021a_glnxa64.zip -d matlab
```

7.進入matlab目錄後，啟動Matlab安裝程序

```
$ cd matlab
$ sudo ./install
```

8.登入matlab帳號

9.選擇正確的license，台大所提供的license應為1089594

10.在Name的地方應會自動填入，無須更改。**Login Name**填入**terminal前面的名字**

11.選擇默認安裝路徑`/usr/local/MATLAB/R2021a`，通常不須更動

12.安裝全數套件

13.將Create symbolic links to MATLAB scripts in打勾，路徑為默認的`/usr/local/bin`，即可開始安裝

14.完成安裝後，利用terminal設定matlab的啟動keyword。首先將terminal移動到家目錄`~`，然後修改.bashrc

```
$ vim .bashrc
```

15.在最後面加上matlab的啟動keyword。如此一來，即可在terminal直接輸入`MATLAB`來開啟matlab

```
$ alias MATLAB='/usr/local/MATLAB/R2021a/bin/matlab'	# define MATLAB as /usr/local/MATLAB/R2020a/bin/matlab
$ source .bashrc	＃rerun .bashrc
```

