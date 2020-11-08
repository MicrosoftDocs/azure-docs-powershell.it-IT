---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: 736e9abe12b00420a4d494510f2cd0d737ae3e02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202279"
---
# Reset-AzP2sVpnGateway

## Sinossi
Reimposta il gateway VPN P2S scalabile.

## SINTASSI

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByP2SVpnGatewayName (impostazione predefinita)
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByP2SVpnGatewayObject
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByP2SVpnGatewayResourceId
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Reimposta il P2SVpnGateway

## ESEMPI

### Esempio 1:
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## PARAMETRI

### -AsJob
Esegui cmdlet in background

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -P2SVpnGateway
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway

## Note

## COLLEGAMENTI CORRELATI

[Get-AzP2sVpnGateway](./Get-AzP2sVpnGateway.md)

[New-AzP2sVpnGateway](./New-AzP2sVpnGateway.md)

[Remove-AzP2sVpnGateway](./Remove-AzP2sVpnGateway.md)

[Update-AzP2sVpnGateway](./Update-AzP2sVpnGateway.md)
