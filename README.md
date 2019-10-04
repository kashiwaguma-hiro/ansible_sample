# ansistrano_sample

## 使い方

デプロイ対象のサーバを起動しておく
```
$ docker-compose build
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

## 参考

ベストプラクティスは[公式](https://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html) があるのでそれを見ましょう.