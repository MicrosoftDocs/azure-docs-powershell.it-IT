---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 6f93a66739fe1943182726e6998267d1e406f0a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853805"
---
# Get-AzApplicationGatewaySslPolicy

## Sinossi
Ottiene i criteri SSL di un gateway dell'applicazione.

## SINTASSI

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzApplicationGatewaySslPolicy** ottiene i criteri SSL di un gateway dell'applicazione.

## ESEMPI

### 1:
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.
Il secondo comando consente di ottenere i criteri SSL dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.

## PARAMETRI

### -ApplicationGateway
Specifica il gateway dell'applicazione dei criteri SSL ottenuti da questo cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy

## Note
* Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking

## COLLEGAMENTI CORRELATI

[New-AzApplicationGatewaySslPolicy](./New-AzApplicationGatewaySslPolicy.md)

[Set-AzApplicationGatewaySslPolicy](./Set-AzApplicationGatewaySslPolicy.md)


