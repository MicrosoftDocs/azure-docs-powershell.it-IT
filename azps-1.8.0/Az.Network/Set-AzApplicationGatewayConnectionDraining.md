---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 042eb9bdff35cb406a879b454b3b78451a89d789
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401760"
---
# Set-AzApplicationGatewayConnectionDraining

## SYNOPSIS
Modifica la configurazione di escolo della connessione di un oggetto impostazioni HTTP back-end.

## SINTASSI

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** modifica la configurazione di esente della connessione di un oggetto impostazioni HTTP back-end.

## ESEMPI

### Esempio 1
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.
Il secondo comando recupera le impostazioni HTTP di back-end denominate Settings01 per $AppGw e archivia le impostazioni nella variabile $Settings back-end.
L'ultimo comando modifica la configurazione di escolo della connessione dell'oggetto impostazioni HTTP back-end archiviato in $Settings impostando Enabled su False e DrainTimeoutInSec su 3600.

## PARAMETERS

### -BackendHttpSettings
Impostazioni http back-end

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -DrainTimeoutInSec
Il numero di secondi per cui è attivo lo scaricamento della connessione.
I valori accettabili sono da 1 secondo a 3600 secondi.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enabled
Se lo scaricamento delle connessioni è abilitato o meno.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)


[Get-AzApplicationGatewayConnectionDraining](./Get-AzApplicationGatewayConnectionDraining.md)

[New-AzApplicationGatewayConnectionDraining](./New-AzApplicationGatewayConnectionDraining.md)

[Remove-AzApplicationGatewayConnectionDraining](./Remove-AzApplicationGatewayConnectionDraining.md)

