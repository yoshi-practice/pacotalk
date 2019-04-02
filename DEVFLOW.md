
# 開発手順

## Angular CLIをグローバルインストール
```
$ npm install -g @angular/cli
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
$ npm install --save hammerjs
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
コンポーネントを反映させるために、`./src/app/app.component.html`）を以下の通り編集します。

```

```