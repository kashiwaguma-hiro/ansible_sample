# ansistrano_sample

## Usage

```
$ docker-compose up -d
$ docker exec -it ansible ansible-playbook -i local deploy.yml -e basic_username=USERNMAE -e basic_password=PASSWORD -e download_url="DOWNLOAD_URL"
```