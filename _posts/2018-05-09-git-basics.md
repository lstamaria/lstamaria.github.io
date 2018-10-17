---
layout: post
title: "Git basics"
date: 2018-05-09
---

Some of the handy git commands are:

```
/* Clone remote git address */
git clone some-remote-repo-address
```

```
/* Create local repo */
git init
```

```
/* Associate remote repo address to local repo */
sudo git remote add origin some-remote-repo-address
```

```
/* Stage changes in local repo */
git add .
```

```
/* Add message to staged changes */
git commit -m 'some message'
```

```
/* Initial upload of changes to remote repo */
git push --set-upstream origin master
```

```
/* Upload changes to remote repo */
git push -u origin
```