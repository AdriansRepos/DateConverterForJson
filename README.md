## 🌐 Jazyk / Language Selection

*Klikněte na sekci níže pro zobrazení v češtině nebo angličtině.*
*Click on a section below to toggle between Czech and English.*

---

<details open>
<summary>🇨🇿 <strong>ČEŠTINA (Czech Version)</strong></summary>

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

</details>

---

<details>
<summary>🇺🇸 <strong>ENGLISH (English Version)</strong></summary>

# DateConverterForJson

A library for serializing and deserializing the `DateOnly` type in `System.Text.Json`, which does not support it by default.

## Usage

```csharp
using DateConverterForJson;

var options = new JsonSerializerOptions
{
    Converters = { new DateOnlyConverter() }
};

string json = JsonSerializer.Serialize(objekt, options);
```

Without this converter, System.Text.Json throws an exception during serialization and deserialization of properties of type DateOnly.

## Installation as a NuGet Package
This library is also available as a package in GitHub Packages. You can easily add it to your project:

1. Set up your GitHub as a package source (if you don't have it in NuGet.config yet).

2. In the Package Manager Console, run the command:
```powershell
Install-Package DateConverterForJson
```

</details>