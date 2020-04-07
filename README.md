# Repositorio de criação da config.ini

[![N|Solid](https://i.imgur.com/mF9AKO0.png)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=fabinhoec2210@gmail.com&item_name=F%C3%A1bio&currency_code=BRL)

Com esta class é possivel criar arquivos muito usado em configurações de softwares.

Confia o arquivos [ArquivoINI.cs](/ArquivoINI.cs) para entender melhor.

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
