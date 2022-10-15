# TRichEdit

## SelectAll()
upadte:2022/06/27

SelectAll()メソッドをした場合、一番最後の文字ではない部分まで選択されてしまう。
そのままクリップボードコピーすると１行無駄に改行が入ってしまう。
代わりにこうする。
```C++:全選択
  richEdit->SelStart = 0;
  richEdit->SelLength = richEdit->Text.Length();
```

***
