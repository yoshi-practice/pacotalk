# Pacotalk

---

## 起動方法

### 共通

```
$ git clone {PROJECT_URL}
$ cd {PROJECT_NAME}
```

### ローカル

#### yarn packageのインストール
```
$ yarn install
```

#### Angular CLIのグローバルインストール
```
$ yarn grobal add @angular/cli
```

#### 起動
```
$ yarn start
```

### docker

#### イメージのビルド
```
$ docker build -t pacotalk .
```

### 起動
```
$ docker run -p 4200:4200 -t pacotalk 
```

### ターミナルを起動
```
$ docker run -p 4200:4200 -it pacotalk ash
```

### docker-compose

#### サービスの開始
```
$ docker-compose up --build
```

#### サービスの停止
```
$ docker-compose stop
```

#### コンテナの停止
```
$ docker-compose down
```
