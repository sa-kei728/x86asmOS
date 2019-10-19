# x86asmOS
x86 assembly OS

## Environment
CPU: Core-i5(x86_64)<br>
OS: Windows Subsystem for Linux(Ubuntu18.04 LTS)

## Reference
・作って理解するOS x86系コンピュータを動かす理論と実践<br>
<https://gihyo.jp/book/2019/978-4-297-10847-2>
・WSL上でGUI利用<br>
<https://www.mazn.net/blog/2018/05/19/1656.html>

## install
### 1. NASM
```
apt install nasm
```
### 2. X Server by WSL
#### 1. install Xserver(VcXsrv) for WindowsOS<br>
<https://sourceforge.net/projects/vcxsrv/><br>
#### 2. apt get by WSL
```
apt-get install build-essential libssl-dev libreadline-dev zlib1g-dev x11-apps x11-utils x11-xserver-utils  fonts-ipafont libxml2-dev libxslt1-dev fontconfig libxrandr-dev
```
#### 3. link by windows font by WSL<br>
```
ln -s /mnt/c/Windows/Fonts /usr/share/fonts/windows
fc-cache -fv
```
#### 4. launch VcXsrv(default setting) and Resident App
#### 5. Display setting by WSL
```
export DISPLAY="localhost:0.0"
```

### 3. bochs
```
git submodule init
git submodule update
cd bochs/bochs
./configure
make
```
