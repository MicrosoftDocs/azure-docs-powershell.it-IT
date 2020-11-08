---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029833"
---
# Get-AzureAutomationAccount

## Sinossi

Ottiene gli account di automazione Azure.

## SINTASSI

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Il cmdlet **Get-AzureAutomationAccount** ottiene gli account di automazione di Microsoft Azure per l'abbonamento.
Un account di automazione è un contenitore per le risorse di automazione che viene isolato dalle risorse di altri account di automazione.
Le risorse di automazione includono manuali operativi, Jobs e asset.

## ESEMPI

### Esempio 1: ottenere un account di automazione
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

Questo comando consente di ottenere l'account di automazione denominato Contoso17.

## PARAMETRI

### -Posizione
Specifica una posizione di Azure associata agli account di automazione.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome di un account di automazione di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

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

## OUTPUT

### Microsoft. Azure. Commands. Automation. Model. AutomationAccount

## Note

## COLLEGAMENTI CORRELATI

[New-AzureAutomationAccount](./New-AzureAutomationAccount.md)

[Remove-AzureAutomationAccount](./Remove-AzureAutomationAccount.md)


