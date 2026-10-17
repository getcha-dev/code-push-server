## 변경 내용


## 🔒 보안 체크 (PR 올리기 전)
<!-- 해당 없으면 체크하고 넘어가세요. 가이드: claude-service-agent/shared/standards/security-guide.md -->
- [ ] 새 API·경로가 인증 없이 열리지 않는다 (열린다면 이유를 본문에)
- [ ] diff 에 키·토큰·비밀번호·`-----BEGIN` 같은 값이 없다
- [ ] `NEXT_PUBLIC_`·`VITE_` 에 서버용 키를 넣지 않았다
- [ ] Dockerfile 이 `ARG`/`ENV` 로 토큰을 받거나 키 파일을 `COPY` 하지 않는다
- [ ] k8s 매니페스트(probe 헤더·env·values)에 평문 비밀이 없다
- [ ] 새 IAM·DB·ES 권한이 최소다 (`*`·`AdministratorAccess`·슈퍼유저 없음)
- [ ] 새 워크플로는 자체 러너·GitHub App 토큰을 쓴다 (사람 PAT·유료 러너 X)
- [ ] WAF·네트워크 변경이면 svc·admin·ad 세 ACL 과 WCU 를 확인했다
