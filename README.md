# [Material-UI](http://callemall.github.io/material-ui/)

Material-UIは、[Googleマテリアルデザイン](https://www.google.com/design/spec/material-design/introduction.html)が埋め込まれた[React](http://facebook.github.io/react/)コンポーネント、及びCSSフレームワークです。

動くサンプルは、[ドキュメンテーションサイト](http://www.material-ui.com/)をご確認下さい。
まだまだ作成途中ですが、私たちがどこに向かっているのか理解することができるかと思います。

## インストール方法

Material-UIは、[npmパッケージ](https://www.npmjs.org/package/material-ui)として利用することができます。
```sh
npm install material-ui
```

依存関係の管理とJSXの変換は、[browserify](http://browserify.org/)と[reactify](https://github.com/andreypopp/reactify)をご使用下さい。
CSSフレームワークは、[Less](http://lesscss.org/)によって実装されています。


## 使用方法

一度、Material-UIをプロジェクトに入れると以下のようにコンポーネントを使用することができます。
```js
/**
 * @jsx React.DOM
 */

var React = require('react'),
  mui = require('material-ui'),
  PaperButton = mui.PaperButton;

var SomeAwesomeComponent = React.createClass({

  render: function() {
    return (
    	<PaperButton type={PaperButton.Types.FLAT} label="Default" />
    );
  }

});

module.exports = SomeAwesomeComponent;
```

## カスタマイズ方法

スタイルシートは2つのlessファイルに分割されています。
* src/less/scaffolding.less
* src/less/components.less

これにより、全ての定義されている変数を[custom-variables.less](https://github.com/callemall/material-ui/blob/master/src/less/variables/custom-variables.less)の上書きのみで、Material-UIのソースを直接変更することなくカスタマイズすることが可能です。
以下実例ですが、main.lessファイルからは以下ように参照されます。
```css
@import "node_modules/material-ui/src/less/scaffolding.less";

//Define a custom less file to override any variables defined in scaffolding.less
@import "my-custom-overrides.less";

@import "node_modules/material-ui/src/less/components.less";
```

## コントリビュート
Material-UIは私たちの敬愛する[React](http://facebook.github.io/react/)と[Googleマテリアルデザイン](http://www.material-ui.com/)から誕生しました。
私たちは、現在[Call-Em-All](https://www.call-em-all.com/)というプロジェクトでこれを使用しています。
支援をしたい場合は、[docs folder](https://github.com/callemall/material-ui/tree/master/docs)をチェックしてみてください。どんな支援も歓迎します。

### その他の言語

[English](https://github.com/callemall/material-ui)