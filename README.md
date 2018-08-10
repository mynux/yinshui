# Yinshui [饮水]
A microblog Jekyll template inspired by twitter&fanfou


1. install bundle by `gem install bundle`
2. `bundle install`
3. `bundle exec jekyll server`

Remtoe repotory on EC2 CMD:

[REMOTE]
Install git if not available via apt-get (Ubuntu) or yum install (CentOS)
$ mkdir fanfou.git
$ cd fanfou.git
$ git init --bare

[LOCAL]
sh-add ~/aws/w-pro15.pem
git remote add ec2-user@mynux.cn:~/repos/fanfou.git
git remote -v
git remote rm yinshui

git remote set-url yinshui ec2-user@b.hengwei.me:~/repos/yinshui.git
git remote add yinshui ec2-user@b.hengwei.me:~/repos/yinshui.git
git push origin HEAD:yinshui
