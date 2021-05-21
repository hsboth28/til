#結論
 * 親コンポーネントでuseStateと関数を定義
 * propsとしてその関数を子コンポーネントに渡す
 * 子コンポーネントでそれを実行して更新

<!-- TypeScript+Reactの記事全然無いのでQiitaに投稿する -->

パラメータ（Props）?をつけて
オプショナルパラメーターにするとundefined型も一緒に定義されるので引数を渡さなかった場合はundifinedになる。
なのでそのままだとundifinedになる可能性があるのでエラーになる。
対策方法

処理をパラメータの存在を確認するif文で囲んであげる
```JavaScript:'undefined' の可能性があるオブジェクトを呼び出すことはできません。
  if (optionParam) {
      optionParam(isState);
    }
```
