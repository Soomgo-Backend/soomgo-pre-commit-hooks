# `soomgo-commit-msg-pre-commit`

커밋 메세지를 조작하는 `pre-commit` 훅

## pre-commit 설정하기

### `commit-msg-with-jira`

```yaml
- repo: https://github.com/Soomgo-Backend/soomgo-commit-msg-pre-commit
  rev: 0.1.1
  hooks:
    - id: commit-msg-with-jira
```

자동으로 커밋 메세지를 조작하는 훅입니다. 현재의 브랜치명이 `[a-zA-Z]+\/[A-Z]+\-[0-9]+` 패턴과 일치할 경우 자동으로 커밋 메세지 앞에 티켓 ID를 추가합니다. 만약 커밋 메세지에 이미 지라 티켓 ID가 포함되었을 경우나 `no-ticket`으로 시작하는 경우에는 무시됩니다.
