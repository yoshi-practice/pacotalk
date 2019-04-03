
# 開発手順

## Angular CLIをグローバルインストール
```
$ yarn add -g @angular/cli
```

## Angular Projectを作成
```
$ ng new pacotalk --routing
$ cd pacotalk
```

## Angular material、CDK、HammerJSを追加 
```
$ ng add @angular/material \
         @angular/cdk
$ yarn add --save hammerjs
```

## Themeを追加

`style.scss`に以下を追加します。
ここではdeeppurple-amberという物を使用します。

```
@import '@angular/material/prebuilt-themes/deeppurple-amber.css';
```

## Material Moduleを作成

`./src/app/material.module.ts`を作成し、以下を入力します。

```
import {NgModule} from '@angular/core';

@NgModule({
  imports: [],
  exports: []
})
export class MaterialModule {}
```

## Material Moduleをインポート

`src/app/app.module.ts`にMaterialModuleをimportします。

```
import { MaterialModule } from './material.module';
```

`@NgModule`にもimportします。

```
MaterialModule,
```

## ナビゲーションバーを追加する
`/src/app/material.module.ts` 以下のように変更します。

```
import { NgModule } from '@angular/core';

import {
  MatSidenavModule,
  MatToolbarModule,
  MatIconModule,
  MatListModule,
} from '@angular/material';

@NgModule({
  imports: [
    MatSidenavModule,
    MatToolbarModule,
    MatIconModule,
    MatListModule,
  ],
  exports: [
    MatSidenavModule,
    MatToolbarModule,
    MatIconModule,
    MatListModule,
  ]
})
export class MaterialModule {}
```

これで、`MatSidenavModule`が使えるようになりました。
`./src/app/app.component.html`）に作成したいコンポーネントを作ってみてください。
（このままではまだ動作しません。）

## Angular Material、Flexboxの設定

```
$ yarn add @angular/flex-layout rxjs-compat
```
を実行し、`flex-layout`と`rxjs-compat`をインストールします。

## インポートと構成
`src/app/app.module.ts`で、`FlexLayoutModule`をインポートします。

```
import {FlexLayoutModule} from '@angular/flex-layout';
```

`@NgModule` でも同様にインポートします。

```
FlexLayoutModule
```

これで`fxLayout`、`fxLayoutAlign`、などのディレクティヴを追加することができました。

## ナビゲーションのCSSを調整

`src/app/app.component.css` に次のCSSを追加します。

```
mat-sidenav-container, mat-sidenav-content, mat-sidenav {
  height: 100%;
}

mat-sidenav {
  width: 250px;
}

a {
  text-decoration: none;
  color: white;
}

a:hover,
a:active {
  color: lightgray;
}

.navigation-items {
  list-style: none;
  padding: 0;
  margin: 0;
  cursor: pointer;
}

.icon {
  display: inline-block;
  height: 30px;
  margin: 0 auto;
  padding-right: 5px;
  text-align: center;
  vertical-align: middle;
  width: 15%;
}

.label {
  display: inline-block;
  line-height: 30px;
  margin: 0;
  width: 85%;
}
```