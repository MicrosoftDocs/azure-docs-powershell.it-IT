---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192023"
---
# Add-AzNetworkSecurityRuleConfig

## SYNOPSIS
Aggiunge una configurazione della regola di sicurezza di rete a un gruppo di sicurezza di rete.

## SINTASSI

### SetByResource (Impostazione predefinita)
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Add-AzNetworkSecurityRuleConfig aggiunge** una configurazione della regola di sicurezza di rete a un gruppo di sicurezza di rete di Azure.

## ESEMPI

### 1: Aggiunta di un gruppo di sicurezza di rete
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

Il primo comando recupera un gruppo di sicurezza di rete Azure denominato "nsg1" dal gruppo di risorse "rg1". Il secondo comando aggiunge una regola di sicurezza di rete denominata "rdp-rule" che consente il traffico Da Internet sulla porta 3389 all'oggetto gruppo di sicurezza di rete recuperato. Mantiene il gruppo di sicurezza di rete Azure modificato.

### 2: Aggiunta di una nuova regola di sicurezza con i gruppi di sicurezza delle applicazioni
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

Prima di tutto, vengono creati due nuovi gruppi di sicurezza delle applicazioni. Recupera quindi un gruppo di sicurezza di rete Azure denominato "nsg1" dal gruppo di risorse "rg1". e aggiunge una regola di sicurezza di rete denominata "rdp-rule". La regola consente il traffico da tutte le configurazioni IP nel gruppo di sicurezza dell'applicazione "srcAsg" a tutte le configurazioni IP in "destAsg" sulla porta 3389. Dopo aver aggiunto la regola, il gruppo di sicurezza di rete Azure modificato viene mantenuto.

## PARAMETERS

### -Access
Specifica se il traffico di rete è consentito o negato.
I valori accettabili per questo parametro sono: Allow e Deny.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

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

### -Descrizione
Specifica una descrizione della configurazione di una regola di sicurezza di rete.

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

### -DestinationAddressPrefix
Specifica un prefisso di indirizzo di destinazione.
I valori accettabili per questo parametro sono:
- Indirizzo Classless Interdomain Routing (CIDR)
- Un intervallo di indirizzi IP di destinazione
- Un carattere jolly (*) per corrispondere a qualsiasi indirizzo IP È possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.

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

### -DestinationApplicationSecurityGroup
Gruppo di sicurezza dell'applicazione impostato come destinazione della regola. Non può essere usato con il parametro 'DestinationAddressPrefix'.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroupId
Gruppo di sicurezza dell'applicazione impostato come destinazione della regola. Non può essere usato con il parametro 'DestinationAddressPrefix'.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
Specifica una porta o un intervallo di destinazione.
I valori accettabili per questo parametro sono:
- Un numero intero
- Intervallo di interi compreso tra 0 e 65535
- Un carattere jolly (*) che corrisponda a qualsiasi porta

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

### -Direction
Specifica se una regola viene valutata sul traffico in arrivo o in uscita.
I valori accettabili per questo parametro sono: in ingresso e in uscita.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifica il nome di una configurazione della regola di sicurezza di rete.

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

### -NetworkSecurityGroup
Specifica un **oggetto NetworkSecurityGroup.**
Questo cmdlet aggiunge all'oggetto specificato da questo parametro una configurazione della regola di sicurezza di rete.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Priority
Specifica la priorità di una configurazione delle regole.
I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.
Il numero di priorità deve essere univoco per ogni regola della raccolta.
Più basso è il numero di priorità, più alta sarà la priorità della regola.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Specifica il protocollo di rete a cui si applica una configurazione di regole.
I valori accettabili per questo parametro sono:
- Tcp
- Udp
- Carattere jolly (*) per trovare le corrispondenze con entrambe le corrispondenze

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
Specifica un prefisso dell'indirizzo di origine.
I valori accettabili per questo parametro sono:
- UN CIDR
- Un intervallo IP di origine
- Un carattere jolly (*) che corrisponda a qualsiasi indirizzo IP.
È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.

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

### -SourceApplicationSecurityGroup
Gruppo di sicurezza dell'applicazione impostato come origine della regola. Non può essere usato con il parametro 'SourceAddressPrefix'.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroupId
Gruppo di sicurezza dell'applicazione impostato come origine della regola. Non può essere usato con il parametro 'SourceAddressPrefix'.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
Specifica una porta o un intervallo di origine.
Questo valore viene espresso come numero intero, come intervallo compreso tra 0 e 65535 o come carattere jolly (*) in modo che corrisponda a qualsiasi porta di origine.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


