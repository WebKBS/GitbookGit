# Git 명령어

## **Git 저장소 초기화:**

```bash
git init
```

이 명령어는 현재 디렉토리를 Git 저장소로 초기화하며, 이 과정에서 `.git`이라는 숨김 폴더가 생성된다. 이 명령어는 한 프로젝트 디렉토리에서 한 번만 실행되어야 한다.

{% hint style="warning" %}
프로젝트당 한번만 실행된다.
{% endhint %}

{% hint style="danger" %}
git init은 반드시 한 프로젝트(root dir)에 한번만 실행해야하고, 하위 폴더에 git init을 실행해서는 안된다.
{% endhint %}



## **변경 사항 확인:**

```bash
git status
```

이 명령어는 현재 작업 디렉토리의 변경 사항을 보여준다. 초기화된 상태에서는 "Untracked files"라는 메시지가 나타남.



## **변경 사항을 Staging Area로 추가:**

```bash
git add .
```

이 명령어는 모든 변경 사항을 Staging Area로 추가한다. 변경한 파일들이 이제 버전 관리에 포함된다.

{% hint style="info" %}
다시 git status를 하면 "Changes to be committed"라는 메시지가 나타나면서 Staging Area에 있는 변경 사항목록이 나타난다.
{% endhint %}

{% hint style="warning" %}
git add . 의 .(점)을 찍는것은 변경사항이 있는 모든 파일을 의미한다. (변경사항이 있는 모든 파일을 staging함)

만약 개별 파일을 staging하려면 아래와 같이 개별 파일이름을 사용하면된다.

```bash
git add example.txt
```
{% endhint %}





## **변경 내용을 확정하고 커밋:**

```bash
git commit -m "<커밋에 대한 메세지>"
```

\-m 은 message의 약자(m)를 뜻한다.

이 명령어는 Staging Area에 있는 변경 사항들을 확정하여 새로운 커밋을 생성한다. 커밋 메시지는 해당 커밋의 목적을 간결하게 설명하는데 사용된다.

이렇게 하면 Git 저장소가 초기화되고, 변경 이력이 기록된 후에 `git status`를 사용하여 현재 상태를 확인할 수 있다.
