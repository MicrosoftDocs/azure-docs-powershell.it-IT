---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 49d55a48f9e9b769854a5cd01929188fd7993d35
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415564"
---
# Get-AzApplicationGatewaySslProfilePolicy

## SYNOPSIS
Ottiene i criteri SSL di un profilo SSL del gateway applicazione.

## SINTASSI

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzApplicationGatewaySslProfilePolicy** ottiene il criterio SSL di un profilo SSL del gateway di applicazione.

## ESEMPI

### Esempio 1
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile. Il secondo comando recupera il profilo SSL denominato SslProfile01 per $AppGw e lo archivia $SslProfile variabile. L'ultimo comando recupera il criterio SSL dal profilo SSL $SslProfile e lo archivia nella $sslpolicy variabile.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslProfile
Profilo SSL del Gateway applicazione

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy

## NOTE

## COLLEGAMENTI CORRELATI



[Remove-AzApplicationGatewaySslProfilePolicy](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[Set-AzApplicationGatewaySslProfilePolicy](./Set-AzApplicationGatewaySslProfilePolicy.md)
