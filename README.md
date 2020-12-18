# Docker-enviroment
使い回しの効くdocker環境を保存

jupyter lab & python script を使用でいる環境

## 実行方法

1. Dockerfileに  `ENV http_proxy`  や`ENV https_proxy`がある場合は環境のproxyを設定
2. `docker-compose up -d`
3. `localhost:8000` や `localhost:8888` でjupyterlabを起動でいる
