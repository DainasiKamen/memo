# 例外

## try-finally時のreturnの注意点
upadte:2022/06/24

tryの中でreturnして、そのあとにfinallyで何か処理する場合、
メソッド内で宣言した変数がreturn時点で初期化(解放？)してしまう。
下記のコードの場合、strは空のメッセージが表示される。
```C++:✖try-finally
    AnsiString str = "初期値";
    try
    {
        return;
    }
    __finally
    {
        ShowMessage(str);
    }
```
try-finally時はreturnを入れないのが吉である。
