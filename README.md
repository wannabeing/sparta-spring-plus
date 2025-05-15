# 🚀 SPRING PLUS
<div style="display: flex; gap: 5px;">
<img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white"/>
<img src="https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white"/>
<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=Postman&logoColor=white" />
</div>

##  개요
- [📌 프로젝트 회고(velog)](https://velog.io/@wannabeing/%ED%9A%8C%EA%B3%A0-%ED%94%8C%EB%9F%AC%EC%8A%A4-%EA%B3%BC%EC%A0%9C-%ED%9A%8C%EA%B3%A0)
- 개발기간: 2025.04.30(수) ~ 2025.05.09(금)
- 자바버전: OpenJDK 17
- 사용기술: Spring Boot, JPA, MySQL
- 코드 개선, QueryDSL 적용, 테스트 코드 작성, SpringSecurity 적용

---

## Level. 1
1. 올바른 곳에 `@Transactional` 어노테이션 추가
    - [Lv1. @Transactional의 이해 커밋](https://github.com/wannabeing/sparta-spring-plus/commit/769d0cdc210f3d0dc5b60308ad61af0b7f01e38f)
2. User 정보에 nickname 필드 추가
    - [Lv1. JWT의 이해 커밋](https://github.com/wannabeing/sparta-spring-plus/commit/47f9f0b88b30de378314241b9323f20c93f723b9)
3. 할 일 검색조건 추가 및 JPQL 적용
    - [Lv1. JPA의 이해 커밋](https://github.com/wannabeing/sparta-spring-plus/commit/4ed10450e57da74a4a85f8fa51279af37532b7f4)
4. 컨트롤러 테스트 코드 수정
   - [Lv1. 컨트롤러 테스트코드의 이해 커밋](https://github.com/wannabeing/sparta-spring-plus/commit/f2233c4670dc1e45892dbbedad391e1beb3dd3dc)
5. AOP 실행전 동작하도록 수정
   - [Lv1. AOP의 이해 커밋](https://github.com/wannabeing/sparta-spring-plus/commit/7519e014cd1ce496b57921167c34d4d8a54bb5dd)

## Level. 2 
6. 할 일 저장 시, 담당자 자동등록 되도록 수정
   - [Lv2. JPA Cascade의 이해 커밋](https://github.com/wannabeing/sparta-spring-plus/commit/a61d95ce01424e6a37e87fbaca09e34a02013246)
7. 댓글 N+1 문제 해결
   - [Lv2. N+1 해결 커밋](https://github.com/wannabeing/sparta-spring-plus/commit/860acb0eba026d3469f9cd891ac18b4cfdcc9fe4)
8. findByIdWithUser 쿼리문 QueryDSL로 수정
   - [Lv2. QueryDSL 적용 커밋](https://github.com/wannabeing/sparta-spring-plus/commit/1d75738d610fae755562d38add8c822e2f59bac2)
9. SpringSecurity 적용
   - [Lv2. SpringSecurity 적용 커밋](https://github.com/wannabeing/sparta-spring-plus/commit/d13ff181aafe191bbbc95ece0f63cab708c86632)
---

## 패키지 구조
```
src
└── java
    └── org.example.expert
        ├── aop                   # AOP 관련 기능
        ├── client                # 외부 API 연동
        ├── config                # 전역 설정 관련 클래스
        ├── domain                # 도메인 패키지
        │   ├── auth              # 인증/인가 (Sign) 관련 기능
        │   ├── comment           # 댓글(Comment) 기능
        │   ├── common            # 공통 DTO, 예외 클래스 등
        │   ├── manager           # 담당자(Manager) 관련 기능
        │   ├── todo              # 일정(Todo) 관련 기능
        │   └── user              # 유저(User) 관련 기능
        └── ExpertApplication     # ✅ 메인
```