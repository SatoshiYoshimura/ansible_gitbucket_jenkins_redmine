# ansible_gitbucket_jenkins_redmine
Enviroment  gitbucket and jenkins and redmine server using ansible in vagrant centos6.5

##使い方

前提
・Vagrant 環境がある
・Ansible が使用できる

###0.clone

```
git clone http://172.19.214.210:8080/gitbucket/git/satoshi_yoshimura/01_linux.git
```

###1.box追加 (既にある場合は飛ばして良い)

```
vagrant box add centos6.5_x86_64 https://vagrantcloud.com/nrel/CentOS-6.5-x86_64/version/4/provider/virtualbox.box
```

###2.立ち上げ

```
vagrant up
```

###3.ansible実行

```
ansible-playbook -i hosts site.yml
```


構築後は, それぞれ以下のURLでアクセスが出来ます.

- GitBucket
    - [http://192.168.33.10:8080/gitbucket/](http://192.168.33.10:8080/gitbucket/)
- Jenkins
    - [http://192.168.33.10:8090](http://192.168.33.10:8090)
- Redmine
    - [http://192.168.33.10:3000](http://192.168.33.10:3000)
