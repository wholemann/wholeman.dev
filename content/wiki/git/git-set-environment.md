---
title: "Git 환경 설정"
date: "2019-12-06 15:26:20 +0900"
template: "wiki"
draft: false
slug: "/wiki/git-set-environment"
category: ""
tags:
---

# git 안내 메시지 영어로 설정하기

mac에서 git 안내 메시지가 영어로 설정되는 경우가 있는데
에러 메시지는 영어로 검색해야 해결법이 잘 나오기 때문에 영어로 설정하자.

~/.bashrc or ~/.zshrc 파일에 아래 코드를 추가하면 됨.

```
alias git="LANG=\"en_US.UTF-8\" git"
```

그 후 source ~/.bashrc (or source ~/.zshrc)
