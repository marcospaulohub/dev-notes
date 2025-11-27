# 🧩 Design Patterns em C#

## ✔ Singleton
```csharp
public sealed class Logger
{
    private static readonly Logger instance = new();
    public static Logger Instance => instance;
}
```
