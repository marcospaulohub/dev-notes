# ⏳ Async/Await no C#

## ✔ Exemplo básico
```csharp
public async Task<string> CarregarDados()
{
    await Task.Delay(1000);
    return "OK";
}
```
