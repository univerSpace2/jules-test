# Simple Blog Backend with NestJS

이 프로젝트는 NestJS 기반으로 구현된 간단한 블로그 백엔드 서비스입니다. 회원가입부터 개인 블로그 포스팅, 댓글 작성, 게시글 추천 기능까지 기본적인 블로그 기능을 제공합니다.

## 주요 기능

### 1. 사용자 인증 및 회원가입

* 사용자 회원가입 (이메일, 비밀번호)
* 로그인 및 JWT 기반 인증
* 사용자 프로필 조회

### 2. 블로그 게시글 관리

* 게시글 생성 (제목, 본문)
* 게시글 조회 (단일/전체)
* 게시글 수정 및 삭제 (작성자 본인만 가능)

### 3. 댓글 기능

* 게시글에 댓글 작성
* 댓글 조회 (해당 게시글의 전체 댓글)
* 댓글 수정 및 삭제 (작성자 본인만 가능)

### 4. 게시글 추천 기능

* 게시글에 추천(Like) 추가
* 중복 추천 방지
* 추천 취소 기능

## 기술 스택

* **Framework**: [NestJS](https://nestjs.com/)
* **Language**: TypeScript
* **Authentication**: JWT + Passport
* **Database**: PostgreSQL (TypeORM 또는 Prisma 선택 가능)

## 디렉토리 구조 (예시)

```
src/
├── auth/         # 인증 모듈
├── users/        # 사용자 모듈
├── posts/        # 게시글 모듈
├── comments/     # 댓글 모듈
├── likes/        # 추천(좋아요) 모듈
├── common/       # 공통 유틸, 인터셉터 등
└── app.module.ts # 루트 모듈
```

## 실행 방법

```bash
# 패키지 설치
yarn install

# 개발 서버 실행
yarn start:dev

# 빌드 후 실행
yarn build
yarn start
```

## 환경 변수 예시

`.env`

```
DATABASE_URL=postgresql://user:password@localhost:5432/blog
JWT_SECRET=your_jwt_secret_key
```

## 향후 개선 방향

* 이미지 업로드 기능
* 태그 및 검색 기능
* 관리자 기능 및 신고 시스템

---

이 프로젝트는 학습 목적 또는 개인 프로젝트로 사용하기 적합합니다. NestJS의 모듈화, 데코레이터 기반 아키텍처, 의존성 주입 등을 경험해보기에 좋은 예제입니다.
