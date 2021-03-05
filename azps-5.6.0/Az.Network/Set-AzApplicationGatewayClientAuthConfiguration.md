---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 79a602047327ef7723da360f0b89743a316d2ec3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964061"
---
# Set-AzApplicationGatewayClientAuthConfiguration

## SYNOPSIS
Modifica la configurazione dell'autenticazione client di un oggetto profilo SSL.

## SINTASSI

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzApplicationGatewayClientAuthConfiguration** modifica la configurazione di autenticazione client di un oggetto profilo SSL.

## ESEMPI

### Esempio 1
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw risorsa. Il secondo comando recupera il profilo SSL denominato SslProfile01 per $AppGw e archivia le impostazioni nella $profile variabile. L'ultimo comando modifica la configurazione dell'autenticazione client dell'oggetto profilo SSL archiviato in $profile.

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
Profilo SSL

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

### -VerifyClientCertIssuerDN
Verificare il nome dell'autorità di certificazione client.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzApplicationGatewayClientAuthConfiguration](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[New-AzApplicationGatewayClientAuthConfiguration](./New-AzApplicationGatewayClientAuthConfiguration.md)

[Get-AzApplicationGatewayClientAuthConfiguration](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[Remove-AzApplicationGatewayClientAuthConfiguration](./Remove-AzApplicationGatewayClientAuthConfiguration.md)