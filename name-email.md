---
description: Git 이름 및 Email 설정
---

# name 및 email설정

## name 설정

```bash
git config --global user.name "<이름>"
```

위 처럼 설정하면 이름이 설정된다.

```bash
git config user.name
```

위 코드를 입력하면 본인이 설정한 name을 확인할 수 있다.



## email 설정

```bash
git config --global user.email example@gamil.com
```

이메일을 설정한다.

{% hint style="info" %}
이메일은 차후 깃허브에 로그인할때 사용하는 이메일을 설정하는 것을 추천한다.
{% endhint %}



아래는 설정한 이메일 확인방법

```bash
git config user.name
```
