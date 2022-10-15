# TImage

## 画像のサイズ変更
upadte:2022/06/24

フォームサイズによってイメージサイズを変更させたい場合、
```C++:サイズ変更
img->Height = 100;
img->Width = 100;
```
としても画像自体のサイズは変わらない。
コントロール自体のサイズは変更されるが、
中の画像のサイズは変更されない。

画像を変更したい場合は
img->Picture->Bitmap->Height = ***;
をすることで、画像自体のサイズを変更できる。
```C++:サイズ変更
img->Picture->Bitmap->Height = 100;
img->Picture->Bitmap->Width = 200;
```
***

