# Yinshui [饮水]
A microblog Jekyll template inspired by twitter&fanfou


1. install bundle by `gem install bundle`
2. `bundle install`
3. `bundle exec jekyll server`

## Setting remote repotory on EC2 CMD:
Install git if not available via apt-get (Ubuntu) or yum install (CentOS)

### REMOTE

```shell
$ mkdir yinshui.git
$ cd yinshui.git
$ git init --bare
```

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

### LOCAL

```shell
chmod 400 ~/aws/w-pro15.pem
ssh-add ~/aws/w-pro15.pem

# useful command to display remote branch.
git remote -v

git remote add yinshui ec2-user@b.hengwei.me:~/repos/yinshui.git
git remote set-url yinshui ec2-user@b.hengwei.me:~/repos/yinshui.git

## push current master branch to remote yinshui.
## option1: push to remote yinshui repo according to current github remote hashref.
git push yinshui origin/master
## option2: push to remote yinshui repo according to current local head hashref.
git push yinshui master
```
