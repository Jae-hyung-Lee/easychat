# Easy Chat

Easy chat 은 채팅 앱을 개발하기 위해 필요한 모든 기능을 제공합니다. 관리의 효율을 위해서 채팅 방은 Firestore 를 사용하고, 비용 절감을 위해서 채팅 메시지, 새로운 채팅 메시지 수 관리 등은 Realtime Database 를 사용합니다.

채팅 방 구독 및 푸시 알림, 아름다운 UI/UX 등 채팅 앱 개발에 필요한 모든 것을 제공합니다.


## 설치

## 초기화

```dart
ChatService.instance.init();
```


## 사용자 정보 연결

여러분들이 이미 개발한 앱에 본 패키지를 사용하는 경우, 회원 정보를 어디서 가져 올 것이지 정해주어야 합니다. 기본적으로 `users` 컬렉션을 사용하며, `displayName` 과 `photoUrl` 필드를 사용합니다. 만약 여러분의 앱이 `users` 컬렉션이 아닌 `members` 컬렉션에 사용자 정보를 저장한다면, `easyuser` 패키지를 설치하여 아래와 같이 

```dart
UserService.instance.init(
    collectionName: 'members',
);
ChatService.instance.init();
```

