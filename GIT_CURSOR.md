# GitHub 계정 생성 및 Git 설치 가이드

## 1. GitHub 계정 생성
1. [GitHub 웹사이트](https://github.com) 접속
2. "Sign up" 버튼 클릭
3. 필요한 정보 입력:
   - 사용자 이름
   - 이메일 주소
   - 비밀번호
4. 이메일 인증 완료

## 2. Git 설치
1. [Git 다운로드 페이지](https://git-scm.com/downloads) 접속
2. 운영체제에 맞는 버전 선택 및 다운로드
3. 설치 프로그램 실행
4. 기본 설정 유지하고 설치 진행
5. 설치 완료 후 컴퓨터 재시작

## 3. Git 기본 설정
1. 사용자 정보 설정:
```bash
git config --global user.name "사용자이름"
git config --global user.email "이메일주소"
```

2. 기본 편집기 설정:
```bash
git config --global core.editor "code --wait"
```

3. 설정 확인:
```bash
git config --list
```

## 4. Cursor IDE 설치
1. [Cursor 공식 웹사이트](https://cursor.sh) 접속
2. 운영체제에 맞는 버전 다운로드
3. 설치 프로그램 실행
4. 설치 완료 후 Cursor 실행

## 5. Cursor 기본 설정
1. GitHub 계정 연동
   - Cursor 실행
   - 설정 메뉴 열기 (Ctrl+,)
   - GitHub 계정 로그인

2. 테마 및 폰트 설정
   - 설정 메뉴에서 "Appearance" 선택
   - 원하는 테마와 폰트 설정

3. 확장 프로그램 설치
   - 확장 프로그램 메뉴 열기 (Ctrl+Shift+X)
   - 필요한 확장 프로그램 검색 및 설치

## 6. 첫 번째 저장소 생성 및 연동
1. GitHub에서 새 저장소 생성
   - GitHub 웹사이트 접속
   - "New repository" 클릭
   - 저장소 이름 및 설명 입력
   - "Create repository" 클릭

2. 로컬 저장소 초기화
```bash
git init
git add .
git commit -m "Initial commit"
```

3. GitHub 저장소와 연동
```bash
git remote add origin https://github.com/사용자이름/저장소이름.git
git branch -M main
git push -u origin main
```

## 7. 일반적인 문제 해결
1. Git 인증 문제
   - GitHub Personal Access Token 생성
   - Git 자격 증명 관리자에서 토큰 등록

2. Cursor GitHub 연동 문제
   - GitHub 계정 로그아웃 후 재로그인
   - Cursor 재시작

3. 저장소 푸시 실패
   - 인터넷 연결 확인
   - GitHub 저장소 권한 확인
   - 로컬 변경사항 커밋 확인

## Git 주요 명령어 참고

### 기본 명령어
```bash
# 저장소 초기화
git init

# 상태 확인
git status

# 변경사항 스테이징
git add <파일명>
git add .  # 모든 파일

# 변경사항 커밋
git commit -m "커밋 메시지"

# 원격 저장소 연결
git remote add origin <저장소URL>

# 변경사항 푸시
git push origin <브랜치명>
```

### 브랜치 관련
```bash
# 브랜치 생성
git branch <브랜치명>

# 브랜치 전환
git checkout <브랜치명>

# 브랜치 생성 및 전환
git checkout -b <브랜치명>

# 브랜치 삭제
git branch -d <브랜치명>
```

### 변경사항 관리
```bash
# 변경사항 확인
git diff

# 변경사항 취소
git checkout -- <파일명>

# 스테이징 취소
git reset HEAD <파일명>

# 커밋 취소
git reset --soft HEAD^
```

### 원격 저장소
```bash
# 원격 저장소 목록
git remote -v

# 원격 저장소 추가
git remote add <이름> <URL>

# 원격 저장소에서 가져오기
git fetch <원격저장소>

# 원격 저장소와 병합
git merge <원격저장소>/<브랜치>
```

### 히스토리 관리
```bash
# 커밋 히스토리 확인
git log

# 간단한 히스토리 확인
git log --oneline

# 특정 파일의 히스토리
git log -- <파일명>
```

### 태그 관리
```bash
# 태그 생성
git tag <태그명>

# 태그 푸시
git push origin <태그명>

# 모든 태그 푸시
git push origin --tags
``` 