---
title: "1장: 개발 환경 설정과 Hello World 작성하기"
tags:
  - dotnet
  - csharp
  - helloworld
  - basic
  - programming
  - begginer
---
# 1장: 개발 환경 설정 & 첫 번째 프로그램

## C# 소개

C#은 마이크로소프트에서 개발한 객체 지향 프로그래밍 언어로, 다양한 응용 프로그램을 만들 수 있는 강력한 기능을 제공합니다. 특히 .NET 플랫폼에서 실행되며, 웹, 데스크톱, 모바일, 게임 개발 등 다양한 분야에서 활용됩니다.

C#의 주요 특징은 다음과 같습니다.

- **객체 지향 프로그래밍(OOP) 지원**: 캡슐화, 상속, 다형성을 활용하여 효율적인 코드 작성 가능
- **간결하고 직관적인 문법**: Java 및 C++와 유사한 구조를 가지면서도 더 쉬운 문법 제공
- **강력한 라이브러리와 프레임워크 지원**: .NET 라이브러리를 활용하여 다양한 기능을 쉽게 구현 가능
- **다양한 플랫폼에서 실행 가능**: Windows, macOS, Linux 등에서 실행 가능

### 왜 C#을 배워야 할까요?

C#은 현대적인 프로그래밍 언어로, 배우기 쉽고 강력한 기능을 제공하여 다양한 개발 분야에서 활용됩니다. 다음과 같은 이유로 C#을 배우는 것이 유용합니다:

- **쉽고 직관적인 문법**: C++이나 Java와 유사한 문법을 가지면서도 코드가 간결하고 읽기 쉬움
- **강력한 개발 도구 지원**: Visual Studio 및 Visual Studio Code를 활용하여 생산성을 높일 수 있음
- **다양한 플랫폼 지원**: Windows, macOS, Linux 등 다양한 운영체제에서 실행 가능
- **다양한 활용 분야**: 웹 개발(ASP.NET), 데스크톱 애플리케이션, 모바일 앱(Xamarin), 게임(Unity) 등 여러 분야에서 사용 가능
- **마이크로소프트 및 기업의 적극적인 지원**: 지속적인 업데이트 및 개선이 이루어지는 신뢰할 수 있는 언어

C#을 배우면 다양한 프로젝트를 수행할 수 있는 기본적인 프로그래밍 능력을 갖출 수 있으며, 특히 .NET 생태계를 활용한 개발이 가능해집니다.

## C# 개발 환경 구축

C# 개발 환경은 일반적으로 Windows 운영체제에서 **Visual Studio** 라는 통합 개발 도구(이하 IDE)를 설치하여 구축합니다. 이는 원래 C#이 윈도우에서만 제대로 된 지원을 받는 언어라는 태생적 한계에 있습니다.

리눅스 생태계에서는 OmniSharp이라고 오픈소스가 있었지만 윈도우 외 운영체제에서는 라이벌 언어인 자바만큼은 활용적이지 않다가 시장의 시선이었습니다. 하지만 `dotnet core`가 출시된 이후부터는 모든 운영체제에서 제대로 된 C#을 개발을 할 수 있게 되었습니다.

IDE로 젯브레인 사에 Rider가 있지만, 이 문서에서는 **Visual Studio Code(VS Code)**를 이용하여 진행하도록 하겠습니다.

### 1. .NET SDK 설치
먼저 C#을 설치하기 위해서는 `.NET SDK`가 필요합니다. .NET SDK는 C# 프로그램을 컴파일하고 실행할 수 있도록 지원하는 개발 도구입니다.

#### Windows

1. Windows에서 `winget` 패키지 관리자를 사용하여 .NET SDK를 설치할 수 있습니다. 터미널(명령 프롬프트 또는 PowerShell)에서 다음 명령어를 입력하세요:
    
    ```
    winget install Microsoft.DotNet.SDK.9
    ```
    
2. 설치 후, 다음 명령어를 입력하여 정상적으로 설치되었는지 확인합니다:
    
    ```
    dotnet --version
    ```
    

#### macOS

4. 홈브루(Homebrew)가 설치되어 있다면, 터미널에서 다음 명령어를 입력하여 설치할 수 있습니다:
    
    ```
    brew install dotnet-sdk
    ```
    
    또는 [공식 다운로드 페이지](https://dotnet.microsoft.com/download)에서 설치 파일을 내려받아 수동으로 설치할 수 있습니다.
    
5. 설치 완료 후, 터미널에서 다음 명령어를 입력하여 정상 설치 여부를 확인합니다:
    
    ```
    dotnet --version
    ```
    

#### Linux

6. 배포판에 따라 다음과 같은 명령어를 사용하여 설치할 수 있습니다:
    
    - Ubuntu/Debian:
        
        ```
        sudo apt update
        sudo apt install dotnet-sdk-9.0
        ```
        
    - Fedora:
        
        ```
        sudo dnf install dotnet-sdk-8.0
        ```
        
    - Arch Linux:
        
        ```
        sudo pacman -S dotnet-sdk
        ```
        
7. 설치 완료 후, 다음 명령어로 확인합니다:
    
    ```
    dotnet --version
    ```
    

### 2. Visual Studio Code(VS Code) 설치 및 설정

**VS Code**는 가벼운 코드 편집기로, C# 개발을 지원하는 확장 기능을 설치하면 더욱 편리하게 사용할 수 있습니다.

#### 설치 방법 (모든 OS 공통)

8. [VS Code 공식 사이트](https://code.visualstudio.com/)에서 설치 파일을 다운로드합니다.
    
9. 설치 후, 실행하여 **Extensions(확장 프로그램)** 탭에서 `C#` 확장을 검색하고 설치합니다.
    
10. 터미널에서 다음 명령어를 입력하여 올바르게 설치되었는지 확인합니다:
    
    ```
    code --version
    ```
    

## 첫 번째 프로그램: "Hello, World!" 출력

개발 환경이 정상적으로 구축되었는지 확인하기 위해 간단한 C# 프로그램을 작성해 보겠습니다.

### 프로젝트 생성

11. 터미널을 열고 원하는 폴더에서 다음 명령어를 입력하여 새 C# 콘솔 애플리케이션을 생성합니다:
    
    ```
    dotnet new console -o HelloWorld
    ```
    
12. 생성된 폴더로 이동합니다:
    
    ```
    cd HelloWorld
    ```
    
13. `Program.cs` 파일을 열어 기본 코드 구조를 확인합니다.
    

### 코드 작성

`Program.cs` 파일을 열어 다음과 같이 수정합니다:

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, World!");
    }
}
```

### 프로그램 실행

터미널에서 다음 명령어를 실행하여 프로그램을 실행해 봅니다:

```
dotnet run
```

출력 결과:

```
Hello, World!
```

이제 C# 개발 환경을 성공적으로 설정하고 첫 번째 프로그램을 실행했습니다! 다음 장에서는 보다 실용적인 프로그램을 만들어 보겠습니다.