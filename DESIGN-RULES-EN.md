Available languages: [Korean](DESIGN-RULES.md) [**English**](DESIGN-RULES-EN.md)

# Design rules
## Script
* The path of the script file must follow the class's namespace
  * The name of the script file must also follow the name of the class
* Just like Java, there can only be one class, interface, or enumeration declaration per script file.
  * Classes within classes do not have to follow this
* Fields must have private access modifiers under any circumstances.
* Fields are unconditionally encapsulated

## Naming convention
* If the class is an abstract class or is intended to be a base for some class, it must have 'Base' at the end of its name (e.g. SoundPlayerBase).
* Classes, structs, interfaces, enums, and methods must be Pascal case
  * Interfaces must always have an 'I' at the beginning of their name
* Fields, properties, events and constants must be camel case
  * Fields used in properties must be prefixed with '\_'.
* For constructors, the parameter name that initializes the field must be the same as the field name
* Don't use var type!
  * Can be used when code becomes too long

## Thread
* Use [Interlocked](https://docs.microsoft.com/ko-kr/dotnet/api/system.threading.interlocked) no matter what!

## Async
* Use [UniTask](https://github.com/Cysharp/UniTask) no matter what!
  * Do not use [UniTaskVoid](https://github.com/Cysharp/UniTask/blob/master/src/UniTask/Assets/Plugins/UniTask/Runtime/UniTaskVoid.cs)!
    * Exceptions are Unity event methods like Awake.
