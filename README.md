# 개발 환경 설정 가이드

## 1. GitHub 계정 생성

1. [GitHub 웹사이트](https://github.com) 접속
2. "Sign up" 버튼 클릭
3. 이메일 주소, 사용자 이름, 비밀번호 입력
4. 이메일 인증 완료
5. 기본 설정 (프로필 정보, 관심사 등) 선택

## 2. Git 설치

### Windows
1. [Git 다운로드 페이지](https://git-scm.com/download/win) 접속
2. "Click here to download" 클릭하여 설치 파일 다운로드
3. 다운로드한 설치 파일 실행
4. 설치 과정에서 기본 설정 유지 (Next 클릭)
5. 설치 완료 후 Git Bash 실행하여 설치 확인
   ```bash
   git --version
   ```

### Git 기본 설정
```bash
git config --global user.name "사용자 이름"
git config --global user.email "이메일 주소"
```

## 3. Cursor IDE 설치 및 설정

### 설치
1. [Cursor 공식 웹사이트](https://cursor.sh) 접속
2. "Download" 버튼 클릭
3. 운영체제에 맞는 버전 선택하여 다운로드
4. 설치 파일 실행하여 설치 완료

### 기본 설정
1. Cursor 실행
2. GitHub 계정 연동
   - 좌측 하단의 계정 아이콘 클릭
   - "Sign in with GitHub" 선택
   - GitHub 계정으로 로그인
3. 테마 및 기본 설정
   - File > Preferences > Settings
   - 원하는 테마, 폰트 크기, 탭 크기 등 설정
4. 확장 프로그램 설치 (선택사항)
   - Extensions 메뉴에서 필요한 확장 프로그램 검색 및 설치

### Git 연동 확인
1. 새로운 프로젝트 생성 또는 기존 프로젝트 열기
2. 터미널에서 Git 명령어 실행 가능한지 확인
3. 소스 컨트롤 탭에서 Git 기능 정상 작동 확인

## 4. 첫 번째 저장소 생성 및 연동

### GitHub 저장소 생성
1. GitHub 웹사이트 접속
2. "New repository" 클릭
3. 저장소 이름, 설명 입력
4. "Create repository" 클릭

### 로컬 저장소 초기화 및 GitHub 연동
```bash
# 새 디렉토리 생성 및 이동
mkdir my-project
cd my-project

# Git 저장소 초기화
git init

# README.md 파일 생성
echo "# My Project" > README.md

# 변경사항 스테이징 및 커밋
git add README.md
git commit -m "Initial commit"

# GitHub 저장소와 연동
git remote add origin https://github.com/사용자이름/저장소이름.git
git branch -M main
git push -u origin main
```

## 5. 문제 해결

### 일반적인 문제
- Git 명령어가 인식되지 않는 경우
  - 시스템 환경 변수 PATH에 Git 경로가 제대로 설정되었는지 확인
  - 컴퓨터 재시작

- GitHub 연동 오류
  - GitHub 계정 정보 확인
  - 토큰이 만료되었는지 확인
  - 새로운 토큰 생성 및 설정

### Cursor 관련 문제
- IDE가 느리게 실행되는 경우
  - 불필요한 확장 프로그램 비활성화
  - 캐시 삭제
  - 최신 버전으로 업데이트

- Git 기능이 작동하지 않는 경우
  - Git이 올바르게 설치되었는지 확인
  - Cursor 재시작
  - 프로젝트 폴더에서 Git 초기화 확인

## 6. 현재 프로젝트 설정 과정

### Git 설정
1. Git 초기화
```bash
git init
```

2. 사용자 정보 설정
```bash
git config --global user.name "ryu-dongsoo"
git config --global user.email "ryudongsoo@jbnu.ac.kr"
```

3. 파일 추가 및 커밋
```bash
git add README.md
git commit -m "Initial commit"
```

4. GitHub 저장소 연동
```bash
git remote add origin https://github.com/ryu-dongsoo/documents.git
git branch -M main
git push -u origin main
```

### 주의사항
- GitHub에 푸시할 때는 Git Bash를 사용하는 것이 권장됨
- PowerShell에서는 일부 Git 명령어 실행 시 문제가 발생할 수 있음
- GitHub 로그인 시 브라우저를 통한 인증이 필요할 수 있음