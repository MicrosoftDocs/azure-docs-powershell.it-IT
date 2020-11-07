---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 8ad5026f0e033c6ab5825c9c862b19ad51b40ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835072"
---
# Get-AzLogProfile

## Sinossi
Ottiene un profilo di log.

## SINTASSI

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzLogProfile** ottiene un profilo di log.

## ESEMPI

## PARAMETRI

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del profilo del log da ottenere.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection

## Note

## COLLEGAMENTI CORRELATI

[Add-AzLogProfile](./Add-AzLogProfile.md)

[Remove-AzLogProfile](./Remove-AzLogProfile.md)


