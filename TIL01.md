# Markdown : 간단하게 작성을 목표로

- #의 갯수에 따라 더 작은 단위의 제목이 된다
- 그냥 쓰면 문단
- - : 순서가 없는 리스트
- 1., 2., 3., : 순서가 있는 리스트
- 스페이스 두번 후 - : 부 목록
- inline code block : 마크다운을 이용해 코드를 표현하는 법 / 백틱 text 백틱
- code block : 큰 영역에 코드를 작성하여 코드로 표현하는 방법 / 백틱 x3 text 백틱X3 / 한 줄 이상 코드로 표현이 가능하다

- 작성된 코드의 언어를 설정해 줄 수 있다 : markdown의 경우 / python의 경우 표현방식이 다름
- [네이버](naver.com) : 대괄호 - 실제로 표시되는 모습 / 소괄호 - 실제 링크 내용
- ![이미지](이미지 링크) : 이미지 표시됨
- ** : 굵게 / *: 기울임 / ~~ : 취소선
- - x3 : 수평선

---

# CLI : 내가 어디 있는지(경로) 알아야 함

- 효율성
- 정밀제어
- 표준성
- 절대 경로 : Root  디렉토리부터 목적 지점까지 거치는 모든 경로를 전부 작성
- 상대 경로 : 현재 작업하고 있는 디렉토리를 기준으로 계산된 상대적 위치 작성

### 명령어

- touch : 텍스트 파일 생성
- mkdir(make directory) : 폴더 생성
- clear : 이전 명령 삭제
- ls : 무엇을 만들었는지 알려줌
- ls -l : 자세히보기
- ls -a: 모든 파일 보기
- cd(change directory) : 폴더 이동(더블클릭으로 들어가는 것과 동일)
- cd . : 현재 폴더
- cd .. : 내 부모 폴더 / 상위 폴더
- start : 폴더 / 파일 열기, 현재 os에서 지원해주는 것으로
- rm(remove) : 삭제(폴더 삭제 불가)
- rm -r hello : 폴더 삭제(폴더 삭제시 안 파일 모두 삭제)
- vi : 메모장 - i : insert 모드 - esc: 편집종료 - :w : 저장 - :q 종료 - :wq : 저장 + 종료 - :lq : 저장하지 않고 종료

---

# GIT: 분산버전관리시스템

로컬 저장소 내 모든 파일의 변경사항을 감시하고 있다.

working directory : 실제 작업 중인 파일들이 위치하는 곳 / 깃이 파악하지 않은 변경사항

staging area : 변경된 파일 중, 다음 버전에 포함시킬 파일들을 선택적으로 추가, 제외 가능 / 준비 영역

repository : 버전 이력과 파일이 영구적으로 저장

commit : 변경된 파일을 저장하는 행위

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/00d2f5e3-321b-4ae4-8059-ad38bad8c2f3/9d917636-3a4d-4318-8907-2c49b9c77cc7/image.png)

git init : 깃으로 인해 관리되는 폴더로 바꿈 / 저장소를 초기화한다

git status : 깃이 버전의 일부로 인식하지 않은 파일을 보여줌 / 워킹디렉토리에 있는 파일들을 보여줌

git add 파일 명 : 깃에 파일명 추가

git commit -m “메세지” : 사용전 내가 누구인지 알려줘야함 / 이게 무엇인지 설명

git config —global [user.email](http://user.email) “이메일” / user.nam”이름” : 내가 누군지 알려주기

git log : 지금까지 된 커밋의 역순으로 보여줌

git log —oneline : 커밋 목록 한줄로 볼 수 있음

git commit —amend : 커밋 메시지 수정

---

# GITHUB : 커밋이 올라가는 것 / 커밋이 없다면 푸시X

- push

git remote add origin 깃헙링크 : 깃헙과 리모트하기

push : 내가 있는 것을 원격으로 보낼 때

pull : 나한테 없는 것을 원격으로부터 들고올 때

git push -u origin master : github로 무시하기

git push : 깃헙에 저장

- pull/clone

git clone 깃헙링크 : 처음 깃헙에서 가져오기

git pull : 가져오기

- 파일 명.gitignore : 안에 깃헙으로 가고 싶지 않은 파일 이름을 넣으면, 깃이 무시함
- gitignore : 이미 git 관리를 받은 이력이 있는 파일은 적용되지 않음