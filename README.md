# C# 문법 특강 - if / switch

## if문
### 개요
- 프로그래밍에서 가장 많이 사용되는 제어문 중 하나입니다.
- 조건문을 사용하여 특정 조건에 따라 코드 블록을 실행하는 제어문입니다.
- 조건식이 true일 경우에만 실행됩니다.

### if 문 기본
#### 문법
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

#### 예제

```csharp
// Boolean 타입 - true 또는 false 값만 가질 수 있다.
bool isGameOver = false;

if (isGameOver)
{
    // 게임이 종료된 경우
    Console.WriteLine("게임이 종료되었습니다.");
}
```

```csharp
bool hasKey = false;

// 중괄호 {} 없는 if문 (한 줄만 실행할 경우)
if (hasKey == true)
    Console.WriteLine("열쇠를 가지고 있습니다."); // 한 줄만 if문에 포함됨
```

```csharp
bool isPlayerDead = false;

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
#### 문법
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

#### 예제

```csharp
bool isGameOver = false;

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
```

```csharp
bool hasKey = false;

// 중괄호 {} 없는 if-else문 (한 줄만 실행할 경우)
if (hasKey)
    Console.WriteLine("열쇠를 가지고 있습니다."); // 한 줄만 if문에 포함됨
else
    Console.WriteLine("열쇠가 없습니다."); // 한 줄만 else문에 포함됨
```

### if-else if-else 문
#### 문법
```csharp
if (조건식1)
{
    // 조건식1이 참일 때 실행되는 구문
}
else if (조건식2)
{
    // 조건식2가 참일 때 실행되는 구문
}
else
{
    // 모든 조건식이 거짓일 때 실행되는 구문
}
```

#### 예제

```csharp
int playerLevel = 5;

if (playerLevel < 10)
{
    Console.WriteLine("쪼렙");
}
else if (playerLevel < 20)
{
    Console.WriteLine("중수");
}
else
{
    Console.WriteLine("고인물");
}  
```

### 연산자

#### 비교 연산자

- == (같다) : 두 값이 같을 때 true
- &lt; (크다) : 왼쪽 값이 오른쪽 값보다 클 때 true
- < (작다) : 왼쪽 값이 오른쪽 값보다 작을 때 true
- &lt;= (크거나 같다) : 왼쪽 값이 오른쪽 값보다 크거나 같을 때 true
- <= (작거나 같다) : 왼쪽 값이 오른쪽 값보다 작거나 같을 때 true
- != (같지 않다) : 두 값이 다를 때 true
    
#### 논리 연산자
- && (AND) : 두 조건이 모두 true일 때 true
- || (OR) : 두 조건 중 하나라도 true일 때 true
- ! (NOT) : 조건이 false일 때 true

#### 삼항 연산자