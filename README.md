### 1) Убедись, что иконка лежит здесь

```
Assets/icon.ico
```

### 2) В `.csproj` добавь ресурсы (если у тебя их ещё нет)

```xml
<ItemGroup>
  <AvaloniaResource Include="Assets/**" />
</ItemGroup>
```

### 3) В `App.axaml` задай иконку для всех `Window`

Открой `App.axaml` и добавь стиль:

```xml
<Application xmlns="https://github.com/avaloniaui"
             xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
             x:Class="MyApp.App">

  <Application.Styles>
    <FluentTheme />

    <!-- Иконка по умолчанию для ВСЕХ окон -->
    <Style Selector="Window">
      <Setter Property="Icon" Value="avares://MyApp/Assets/icon.ico"/>
    </Style>
  </Application.Styles>

</Application>
```
