---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 1399dba141cb885e0ad184a588707e7c4f4efe7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997245"
---
# New-AzApplicationGatewayHttpListener

## SYNOPSIS
Crea un listener HTTP per un gateway applicazione.

## SINTASSI

### SetByResourceId
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzApplicationGatewayHttpHttpHttp Listener crea** un listener HTTP per un gateway applicazione di Azure.

## ESEMPI

### Esempio 1: Creare un listener HTTP
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

Questo comando crea un listener HTTP denominato Listener01 e archivia il risultato nella variabile $Listener.

### Esempio 2: Creare un listener HTTP con SSL
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

Questo comando crea un listener HTTP che usa l'offload SSL e fornisce il certificato SSL nella variabile $SSLCert 01.
Il comando archivia il risultato nella variabile denominata $Listener.

### Esempio 3: Creare un listener HTTP con criteri firewall
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

Questo comando crea un listener HTTP denominato Listener01, FirewallPolicy $firewallPolicy e archivia il risultato nella variabile $Listener.

### Esempio 4: Aggiungere un listener HTTPS con SSL e HostNames
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

Questo comando crea un listener HTTP che usa l'offload SSL e fornisce il certificato SSL nella variabile $SSLCert 01 insieme a due HostNames.
Il comando archivia il risultato nella variabile denominata $Listener.

## PARAMETERS

### -CustomErrorConfiguration
Errore del cliente di un gateway applicazioni

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -FirewallPolicy
Specifica il riferimento all'oggetto a un criterio firewall di primo livello. Il riferimento all'oggetto può essere creato usando New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.
$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Un criterio firewall creato con il commandlet riportato sopra può essere indicato a livello di regola del percorso. Il comando precedente crea impostazioni dei criteri predefinite e regole gestite.
Invece dei valori predefiniti, gli utenti possono specificare PolicySettings e ManagedRules usando rispettivamente New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules predefiniti.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyId
Specifica l'ID di una risorsa firewall dell'applicazione Web di primo livello esistente.
Gli ID dei criteri del firewall possono essere restituiti usando il cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy firewall. Una volta fornito l'ID, è possibile usare il *parametro FirewallPolicyId* invece del *parametro FirewallPolicy.*
Ad esempio: -FirewallPolicyId /subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendIPConfiguration
Specifica l'oggetto di configurazione IP front-end per il listener HTTP.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendIPConfigurationId
Specifica l'ID della configurazione IP front-end per il listener HTTP.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPort
Specifica la porta front-end per il listener HTTP.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPortId
Specifica l'ID dell'oggetto porta front-end per il listener HTTP.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostName
Specifica il nome host del listener HTTP del gateway applicazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostNames
Nomi host

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifica il nome del listener HTTP creato dal cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Specifica il protocollo utilizzato dal listener HTTP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireServerNameIndication
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCertificate
Specifica l'oggetto certificato SSL per il listener HTTP.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCertificateId
Specifica l'ID del certificato SSL per il listener HTTP.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslProfile
SslProfile

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslProfileId
SslProfileId

```yaml
Type: System.String
Parameter Sets: SetByResourceId
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

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttpApplication

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzApplicationGatewayHttpHttp Più](./Add-AzApplicationGatewayHttpListener.md)

[Get-AzApplicationGatewayHttpHttp Più](./Get-AzApplicationGatewayHttpListener.md)

[Remove-AzApplicationGatewayHttpHttp Più](./Remove-AzApplicationGatewayHttpListener.md)

[Set-AzApplicationGatewayHttpHttp Più](./Set-AzApplicationGatewayHttpListener.md)


