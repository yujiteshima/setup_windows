# wsl2 setup
windows11_proでは、ではじめからwsl2がインストール済みだった。
Ubuntu 22.04をインストールする
```bash
wsl --install -d Ubuntu-22.04
```
まずapt update
```bash
sudo apt update
```
gitの設定
```bash
sudo apt-get install git
git config --global user.name yujiteshima
git config --global user.email yuji.teshima@gmail.com
git config --global pull.rebase false
git config --global core.editor "code --wait"
git config --list
```
ubuntu ssh keyを作成
何回か止まるが全部enter
```bash
ssh-keygen -t rsa
```
githubにssh key登録
clip.exeに出力するとクリップボードに格納できてペーストできる
```bash
cat ~/.ssh/id_rsa.pub | clip.exe
```
接続の確認
```bash
ssh -T git@github.com
```
初回アクセスは警告が出るがYesでOK
Hi, yujiteshimaで成功
