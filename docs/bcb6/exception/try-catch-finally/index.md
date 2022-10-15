# 例外

## try-chatch-finallyの書き方
upadte:2022/06/24

try catch finally は１つにまとめることはできない。
```C++:✖try-catch-finally
  try{
    throw Exception("わざとエラー");
  }
  catch(Exception &e){
    ShowMessage("catch");
  }
  __finally{
    ShowMessage("finally");
  }
```

実現するにはこうする。
```C++:〇try-catch-finally
  try
  {
    try{
      throw Exception("わざとエラー");
    }
    catch(Exception &e){
      ShowMessage("catch");
    }
  }
  __finally{
    ShowMessage("finally");
  }
```
