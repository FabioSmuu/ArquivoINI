# Repositorio de criação da config.ini

[![N|Solid](https://cdn.discordapp.com/attachments/631607183301148672/724397007170568313/paypal.png)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=fabinhoec2210@gmail.com&item_name=F%C3%A1bio&currency_code=BRL)  [![N|Solid](https://cdn.discordapp.com/attachments/631607183301148672/724397005543178270/picpay.png)](https://app.picpay.com/user/smuu)

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
