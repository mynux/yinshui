# Yinshui [饮水]
A microblog Jekyll template inspired by twitter&fanfou


1. install bundle by `gem install bundle`
2. `bundle install`
3. `bundle exec jekyll server`

##Setting remtoe repotory on EC2 CMD:

[REMOTE]
Install git if not available via apt-get (Ubuntu) or yum install (CentOS)
$ mkdir yinshui.git
$ cd yinshui.git
$ git init --bare

Remote hooks/post-receive
```shell
#!/bin/bash -l
GIT_REPO=$HOME/repos/t.hengwei.me.git
TMP_GIT_CLONE=$HOME/tmp/git/t.hengwei.me
PUBLIC_WWW=/var/www/t.hengwei.me

git clone $GIT_REPO $TMP_GIT_CLONE
jekyll build --source $TMP_GIT_CLONE --destination $PUBLIC_WWW
rm -Rf $TMP_GIT_CLONE
exit
```

[LOCAL]
ssh-add ~/aws/w-pro15.pem
git remote -v

git remote set-url origin ec2-user@b.hengwei.me:~/repos/yinshui.git
git remote add yinshui ec2-user@b.hengwei.me:~/repos/yinshui.git
git push origin HEAD:yinshui
