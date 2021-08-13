# opencv
opencvとりあえず

https://github.com/opencv/opencv
にあるcascadeファイルを
/usr/local/opt/opencv/share/OpenCV/
におくといい。なかったらmkdirで順次作っていく


一応環境構築シート

まず作業するディレクトリを作ってそこに移動したのち仮想環境を作る
cd Desktop
mkdir coordinate(ほんとはなんて名前でもいいけど)
python -m venv .venv


仮想環境の中に入ってみてバージョン確認、そのあと抜ける
source .venv/bin/activate
python -V
(そしたら多分普段使ってるやつと同じバージョンが表示される）
deactivate

pyenvのバージョン確認
pyenv versions
pyenv 
→pyenvが通らない場合
https://qiita.com/koooooo/items/b21d87ffe2b56d0c589b

venvのバージョンを3.8.5に変更する
pyenv install 3.8.5
pyenv global 3.8.5
python -m venv .venv --clear

仮想環境の中に入ってみて再度バージョン確認、3.8.5になってればok
source .venv/bin/activate
python -V
3.8.5ならおk

仮想環境にいるまま、pipをアップグレードして、opencvをインストールする
pip install --upgrade pip
pip install opencv-python

次にcascadeファイルを入れる。（もしかしたらデフォで入ってるかも）
https://github.com/opencv/opencv
/usr/local/opt/opencv/share/OpenCV/
ファイルをここに移動

＊チームM1のpyenv
arch -arch x86_64 env PATH=${PATH/\/opt\/homebrew\/bin:/} pyenv install 3.8.5
CPPFLAGS="-I$(brew --prefix zlib)/include" pyenv install -v 3.8.5


Successfully installed numpy-1.21.1 opencv-python-4.5.3.56
