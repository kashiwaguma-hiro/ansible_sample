# ansistrano_sample

## Usage

デプロイ対象のサーバを起動しておく
```
$ docker-compose up -d
```

デプロイをlocalインベントリを使って行う
```
$ docker exec -it ansible ansible-playbook -i local deploy.yml -e basic_username=USERNMAE -e basic_password=PASSWORD -e download_url="DOWNLOAD_URL"
```

デプロイをlocalインベントリのbatchesグループのみに反映
```
$ docker exec -it ansible ansible-playbook -i local deploy.yml --limit batches -e basic_username=USERNMAE -e basic_password=PASSWORD -e download_url="DOWNLOAD_URL"
```