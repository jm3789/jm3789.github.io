## 1. Repository 생성하여 GitHub page 시작
웹페이지로 만들어질 repo를 생성하고 로컬 저장소에 연결함.
- Github에서 (username).github.io 이름의 Repo 생성
- Repo를 로컬 저장소와 연결
  - Remote Repository의 주소를 복사 
  - git clone을 이용하여 로컬 저장소와 연결
- index.html로 웹페이지에 보일 예시 파일 작성, github에 push
  - git commit -m "msg"로 커밋 남김
  - git branch -M main 으로 현재 branch의 이름을 main으로 변경

## 2. Jekyll 시작, 첫 포스트 업로드
Jekyll을 설치하고, local에 문서를 편집하여 웹페이지를 관리함.
- 현재 디렉토리에 jekyll new . --force로 Jekyll 설치
- (bundle exec) jekyll serve 실행 후, localhost:4000 접속
- _config.yml에서 정보를 수정
  - (해당 진행 상황을 commit 및 push했으나 이후에 생긴 문제를 해결하던 중 커밋이 삭제됨)
- _posts 폴더에 2021-11-11-new_post.md 문서 생성, 포스트 내용 작성
  - markdown 형식
- 로컬 저장소에 commit 및 push

## 3. 테마 추가
Git blog에 Lanyon 테마를 적용함.
- git clone으로 poole/lanyon 저장소를 로컬에 받아옴
- 변경된 파일들을 git에 push
  - (웹페이지에 문제가 생겨 커밋과 삭제를 여러 번 반복하였으나, 이후 _config.yml 문서에서 baseurl 부분을 주석 처리하여 해결함)

## 4. 댓글 추가
Disqus를 이용해 댓글 기능을 추가하여 블로그를 Customize함.
- Disqus에 가입하고, Website URL에 github page 주소 입력하여 연결
  - Platform 중 Jekyll 선택
- _config.yml에 comment와 관련된 key와 value를 추가
- disqus 홈페이지에서 Universal Code를 복사하고 post.html에 붙여넣음
 - comments: True로 지정된 글에만 댓글이 허용되도록 코드를 수정
- 로컬 저장소에 commit 및 push
