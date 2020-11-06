---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: 6591250c903b3f51ccbbd567e290f9d83fab983a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508475"
---
# Stop-AzureRmWebApp

## Sinossi
Interrompe un'app Web Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### S1
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S2
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Stop-AzureRmWebApp** interrompe un'app Web di Azure.

## ESEMPI

### Esempio 1: arrestare un'app Web
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

Questo comando interrompe l'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.

## PARAMETRI

### -Nome
Nome Web App

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome gruppo risorse

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Web App
Oggetto Web App

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Sito
Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)

[New-AzureRmWebApp](./New-AzureRmWebApp.md)

[Remove-AzureRmWebApp](./Remove-AzureRmWebApp.md)

[Riavviare-AzureRmWebApp](./Restart-AzureRmWebApp.md)

[Start-AzureRmWebApp](./Start-AzureRmWebApp.md)


