---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192835"
---
# New-AzApplicationGatewayPathRuleConfig

## Sinossi
Crea una regola di percorso del gateway applicazione.

## SINTASSI

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzApplicationGatewayPathRuleConfig** crea una regola di percorso del gateway dell'applicazione.
Le regole create da questo cmdlet possono essere aggiunte a una raccolta di impostazioni di configurazione della mappa percorso URL e quindi assegnate a un gateway.
Le impostazioni di configurazione della mappa percorso vengono usate in bilanciamento del carico del gateway applicazione.

## ESEMPI

### Esempio 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Questi comandi creano una nuova regola di percorso del gateway applicazione e quindi usano il cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** per assegnare la regola a un gateway dell'applicazione.
A questo scopo, il primo comando crea un riferimento a un oggetto al gateway ContosoApplicationGateway.
Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.
I due comandi successivi creano un pool di indirizzi back-end e un oggetto impostazioni HTTP back-end; questi oggetti (archiviati nelle variabili $AddressPool e $HttpSettings) sono necessari per creare un oggetto regola di percorso.
Il quarto comando crea l'oggetto della regola di percorso e viene archiviato in una variabile denominata $PathRuleConfig.
Il quinto comando USA **Add-AzApplicationGatewayUrlPathMapConfig** per aggiungere le impostazioni di configurazione e la nuova regola di percorso contenuta in tali impostazioni in ContosoApplicationGateway.

### Esempio 2
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

Questo comando crea una regola di percorso con il nome "base", Paths come "/base", BackendAddressPool come $AddressPool, BackendHttpSettings come $HttpSettings e FirewallPolicy come $firewallPolicy. NGS e la nuova regola di percorso contenuta in tali impostazioni in ContosoApplicationGateway.

## PARAMETRI

### -BackendAddressPool
Specifica un riferimento a un oggetto a una raccolta di impostazioni del pool di indirizzi di backend da aggiungere alle impostazioni di configurazione delle regole del percorso gateway.
Puoi creare questo riferimento di oggetto usando il cmdlet New-AzApplicationGatewayBackendAddressPool e la sintassi simile alla seguente: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`
Il comando precedente aggiunge due indirizzi IP (192.16.1.1 e 192.168.1.2) al pool di indirizzi.
Tieni presente che l'indirizzo IP è racchiuso tra virgolette e separato tramite virgole.
La variabile risultante, $AddressPool, può quindi essere usata come valore di parametro per il parametro *DefaultBackendAddressPool* .
Il pool di indirizzi di backend rappresenta gli indirizzi IP nei server back-end.
Questi indirizzi IP dovrebbero appartenere alla subnet della rete virtuale o devono essere indirizzi IP pubblici.
Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendAddressPoolId* nello stesso comando.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
Specifica l'ID di un pool di indirizzi di backend esistente che può essere aggiunto alle impostazioni di configurazione della regola del percorso gateway.
Gli ID del pool di indirizzi possono essere restituiti tramite il cmdlet Get-AzApplicationGatewayBackendAddressPool.
Dopo aver ottenuto l'ID, puoi usare il parametro *DefaultBackendAddressPoolId* invece del parametro *DefaultBackendAddressPool* .
Ad esempio:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" il pool di indirizzi back-end rappresenta gli indirizzi IP nei server back-end.
Questi indirizzi IP dovrebbero appartenere alla subnet della rete virtuale o devono essere indirizzi IP pubblici.

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

### -BackendHttpSettings
Specifica un riferimento a un oggetto a una raccolta di impostazioni HTTP di backend da aggiungere alle impostazioni di configurazione della regola del percorso del gateway.
Puoi creare questo riferimento di oggetto usando il cmdlet New-AzApplicationGatewayBackendHttpSettings e la sintassi simile alla seguente: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSettings"-Port 80-Protocol "http"-CookieBasedAffinity "disabled" la variabile risultante, $HttpSettings, può quindi essere usata come valore di parametro per il parametro *DefaultBackendAddressPool* :-DefaultBackendHttpSettings $HttpSettings le impostazioni http di backend consentono di configurare proprietà come la porta, il protocollo e l'affinità basata su cookie per un pool di back-end.
Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendHttpSettingsId* nello stesso comando.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
Specifica l'ID di una raccolta di impostazioni HTTP di backend esistente che può essere aggiunta alle impostazioni di configurazione della regola del percorso del gateway.
Gli ID delle impostazioni HTTP possono essere restituiti usando il cmdlet Get-AzApplicationGatewayBackendHttpSettings.
Dopo aver ottenuto l'ID, puoi usare il parametro *DefaultBackendHttpSettingsId* invece del parametro *DefaultBackendHttpSettings* .
Ad esempio:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" le impostazioni HTTP di backend configurano proprietà come la porta, il protocollo e l'affinità basata su cookie per un pool di backend.
Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendHttpSettings* nello stesso comando.

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

### -FirewallPolicy
Specifica il riferimento all'oggetto a un criterio firewall di primo livello. Il riferimento all'oggetto può essere creato usando il cmdlet New-AzApplicationGatewayWebApplicationFirewallPolicy.
$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" un criterio firewall creato usando il unifiedgroup precedente può essere riferito a un livello di regola di percorso. sopra il comando creerebbe le impostazioni dei criteri e le regole gestite predefinite.
Invece dei valori predefiniti, gli utenti possono specificare PolicySettings, ManagedRules usando New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules rispettivamente.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyId
Specifica l'ID di una risorsa di firewall applicazione Web di primo livello esistente.
Gli ID dei criteri del firewall possono essere restituiti tramite il cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy. Dopo aver ottenuto l'ID, puoi usare il parametro *FirewallPolicyId* invece del parametro *firewallpolicy* .
Ad esempio:-FirewallPolicyId "/subscriptions/<Subscription-ID>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
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

### -Nome
Specifica il nome della configurazione della regola di percorso creata da questo cmdlet.

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

### -Percorsi
Specifica una o più regole di percorso del gateway applicazione.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
App gateway RedirectConfiguration

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
ID dell'applicazione gateway RedirectConfiguration

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

### -RewriteRuleSet
App gateway RewriteRuleSet

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSetId
ID dell'applicazione gateway RewriteRuleSet

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule

## Note

## COLLEGAMENTI CORRELATI

[Add-AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[Get-AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[New-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)

[New-AzApplicationGatewayBackendHttpSetting](./New-AzApplicationGatewayBackendHttpSetting.md)

[New-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[New-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


