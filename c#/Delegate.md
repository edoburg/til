Delegate
==========

cにおける関数ポインタに近いもの
* 複数のメソッドを同時に参照できる
* 

書き方
------

定義

``` csharp
delegate 戻り値の型 デリゲート型名(引数リスト)

delegate void SomeDelegate(int n);
```

使い方

``` csharp

    delegate int DelegateFunc(double d);

    class DelegateTest
    {
        static void Test()
        {
            DelegateFunc f = A;
            f += B;
            f(123.4);
        }

        static int A(double d)
        {
            return (int)d;
        }

        static int B(double d)
        {
            Console.WriteLine("function B {0}", d);
            return (int)(d * d);
        }
    }

```

