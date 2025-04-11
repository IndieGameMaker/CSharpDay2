# C# 문법 특강 - if / switch

## Boolean 타입과 if문

```csharp
// Boolean 타입 - true 또는 false 값만 가질 수 있다.
bool isGameActive = true;
bool hasKey = false;

// 기본 if문 구조
if (isGameActive)
{
    // 이 코드 블록은 isGameActive가 true일 때만 실행
    Console.WriteLine("게임이 실행 중입니다.");
}

// 중괄호 {} 없는 if문 (한 줄만 실행할 경우)
if (hasKey)
    Console.WriteLine("열쇠를 가지고 있습니다."); // 한 줄만 if문에 포함됨

```