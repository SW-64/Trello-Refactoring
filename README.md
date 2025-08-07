# 🖥️ NestJs Trello Project (팀 협업 개발도구 만들기) 

![thumbnail](https://github.com/user-attachments/assets/974904ff-6aa1-4c4e-bcfa-350b3bdb383b)

## 목차 
- 프로젝트 소개 
- 팀원 구성
- 개발 기간
- 개발 환경
- ERD 및 와이어 프레임
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
### 2024.07.11 ~ 2024.07.17
--- 
##  개발 환경
- 운영체제 : Window/Mac
- BackEnd : TypeScript, NestJs, MySQL(TypeORM)
- Tool : Visual Studio Code, Insomnia, DBeaver, Swagger

---
## ERD  및 와이어 프레임


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


## SSE

코드 흐름

1.  클라이언트(유저 ID 5)가 **/sse/5**에 연결 = **sendClientAlarm(5) 호출**
2.  어떤 카드가 유저 ID 5에게 할당 = **emitCardChangeEvent(5) 실행**

```
  private users$: Subject<any> = new Subject();
  private observer = this.users$.asObservable();

  // 이벤트 발생 함수
  emitCardChangeEvent(userId: number) {
    this.users$.next({ id: userId });
  }

  // 이벤트 연결
  sendClientAlarm(userId: number): Observable<any> {
    return this.observer.pipe(
      filter((user) => user.id === userId),
      map(() => {
        return {
          data: {
            message: '카드의 담당자가 사용자님으로 변경되었습니다.',
          },
        } as MessageEvent;
      }),
    );
  }
```

3.  내부 Subject에서 이벤트 발생 → .pipe() 내부 로직 실행
4.  해당 유저에게 **message: 카드의 담당자가 사용자님으로 변경되었습니다** 가 SSE로 전달
  
  
  
          


<br />

### 여기서 왜 emitCardChangeEvent 함수를 실행하게되면 sendClientAlarm 함수가 실행될까?
<br />

1. Subject.next = <u>이벤트를 발생시킴</u>

2. observer.pipe = <u>이벤트를 듣고 필터링 및 가공해서 구독자에게 전달</u>

<br />

**즉, Subject가 이벤트를 발생시키면 Observer는 이벤트를 듣는다.**

**Observer를 통해 읽기만 가능하게 ( 읽기 전용 권한 ) 을 주는 설계**

<br />
<br />

### 왜 WebSocket이 아닌 SSE?

구현하는 목적은 단순 알람을 전달하기 위함이다.
<br /> 이 말은 즉, 단방향 통신으로도 가능하다는 얘기다.
<br /> 또한, SSE는 WebSocket보다 가볍고 단순하기 때문에 네트워크 부하도 낮다.



---
## LexoRank

### LexoRank란?
<br />

문자열 기반 정렬 알고리즘
<br />사전식 순서를 사용하여 항목 간 정렬을 유연하게 처리
<br />중간 삽입 시에도 전체 순위값 갱신 없이, O(1)로 정렬 유지 가능



### 왜 사용?

<br /> 다음 3가지의 방식은 각각 한계를 갖고있음
<br />


Integer 방식 : 	순서 변경 시 여러 항목의 순위값 수정 필요 → O(N)
<br /> GreenHopper 방식	: 순위값 간격 고갈 시 전체 재정렬 필요 → 시스템 중단 발생 가능
<br /> Linked List 방식	: 연결 정보 유지 비용 & 조회 성능 저하

순위값 수정, 순위값 고갈 시 재정렬, 조회 성능
<br /> 이 3가지의 성능을 좋게 갖춘 방법이
**lexoRank**

<br />

### LexoRank의 구성 요소

Bucket	= 순위 고갈 시, 무중단 재정렬을 위한 공간 분리 
<br />FixedKey =	기본적인 순서 결정 키 (고정 길이)
<br />VariableKey =	FixedKey가 고갈됐을 때 사용하는 가변 키 (길이 확장 가능)
<br />



### 코드 내부


<img width="759" height="350" alt="Image" src="https://github.com/user-attachments/assets/a841e88c-ccfe-4301-a7ec-619346686cb9" />

<img width="758" height="357" alt="Image" src="https://github.com/user-attachments/assets/e8528f30-31f9-4390-93f3-b4a26a237428" />

<img width="759" height="371" alt="Image" src="https://github.com/user-attachments/assets/729304e5-47bc-403c-961b-446582b788e1" />




### 정리
LexoRank는 드래그 앤드 드롭 기반 정렬에서, 빠르고 안정적으로 순서를 유지하면서도 시스템 중단 없이 유연하게 대응할 수 있는 뛰어난 정렬 알고리즘
<br /> LINE 내부에서는 실제 라이브러리로 구현










