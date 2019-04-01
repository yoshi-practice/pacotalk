# Pacotalk

---

## 起動方法

### 共通

```
$ git clone {PROJECT_URL}
$ cd {PROJECT_NAME}
```

### ローカル

#### npm packageのインストール
```
$ npm install
```

#### Angular CLIのグローバルインストール
```
$ npm install -g @angular/cli
```

#### 起動
```
$ npm run start
```

### docker

#### イメージのビルド
```
$ docker build -t pacotalk .
```

### 起動
```
$ docker run -p 4200:4200 -it pacotalk 
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
