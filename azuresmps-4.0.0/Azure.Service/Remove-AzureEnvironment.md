---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029939"
---
# Remove-AzureEnvironment

## Sinossi
Elimina un ambiente Azure da Windows PowerShell.

## SINTASSI

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureEnvironment** Elimina un ambiente Azure dal profilo comune in modo che Windows PowerShell non riesca a trovarlo.
Questo cmdlet non elimina l'ambiente da Microsoft Azure o modifica l'ambiente effettivo in alcun modo.

Un ambiente Azure una distribuzione indipendente di Microsoft Azure, ad esempio AzureCloud per Azure globale e AzureChinaCloud per Azure gestito da 21Vianet in Cina.
Puoi anche creare ambienti Azure locali usando Azure Pack e i cmdlet WAPack.
Per altre informazioni, vedere [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

## ESEMPI

### Esempio 1: eliminare un ambiente
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

Questo comando Elimina l'ambiente ContosoEnv da Windows PowerShell.

### Esempio 2: eliminare più ambienti
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

Questo comando Elimina gli ambienti i cui nomi iniziano con "contoso" da Windows PowerShell.

## PARAMETRI

### -Force
Elimina la richiesta di conferma.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome dell'ambiente da rimuovere.
Questo parametro è obbligatorio.
Questo valore di parametro fa distinzione tra maiuscole e minuscole.
I caratteri jolly non sono consentiti.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet. Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.

## OUTPUT

### None o System. Boolean
Se si usa il parametro *PassThru* , questo cmdlet restituisce un valore booleano.
In caso contrario, non restituirà alcun output.

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


