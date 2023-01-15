사용할 수 있는 언어: [**한국어**](DESIGN-RULES.md) [영어](DESIGN-RULES-EN.md)

# 디자인 규칙
## 스크립트
* 스크립트 파일의 경로는 클래스의 네임스페이스를 따라가야 합니다
  * 스크립트 파일의 이름 또한 클래스의 이름을 따라가야 합니다
* 자바처럼 스크립트 파일 하나에 클래스 또는 인터페이스, 열거 선언은 하나만 있어야 합니다
  * 클래스 안의 클래스의 경우는 이를 따르지 않아도 됩니다
* 필드는 어떤 상황에서도 접근 제한자는 private 이어야 합니다

## 명명 규칙
* 클래스가 추상 클래스이거나 어떠한 클래스의 기반이 되게 만든 거라면 이름 맨 뒤에 'Base'가 붙어야 합니다 (예: SoundPlayerBase)
* 클래스, 구조체, 인터페이스, 열거, 메소드는 파스칼 케이스여야 합니다
  * 인터페이스는 항상 이름 맨 앞에 'I'가 붙어있어야 합니다
* 필드, 프로퍼티, 이벤트, 상수는 카멜 케이스여야 합니다
  * 프로퍼티에서 사용하는 필드의 경우에는 맨 앞에 '\_'가 붙어있어야 합니다
* 생성자의 경우 필드를 초기화하는 매개변수 이름은 필드 이름과 같아야 합니다
* var 타입 사용 금지!
  * 코드가 너무 길어질 때는 사용 가능

## 스레드
* 무슨 일이 있던 [Interlocked](https://docs.microsoft.com/ko-kr/dotnet/api/system.threading.interlocked) 사용하기!

## 비동기
* 무슨 일이 있든 [UniTask](https://github.com/Cysharp/UniTask) 사용하기!
  * [UniTaskVoid](https://github.com/Cysharp/UniTask/blob/master/src/UniTask/Assets/Plugins/UniTask/Runtime/UniTaskVoid.cs) 사용 금지!
