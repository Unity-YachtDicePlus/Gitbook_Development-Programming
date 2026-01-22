---
layout:
  width: wide
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
  metadata:
    visible: true
---

# Page 1



<details>

<summary>public override void OnStartClient()</summary>

* **호출 시점**: 서버에서 Spawn된 NetworkObject가 클라이언트에 나타날 때
* **누가 실행?**: **모든 연결된 클라이언트**에서 실행됨
* **용도**: 클라이언트별 초기화 (UI 활성화, 카메라 설정 등)

</details>

<details>

<summary>SyncVar</summary>

* 서버에서 값을 바꾸면 모든 클라이언트에 자동으로 복사되는 변수
* 서버에서만 값을 변경할 수 있음. ServerRpc를 통해 요청할 수 있다.
* List, Dictionary 등의 복잡한 변수는 SyncVar X. 따로 SyncList, SyncDictionary 등이 존재

</details>

<details>

<summary>SyncVar(OnChange = nameof(특정 함수))</summary>

* SyncVar 변수 값이 바뀔 때 자동으로 '특정 함수'를 호출해주는 기능
* 만약 서버에서 SyncVar 값이 변경된다면 모든 클라이언트에서 '특정 함수'가 자동 호출된다.

</details>

<details>

<summary>ServerRpc</summary>

* 클라이언트에서 호출하면 서버에서 실행되는 함수
* 클라이언트에서 해당 함수를 호출하면 네트워크로 서버에 전달되고 실행됨.
* 클라이언트가 서버에 무언가를 요청할 때 사용
* 이름 규칙: 함수 이름 끝에 ServerRpc 추가

</details>

