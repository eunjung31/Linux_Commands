# Linux_Commands
Some useful commands for Linux users

---

## 경로

|명령어|설명|
|------|---|
|pwd|현재 디렉토리|
|cd|경로로 이동|
|cd ~|홈 디렉토리로 이동; ~ : 틸드|
|cd -|직전 경로로 이동|

---

## 폴더 리스트
|명령어|설명|
|------|---|
|ls|폴더 내 파일/폴더 리스트 보기|
|ls -l|ls + 상세정보|
|ls -a|ls + 숨겨진 리스트까지 보기|
|ls -al / ls -la|ls + 상세정보 + 숨겨진 리스트까지 보기|
|ls -l 폴더이름|해당 폴더 내 list만 보기|
|ls -l -d 폴더이름|해당 폴더 내 list만 보기 + 자세한 정보|


---

## 파일/폴더 관리 
|명령어|설명|
|------|---|
|touch 파일이름|새로운 파일 생성|
|mkdir 폴더이름|새로운 폴더 생성|
|mkdir '폴더 이름'|새로운 폴더 생성; 폴더 이름에 공백이 있을 경우 (not suggested)|
|mv|파일/폴더 이름 변경; 폴더/파일 위치 변경|
|mv -i 이동할 위치|파일/폴더 이동; 덮어쓸 위험이 있는 경우 사용|
|cp 파일이름1 파일이름2|파일 복사|
|cp -i 파일이름1 파일이름2|파일 복사; 덮어쓸 위험이 있는 경우 사용 |
|cp -r 폴더이름1 폴더이름2|폴더 복사|


---

## 파일 내용 출력 1
|명령어|설명|
|------|---|
|cat 파일이름|파일 내용 출력|
|cat 파일이름1 파일이름2|파일1 파일2 이어붙여서 출력|
|less 파일이름|파일 내용 출력; 시각적으로 cat보다 직관적으로 출력|
|less 파일이름1 파일이름2|파일1 파일2 이어붙여서 출력|

* less 명령어와 관련된 key
 - g : 가장 처음 부분
 - G : 가장 끝 부분
 - :p : 이전 페이지
 - :P : 다음 페이지


## 파일 내용 출력 2
|명령어|설명|
|------|---|
|head 파일이름|파일 앞부분 10줄 출력|
|head -n 20 파일이름|파일 앞부분 20줄 출력|
|tail 파일이름|파일 끝부분 10줄 출력|
|tail -n 20 파일이름|파일 끝부분 20줄 출력|

* 파일에서 3번째 줄만 보고싶다면? 
 => head -n 3 파일이름 | tail -n 1 
 
 ---
 
 ## 이전 커맨드 확인하기
|명령어|설명|
|------|---|
|history|이전 커맨드 확인|
|!커맨드번호|해당 커맨드 실행|

---

 ## 터미널 사용 꿀팁
|명령어|설명|
|------|---|
|ctrl+a|명령어 시 맨 앞으로 이동|
|ctrl+e|명령어 시 맨 뒤으로 이동|
|clear|터미널 깨끗하게 지우기|

---

 ## vim
 * 일반 모드, 입력 모드, 비주얼 모드, 명령 모드  
 ![vim_modes](https://kirkim.github.io/assets/img/etc/vim_image1.png)


### 일반 모드
![일반모드_hjkl](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSdW8Wrdr58Ib3E7i1eOBm8KCBjPYKGrWopMg&usqp=CAU)

|명령어|설명|
|------|---|
|h|왼쪽으로|
|l|오른쪽으로|
|k|위로|
|j|아래로|
|0|그 줄에서 제일 앞으로|
|$|그 줄에서 제일 뒤로|
|ctrl+g|현재 위치가 몇 번째 줄인지|
|gg|파일 제일 앞으로|
|G|파일 제일 뒷줄로|
|x|한 단어씩 지우기|
|숫자 x|여러 단어씩 지우기|
|dd|문장 지우기|
|숫자 dd|여러 문장 지우기|
|u|뒤로가기(작업 취소)|


 ### 입력 모드
|명령어|설명|
|------|---|
|i|현재 커서 위치에서 입력 모드로 변경|
|a|현재 커서 위치보다 한 칸 뒤에서 입력 모드로 변경|
|o|현재 커서 위치보다 한 줄 뒤에서 입력 모드로 변경|
|I|현재 커서 줄 맨 앞에서 입력 모드로 변경|
|A|현재 커서 줄 맨 뒤에서 입력 모드로 변경|
|O|현재 커서 줄 앞 줄에서 입력 모드로 변경|


 ### 명령 모드
|명령어|설명|
|------|---|
|:w|저장|
|:q|나가기|
|:wq|저장+나가기|
|:q!|강제 종료|
|/word|텍스트 검색|
|n|텍스트 검색 후 다음|
|N|텍스트 검색 후 이전|
|:s/치환전/치환후|한 줄에서 단어 치환|
|%s/치환전/치환후|모든 줄에서 단어 치환; but 줄마다 하나|
|%s/치환전/치환후/g|모든 단어 치환|
|%s/치환전/치환후/gc|모든 단어 치환, but 어떤 단어를 바꿀지 선택|


## 비주얼 모드
|명령어|설명|
|------|---|
|v|글자 단위 블록 씌우기|
|V|문장 단위 블록 씌우기|
|블록 후 + x|블록된 부분 삭제|
|블록 후 + y|블록된 부분 복사|
|p|복사한 부분 다음 줄에 붙여넣기|
|P|복사한 부분 이전 줄에 붙여넣기|


## 기타
|명령어|설명|예시|
|------|---|---|
|man|remote에 올라간 해당 커밋번호를 되돌림|man cal|
|apt install 설치패키지이름|패키지 설치|
|dpkg -L 설치패키지이름|패키지 설치 경로|
|apt remove 설치패키지이름|패키지 |


---

