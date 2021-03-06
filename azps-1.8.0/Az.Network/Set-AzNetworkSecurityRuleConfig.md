---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 4293f044a270a43f12c7b4d74a410a324d0284dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677946"
---
# Set-AzNetworkSecurityRuleConfig

## Sinossi
Aggiorna una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete.

## SINTASSI

### SetByResource (impostazione predefinita)
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzNetworkSecurityRuleConfig** aggiorna una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete.

## ESEMPI

### Esempio 1: modificare la configurazione di Access in una regola di sicurezza di rete
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

Il primo comando ottiene il gruppo di sicurezza di rete denominato NSG-FrontEnd e lo archivia nella variabile $nsg.
Il secondo comando usa l'operatore pipeline per passare il gruppo di sicurezza in $nsg a Get-AzNetworkSecurityRuleConfig, che ottiene la configurazione della regola di sicurezza denominata RDP-Rule.
Il terzo comando modifica la configurazione di Access di RDP-Rule in Deny.

## PARAMETRI

### -Access
Specifica se il traffico di rete è consentito o negato. I valori accettabili per questo parametro sono: Allow e Deny.

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

### -Descrizione
Specifica una descrizione per una configurazione di regola.
La dimensione massima è di 140 caratteri.

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
Specifica un prefisso per l'indirizzo di destinazione.
I valori accettabili per questo parametro sono i seguenti:
- Un indirizzo CIDR (classe Interdomain Routing) 
- Un intervallo di indirizzi IP di destinazione 
- Un carattere jolly (*) in modo che corrisponda a qualsiasi indirizzo IP, è possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.

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
Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola. Non può essere usato con il parametro "DestinationAddressPrefix".

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
Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola. Non può essere usato con il parametro "DestinationAddressPrefix".

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
I valori accettabili per questo parametro sono i seguenti:
- Un numero intero 
- Un intervallo di numeri interi compresi tra 0 e 65535
- Carattere jolly (*) che corrisponde a qualsiasi porta

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

### -Direzione
Specifica se una regola viene valutata per il traffico in entrata o in uscita.
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

### -Nome
Specifica il nome della configurazione della regola di sicurezza della rete impostata da questo cmdlet.

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
Specifica l'oggetto **NetworkSecurityGroup** che contiene la configurazione della regola di sicurezza della rete da impostare.

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

### -Priorità
Specifica la priorità di una configurazione di regola.
I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.
Il numero di priorità deve essere univoco per ogni regola della raccolta.
Minore è il numero di priorità, maggiore è la priorità della regola.

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

### -Protocollo
Specifica il protocollo di rete a cui si applica una configurazione di regola.
I valori accettabili per questo parametro sono:--TCP
- UDP
- Carattere jolly (*) in modo che corrisponda a entrambi

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
Specifica un prefisso per l'indirizzo di origine.
I valori accettabili per questo parametro sono i seguenti:
- UN CIDR
- Un intervallo IP di origine
- Un carattere jolly (*) in modo che corrisponda a qualsiasi indirizzo IP è anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.

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
Gruppo di sicurezza dell'applicazione impostato come origine per la regola. Non può essere usato con il parametro "SourceAddressPrefix".

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
Gruppo di sicurezza dell'applicazione impostato come origine per la regola. Non può essere usato con il parametro "SourceAddressPrefix".

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
Specifica la porta o l'intervallo di origine.
I valori accettabili per questo parametro sono i seguenti:
- Un numero intero
- Un intervallo di numeri interi compresi tra 0 e 65535
- Carattere jolly (*) che corrisponde a qualsiasi porta

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup

## Note

## COLLEGAMENTI CORRELATI

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)


