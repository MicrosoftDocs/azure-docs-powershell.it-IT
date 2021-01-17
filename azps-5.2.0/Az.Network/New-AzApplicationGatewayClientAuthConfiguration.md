---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 6e8c3cdbfa1242cba19d3aa3250c4bf4e381ae92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347452"
---
# New-AzApplicationGatewayClientAuthConfiguration

## Sinossi
Crea una nuova configurazione di autenticazione client per il profilo SSL.

## SINTASSI

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzApplicationGatewayClientAuthConfiguration** crea una nuova configurazione di autenticazione client per il profilo SSL.

## ESEMPI

### Esempio 1
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

Il comando crea una nuova configurazione di autenticazione client e la archivia in $clientAuthConfig variabile da usare in un profilo SSL. 

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -VerifyClientCertIssuerDN
Verificare il nome dell'autorità di certificazione del certificato client.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayClientAuthConfiguration

## Note

## COLLEGAMENTI CORRELATI

[Add-AzApplicationGatewayClientAuthConfiguration](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[Get-AzApplicationGatewayClientAuthConfiguration](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[Remove-AzApplicationGatewayClientAuthConfiguration](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[Set-AzApplicationGatewayClientAuthConfiguration](./Set-AzApplicationGatewayClientAuthConfiguration.md)