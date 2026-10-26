# DateConverterForJson

Knihovna pro serializaci a deserializaci typu `DateOnly` v `System.Text.Json`, který ho ve výchozím stavu nepodporuje.

## Použití

```csharp
using DateConverterForJson;

var options = new JsonSerializerOptions
{
    Converters = { new DateOnlyConverter() }
};

string json = JsonSerializer.Serialize(objekt, options);
```

Bez tohoto konvertoru `System.Text.Json` u vlastností typu `DateOnly` vyhazuje výjimku při serializaci i deserializaci.

## Instalace jako NuGet balíček

Tato knihovna je dostupná také jako balíček v **GitHub Packages**. Můžete si ji snadno přidat do svého projektu:

1. Nastavte si jako zdroj balíčků váš GitHub (pokud ho ještě nemáte v NuGet.config).
2. V **Package Manager Console** spusťte příkaz:
   ```powershell
   Install-Package DateConverterForJson
   ```
