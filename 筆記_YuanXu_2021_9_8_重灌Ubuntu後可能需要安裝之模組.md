# 重灌Ubuntu後可能需要安裝之模組

## Local computer中安裝module模組

1.`$ sudo apt-get install environment-modules`

2.`$ source /etc/profile`

3.`$ source .bashrc`

4.輸入`$ module`確認有無安裝完成，有顯示出版本資訊即安裝完成

## Local computer中安裝mpi模組

**若在local computer執行make mpi發生mpicxx: Command not found的話請先下載mpi模組**

1.回到local computer根目錄，接著輸入`$ sudo apt-get install mpich libmpich-dev`