---
title: "리얼 리눅스 Git 강의 요약"
date: "2019-12-06 15:37:02 +0900"
template: "wiki"
draft: false
slug: "/wiki/real-linux-training"
category: ""
tags:
---

### Git 상태확인 명령어 (중간중간 치면서 수시로 확인하자)
- git show
- git log
- git shortlog
- git diff
- git status
- git log --oneline

### Commit message signed

- 요즘은 Signed-off-by 방식을 쓰진 않고 CLA(contributor license agreement) 를 씀.

### Commit 수정

- 가장 최신 커밋에 덮어씌우는 방식.

```bash
git commit --amend
```

- base는 remote 기준이고 --amend를 하면 local의 history가 base와 달라지기 때문에 --force가 필요.

```bash
git push origin master --force
```

### Pull request

- 전송단위는 branch
- base와 내가 제출하는 branch와 compare
- master는 총 3개. local, remote(origin), remote(upstream)
- checkout은 .git으로부터 가져오는 것.

```bash
git checkout -- test.c
```

### rebase

- upstream의 base와 local의 base는 달라질 수 있다. 그래서 base의 갱신(re) 필요 => rebase.
- pull: fetch + merge;
- fetch: .git에 넣어놓기만 함.
- upstream의 base가 변하는 경우(중간 commit을 수정했다거나) rebase에서 충돌나는 경우가 있음. 그래서 push --force를 제어하는 것.

```bash
git fetch upstream master
git rebase upstream/master
// 만약 pull request를 보내놓은 branch를 rebase 했다면
// push -f 를 하면 자동으로 pull request도 갱신된다.
git push origin develop -f
```

- rebase 중 했던 작업을 모두 초기화

```bash
git rebase --abort
```

- 커밋 지우기: git reset --hard HEAD~1
- 전체복구하기: git reset --hard origin/master
- rebase 시 같은 파일을 작업하여 충돌이 난다면 충돌을 해결하고

```bash
git add [수정된 파일]
git rebase --continue (rebase 중 충돌이 났기 때문에 rebase --continue를 해줘야 함)
```

### 오픈 소스 커밋하기

- commit 메시지는 Why: 70~80% How: 20~30%
- commit 예시)

```bash
Fs/ex4: Fix the B problem

When ~~~, the B error can occur.
The reason is that  ~~~

Before: 
After: 

Fixes: the commit 5637d49 ("fs/ext4: Add B feature")
Fixes: #91

Cc: Namhung Kim <namhyung@kernel.org>
Reviewed-by:
Suggested-by:
Reported-by:
```
