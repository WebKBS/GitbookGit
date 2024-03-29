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

만약 여러 파일을 이어서 add하고 싶다면

```bash
git add example1.txt example2.txt
```

위 처럼 띄어쓰기 한칸으로 다음 파일 이름을 입력하면 된다.
{% endhint %}



## **변경 내용을 확정하고 커밋:**

```bash
git commit -m "<커밋에 대한 메세지>"
```

\-m 은 message의 약자(m)를 뜻한다.

이 명령어는 Staging Area에 있는 변경 사항들을 확정하여 새로운 커밋을 생성한다. 커밋 메시지는 해당 커밋의 목적을 간결하게 설명하는데 사용된다.

이렇게 하면 Git 저장소가 초기화되고, 변경 이력이 기록된 후에 `git status`를 사용하여 현재 상태를 확인할 수 있다.

{% hint style="info" %}
커밋을 할때 무엇이 변경되었는가에 대한 설명 메세지는 반드시 남겨두자.
{% endhint %}



## **커밋 이력 확인:**

```bash
git log
```

이 명령어는 현재까지의 커밋 이력을 보여준다. 커밋 메시지, 저자, 날짜 등이 표시되며, 최신 커밋이 가장 상단에 나열된다.

### Option

* \--oneline

```bash
git log --oneline
```

이 명령어는 간략한 한 줄로 표시된 커밋 이력을 보여준다. 각 줄은 커밋 해시와 커밋 메시지로 구성되어 있다.

`git log --oneline`을 통해 간략하게 커밋 이력을 확인할 수 있다. 이 옵션은 프로젝트의 커밋 이력을 더 간결하게 보고 싶을 때 유용하다.



* \--amend

```bash
git commit --amend
```

이 명령을 실행하면 텍스트 편집기가 열리면서 커밋 메시지를 변경할 수 있고, \
추가로 파일을 스테이징할 수 있다. 저장하고 나가면 Git은 최근 커밋을 수정하고 새로운 커밋을 만든다.\
실수로 commit을 했을때 수정이 가능한 방법중 하나.
