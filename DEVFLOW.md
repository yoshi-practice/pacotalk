
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

