
# How to develop?

## Angular CLI global install
```
$ npm install -g @angular/cli
```

## Create an Angular Project
```
$ ng new pacotalk --routing
$ cd pacotalk
```

## Add Angular material, CDK and HammerJS 
```
$ ng add @angular/material @angular/cdk
$ npm install --save hammerjs
```

## Add theme

for `style.scss`

```
@import '@angular/material/prebuilt-themes/deeppurple-amber.css';
```

## Importing Material Components

Make `./src/app/material.module.ts` and edit

```
import {NgModule} from '@angular/core';

@NgModule({
  imports: [],
  exports: []
})
export class MaterialModule {}
```