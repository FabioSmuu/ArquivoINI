# Gerenciamento IO de arquivos INI
Este código se trata de uma simples class em C# para a manipulação de arauivos.ini

Confira o arquivos [ArquivoINI.cs](/ArquivoINI.cs).

### Para colocar em seu projeto C#, segue o exemplo:
```cs
try
{
    var config = new ArquivoINI("config.ini");
    if (File.Exists("config.ini"))
    {
        boleano = Convert.ToBoolean(config.Ler("boleano", "Config"));
        numerico = Convert.ToInt32(config.Ler("numerico", "Config"));
        normal = config.Ler("normal", "Config");
    }

    else
    {
        config.Escrever("boleano", "true", "Config");
        config.Escrever("numerico", "13", "Config");
        config.Escrever("normal", "Esta é uma string", "Config");
    }

}
catch (Exception e)
{
    Console.ForegroundColor = ConsoleColor.Red;
    Console.Write("\r[Erro] ");
    Console.ForegroundColor = ConsoleColor.DarkRed;
    Console.WriteLine(e.Message);
}
```

**Obrigado pela sua atenção!**
