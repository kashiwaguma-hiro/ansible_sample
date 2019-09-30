FROM ansible/ansible:ubuntu1404

# FYXME なぜか ansibleイメージで ansibleコマンドが入ってないので入れてます...
RUN pip install ansible

# ansistrano https://github.com/ansistrano/deploy を導入
RUN ansible-galaxy install ansistrano.deploy ansistrano.rollback

CMD ["/sbin/init"]
