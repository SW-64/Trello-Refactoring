# 🖥️ NestJs Trello Project (팀 협업 개발도구 만들기) 

![thumbnail](https://github.com/user-attachments/assets/974904ff-6aa1-4c4e-bcfa-350b3bdb383b)

## 목차 
- 프로젝트 소개 
- 팀원 구성
- 개발 기간
- 개발 환경
- API 명세서 및 ERD 와이어 프레임
- 파일 구조
- 나의 역할
- 주요 기능 및 설명
- 트러블 슈팅


---
## 프로젝트 소개
- 프로젝트 이름 : Trello Proejct
- 내용 : NestJs를 이용한 팀 협업 개발도구 만들기
- 구분 : 팀 프로젝트
- GitHub : https://github.com/ysys29/p6.teamTrello
--- 
## 팀원 구성
- 팀장 : 이강산 [@KangSanLee24](https://github.com/KangSanLee24)
- 팀원 : 이연서 [@ysys29](https://github.com/ysys29)
- 팀원 : 이성운 [@SW-64](https://github.com/SW-64)
- 팀원 : 나지윤 [@jiyoon-na](github.com/jiyoon-na)
- 팀원 : 유승엽 [@seungyeopyoo](https://github.com/seungyeopyoo)

##  개발 기간
2024.07.11 ~ 2024.07.17
--- 
##  개발 환경
- 운영체제 : Window/Mac
- BackEnd : TypeScript, NestJs, MySQL(TypeORM)
- Tool : Visual Studio Code, Insomnia, DBeaver, Swagger

---
## API 명세서 및 ERD 와이어 프레임
- API 명세서 
![image](https://github.com/user-attachments/assets/e5ebabd4-19b2-40d4-9216-96a8dc7443c4)


- ERD 
![image](https://github.com/user-attachments/assets/2d82a2de-05c7-4347-a784-27b0816d8a5f)

- 와이어프레임 
![와이어프레임 PNG](https://github.com/user-attachments/assets/afc65fcc-3df3-4467-95f8-eff0519977b4)
---
### 폴더 구조

```markdown
📦.github
📦.vscode
📦coverage
📦dist
📦node_modules
📦src
 ┣ 📂auth
 ┃ ┣ 📂dtos
 ┃ ┣ 📂interfaces
 ┃ ┣ 📂strategies
 ┃ ┣ 📜auth.controller.ts
 ┃ ┣ 📜auth.module.ts
 ┃ ┣ 📜auth.service.spec.ts
 ┃ ┗ 📜auth.service.ts
 ┣ 📂board
 ┃ ┣ 📂dtos
 ┃ ┣ 📂entities
 ┃ ┣ 📜board.controller.ts
 ┃ ┣ 📜board.module.ts
 ┃ ┣ 📜board.service.spec.ts
 ┃ ┗ 📜board.service.ts
 ┣ 📂card
 ┃ ┣ 📂dto
 ┃ ┣ 📂dummies
 ┃ ┣ 📂entities
 ┃ ┣ 📜card.controller.ts
 ┃ ┣ 📜card.module.ts
 ┃ ┣ 📜card.service.spec.ts
 ┃ ┗ 📜card.service.ts
 ┣ 📂comment
 ┃ ┣ 📂dto
 ┃ ┣ 📂entities
 ┃ ┣ 📜comment.controller.ts
 ┃ ┣ 📜comment.module.ts
 ┃ ┗ 📜comment.service.ts
 ┣ 📂configs
 ┣ 📂email
 ┃ ┣ 📂dtos
 ┃ ┣ 📂entities
 ┃ ┣ 📜email.controller.ts
 ┃ ┣ 📜email.module.ts
 ┃ ┗ 📜email.service.ts
 ┣ 📂invitation
 ┃ ┣ 📂dtos
 ┃ ┣ 📂entities
 ┃ ┣ 📂types
 ┃ ┣ 📜invitation.controller.ts
 ┃ ┣ 📜invitation.module.ts
 ┃ ┗ 📜invitation.service.ts
 ┣ 📂list
 ┃ ┣ 📂dtos
 ┃ ┣ 📂dummies
 ┃ ┣ 📂entities
 ┃ ┣ 📂types
 ┃ ┣ 📜list.controller.ts
 ┃ ┣ 📜list.module.ts
 ┃ ┣ 📜list.service.spec.ts
 ┃ ┗ 📜list.service.ts
 ┣ 📂user
 ┃ ┣ 📂dtos
 ┃ ┣ 📂entities
 ┃ ┣ 📜user.controller.spec.ts
 ┃ ┣ 📜user.controller.ts
 ┃ ┣ 📜user.module.ts
 ┃ ┣ 📜user.service.spec.ts
 ┃ ┗ 📜user.service.ts
 ┣ 📜app.controller.ts
 ┣ 📜app.module.ts
 ┗ 📜main.ts
 ┣ 📂test
📦.env
📦.gitignore
📦.eslintre.js
📦.prettierrc
📦.gitignore
📦.nest-cli,json
📦package-lock.json
📦package.json
📦README.md
📦tsconfig.build.json
📦tsconfig.json
```
---

##  내 역할
  - 카드 생성
  - 카드 조회
  - 카드 수정
  - 카드 순서 변경
  - 카드 삭제
  - 카드 작업자 할당
  - 카드 작업자 제거


## 주요 기능 및 설명

- **5. 카드**
  - 5-5-1 카드 생성
  - https://github.com/ysys29/p6.teamTrello/blob/cf4b883f2a7bdfaa41e134ff6e97f6415c9d5c28/src/card/card.service.ts#L23-L58
    ![카드생성](https://github.com/user-attachments/assets/8c1c753b-6878-4723-8dc8-b8c23fba989e)
  - 5-5-2 카드 조회
  - https://github.com/ysys29/p6.teamTrello/blob/cf4b883f2a7bdfaa41e134ff6e97f6415c9d5c28/src/card/card.service.ts#L60-L71
    ![카드상세조회](https://github.com/user-attachments/assets/10da11cb-5261-466b-a041-5f97d66552d3)
  - 5-5-3 카드 수정
  - https://github.com/ysys29/p6.teamTrello/blob/cf4b883f2a7bdfaa41e134ff6e97f6415c9d5c28/src/card/card.service.ts#L73-L95
    ![카드수정](https://github.com/user-attachments/assets/a93978de-6434-43ae-aa0f-a08f0bd5c0a0)
  - 5-5-4 카드 순서 변경
  - https://github.com/ysys29/p6.teamTrello/blob/cf4b883f2a7bdfaa41e134ff6e97f6415c9d5c28/src/card/card.service.ts#L108-L174
    ![카순변](https://github.com/user-attachments/assets/912ded06-c1a2-4af7-957a-3bed77531323)
  - 5-5-5 카드 삭제
  - https://github.com/ysys29/p6.teamTrello/blob/cf4b883f2a7bdfaa41e134ff6e97f6415c9d5c28/src/card/card.service.ts#L97-L106
    ![카드삭제](https://github.com/user-attachments/assets/7f000534-f519-4e6b-b0a9-53d8b5c83f88)
  - 5-5-6 카드 작업자 할당
  - https://github.com/ysys29/p6.teamTrello/blob/cf4b883f2a7bdfaa41e134ff6e97f6415c9d5c28/src/card/card.service.ts#L176-L197
    ![카드작업자할당](https://github.com/user-attachments/assets/8c5aa5aa-eb7d-4c33-a1ac-7a502e9d308c)
  - 5-5-7 카드 작업자 제거
  - https://github.com/ysys29/p6.teamTrello/blob/cf4b883f2a7bdfaa41e134ff6e97f6415c9d5c28/src/card/card.service.ts#L199-L213
    ![카드작업자삭제](https://github.com/user-attachments/assets/f330d0d8-2a26-4b4c-a604-2d43447467be)

## 트러블 슈팅
### 외래키 관련 오류
-![image (5)](https://github.com/user-attachments/assets/2c32426d-3ee1-4c34-bd01-d619bd718b00)
- 참조하는 컬럼에는 unsignd:true의 속성값이 있었지만, 참조받는 컬럼에는 아무 속성이 없었다.
- 양쪽 unsigned:true값을 삭제함으로써 에러를 해결할 수 있었다.


