# C# 문법 특강 - if / switch

## if문
### 개요
- 프로그래밍에서 가장 많이 사용되는 제어문 중 하나입니다.
- 조건문을 사용하여 특정 조건에 따라 코드 블록을 실행하는 제어문입니다.
- 조건식이 true일 경우에만 실행됩니다.

### if 문 기본

```csharp
if (조건식)
{
    // 조건식이 참일 때 실행되는 구문
}
```

#### BSD 스타일 (Allman 스타일)
```csharp
if (조건식)
{
    // 조건식이 참일 때 실행되는 구문
}
else
{
    // 조건식이 거짓일 때 실행되는 구문
}
```
#### K&R 스타일 (Inline 스타일)
```csharp
if (조건식) {
    // 조건식이 참일 때 실행되는 구문
} else {
    // 조건식이 거짓일 때 실행되는 구문
}
```

### 예제

```csharp
// Boolean 타입 - true 또는 false 값만 가질 수 있다.
bool isGameOver = false;
bool hasKey = false;
bool isPlayerDead = false;

if (isGameOver)
{
    // 게임이 종료된 경우
    Console.WriteLine("게임이 종료되었습니다.");
}

// 중괄호 {} 없는 if문 (한 줄만 실행할 경우)
if (hasKey == true)
    Console.WriteLine("열쇠를 가지고 있습니다."); // 한 줄만 if문에 포함됨

if (isPlayerDead == false)
{
    Console.WriteLine("플레이어가 살아있습니다.");
}

if (!isPlayerDead)
{
    Console.WriteLine("플레이어가 살아있습니다.");
}
```

### if-else 문

```csharp
if (조건식)
{
    // 조건식이 참일 때 실행되는 구문
}
else
{
    // 조건식이 거짓일 때 실행되는 구문
}
```

### 예제

```csharp
bool isGameOver = false;
bool hasKey = false;

if (isGameOver)
{
    // 게임이 종료된 경우
    Console.WriteLine("게임이 종료되었습니다.");
}
else
{
    // 게임이 종료되지 않은 경우
    Console.WriteLine("게임이 진행 중입니다.");
}

// 중괄호 {} 없는 if-else문 (한 줄만 실행할 경우)
if (hasKey)
    Console.WriteLine("열쇠를 가지고 있습니다."); // 한 줄만 if문에 포함됨
else
    Console.WriteLine("열쇠가 없습니다."); // 한 줄만 else문에 포함됨
```
