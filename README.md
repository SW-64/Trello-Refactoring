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
### 2024.07.11 ~ 2024.07.17
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
### 정리
LexoRank는 드래그 앤드 드롭 기반 정렬에서, 빠르고 안정적으로 순서를 유지하면서도 시스템 중단 없이 유연하게 대응할 수 있는 뛰어난 정렬 알고리즘
<br /> LINE 내부에서는 실제 라이브러리로 구현



### 코드 내부


#### 카드가 빈 리스트로 이동 시
```
// 이동할 아이템에 새로 할당할 lexoRank 정의
      let lexoRank: LexoRank;
// 카드가 빈 리스트로 이동할때
      const existedCard = await queryRunner.manager.findOneBy(Card, { listId: listId });
      if (!beforeId && !afterId && !existedCard) {
        lexoRank = LexoRank.middle();
        await queryRunner.manager.update(Card, cardId, {
          listId: listId,
          lexoRank: lexoRank.toString(),
        });
        await queryRunner.commitTransaction(); // 트랜잭션 커밋
        return true;
      }
```
#### 카드가 다른 리스트로 이동 시
```
// 이동할 위치에 따른 LexoRank값 할당
      // 1. 맨 처음-> 첫번째 위치한 카드의 LexoRank값에서 genPrev()를 이용해 더 작은 LexoRank값을 할당
      if (!beforeCard) lexoRank = afterCardLexoRank.genPrev();
      // 2. 맨 끝  -> 마지막에 위치한 카드의 LexoRank값에서 genNext()를 이용해 더 큰 LexoRank값을 할당
      else if (!afterCard) lexoRank = beforeCardLexoRank.genNext();
      // 3. 두 카드 사이 ->  between()을 이용해서 두 카드의 LexoRank값들의 사이값인 LexoRank값을 할당
      else lexoRank = beforeCardLexoRank.between(afterCardLexoRank);

      // 선택한 리스트와 변경된 lexoRank값 update하기
      const updateResult = await queryRunner.manager.update(Card, cardId, {
        listId: listId,
        lexoRank: lexoRank.toString(),
      });
```

전체 코드
```
// 이동할 아이템에 새로 할당할 lexoRank 정의
      let lexoRank: LexoRank;

      // 해당 리스트가 없을때 false 반환
      const existedList = await queryRunner.manager.findOneBy(List, { id: listId });
      if (!existedList) throw new NotFoundException('해당 리스트가 없습니다.');

      // 카드가 빈 리스트로 이동할때
      const existedCard = await queryRunner.manager.findOneBy(Card, { listId: listId });
      if (!beforeId && !afterId && !existedCard) {
        lexoRank = LexoRank.middle();
        await queryRunner.manager.update(Card, cardId, {
          listId: listId,
          lexoRank: lexoRank.toString(),
        });
        await queryRunner.commitTransaction(); // 트랜잭션 커밋
        return true;
      }
      // beforeId, afterId 중 최소 1개는 있어야 한다. 둘 다 없다면 false 반환
      // beforecard가 Null 이라면 첫번재 순서
      // aftercard가 Null 이라면 마지막 순서
      else if (!beforeId && !afterId) throw new NotFoundException('beforeId, afterId 중 1개를 입력해주세요');

      // Id값으로 이동 했을때 전과 후의 카드 찾기
      const beforeCard = beforeId ? await queryRunner.manager.findOneBy(Card, { id: beforeId }) : null; // ex) 6번 리스트를 2번과 3번 사이로 이동시킨다면 2번 리스트
      const afterCard = afterId ? await queryRunner.manager.findOneBy(Card, { id: afterId }) : null; // ex) 6번 리스트를 2번과 3번 사이로 이동시킨다면 3번 리스트

      // 해당 리스트 안에, 해당 카드가 없다면 false 반환
      // beforeId 혹은 afterId가 Null값을 줄 수 있는 경우를 제외해야한다.
      // 의도적으로 Null값을 줄 수는 있지만, 리스트 id에 맞게 찾았을때 카드가 null값이 나오면 안된다.
      if (afterId != null || beforeId != null) {
        const existedBeforeCard = beforeId
          ? await queryRunner.manager.findOneBy(Card, { id: beforeId, listId: listId })
          : null;
        const existedAfterCard = afterId
          ? await queryRunner.manager.findOneBy(Card, { id: afterId, listId: listId })
          : null;
        if ((beforeId && !existedBeforeCard) || (afterId && !existedAfterCard))
          throw new NotFoundException('해당 리스트에 해당 카드가 없습니다.');
      }

      // 이전과 이후 카드의 lexoRank 값
      const beforeCardLexoRank = beforeCard ? LexoRank.parse(beforeCard.lexoRank) : null;
      const afterCardLexoRank = afterCard ? LexoRank.parse(afterCard.lexoRank) : null;

      // 유효성 검사 끝

      // 카드 변경 로직

      // 이동할 위치에 따른 LexoRank값 할당
      // 1. 맨 처음-> 첫번째 위치한 카드의 LexoRank값에서 genPrev()를 이용해 더 작은 LexoRank값을 할당
      if (!beforeCard) lexoRank = afterCardLexoRank.genPrev();
      // 2. 맨 끝  -> 마지막에 위치한 카드의 LexoRank값에서 genNext()를 이용해 더 큰 LexoRank값을 할당
      else if (!afterCard) lexoRank = beforeCardLexoRank.genNext();
      // 3. 두 카드 사이 ->  between()을 이용해서 두 카드의 LexoRank값들의 사이값인 LexoRank값을 할당
      else lexoRank = beforeCardLexoRank.between(afterCardLexoRank);

      // 선택한 리스트와 변경된 lexoRank값 update하기
      const updateResult = await queryRunner.manager.update(Card, cardId, {
        listId: listId,
        lexoRank: lexoRank.toString(),
      });
      console.log(updateResult);
      if (updateResult.affected === 0) {
        throw new Error('카드 업데이트에 실패했습니다.');
      }

      // console.log('updateResult', updateResult);
      await queryRunner.commitTransaction(); // 트랜잭션 커밋

      // 업데이트된 카드 정보 반환
      const updatedCard = await this.cardRepository.findOne({ where: { id: cardId } });
      if (!updatedCard) {
        throw new NotFoundException('업데이트 된 카드를 찾을 수 없습니다.');
      }
      console.log(updatedCard);
      // await queryRunner.manager.save(updateResult);
      // return updatedCard;
      return true;
      // await this.findAll();
    } catch (e) {
      await queryRunner.rollbackTransaction();
      throw e;
    } finally {
      await queryRunner.release();
    }
```















