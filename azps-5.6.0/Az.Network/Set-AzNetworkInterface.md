---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 0afd299103f1595afd100a7e9a72c4045896419d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987698"
---
# Set-AzNetworkInterface

## SYNOPSIS
Aggiorna un'interfaccia di rete.

## SINTASSI

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
**Set-AzNetworkInterface** aggiorna un'interfaccia di rete.

## ESEMPI

### Esempio 1: Configurare un'interfaccia di rete
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

Questo esempio configura un'interfaccia di rete.
Il primo comando ottiene un'interfaccia di rete denominata NetworkInterface1 nel gruppo di risorse ResourceGroup1.
Il secondo comando imposta l'indirizzo IP privato della configurazione IP.
Il terzo comando imposta il metodo di allocazione IP privato su Statico.
Il quarto comando imposta un tag nell'interfaccia di rete.
Il quinto comando usa le informazioni archiviate nella variabile $Nic per impostare l'interfaccia di rete.

### Esempio 2: Modificare le impostazioni DNS in un'interfaccia di rete
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

Il primo comando ottiene un'interfaccia di rete denominata NetworkInterface1 presente nel gruppo di risorse ResourceGroup1. Il secondo comando aggiunge il server DNS 192.168.1.100 a questa interfaccia. Il terzo comando applica queste modifiche all'interfaccia di rete. Per rimuovere un server DNS, seguire i comandi elencati sopra, ma sostituire ". Aggiungere" con ". Rimuovi" nel secondo comando.

### Esempio 3: Abilitare l'inoltro IP su un'interfaccia di rete
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

Il primo comando ottiene un'interfaccia di rete esistente denominata NetworkInterface1 e la archivia nella $nic variabile. Il secondo comando modifica il valore di inoltro IP in true. Infine, il terzo comando applica le modifiche all'interfaccia di rete. Per disabilitare l'inoltro IP in un'interfaccia di rete, seguire l'esempio di esempio, ma assicurarsi di modificare il secondo comando in "$nic. EnableIPForwarding = 0".

### Esempio 4: Cambiare la subnet di un'interfaccia di rete
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

Il primo comando ottiene l'interfaccia di rete NetworkInterface1 e la archivia nella $nic variabile. Il secondo comando ottiene la rete virtuale associata alla subnet a cui verrà associata l'interfaccia di rete. Il secondo comando recupera la subnet e la archivia nella variabile $subnet 2. Il terzo comando ha associato l'indirizzo IP privato primario dell'interfaccia di rete alla nuova subnet. Infine, l'ultimo comando ha applicato queste modifiche all'interfaccia di rete.
>[!NOTE] 
>Le configurazioni IP devono essere dinamiche prima di poter cambiare la subnet. In caso di configurazioni IP statiche, modificarle in dinamiche prima di procedere. 
>[!NOTE]
>Se l'interfaccia di rete ha più configurazioni IP, il quarto comando deve essere eseguito per tutte queste configurazioni IP prima di eseguire il comando Set-AzNetworkInterface di configurazione finale. Questa operazione può essere eseguita come specificato nel comando, ma sostituendo "0" con il numero appropriato. Se un'interfaccia di rete ha configurazioni N IP, è necessario che esistano N-1 di questi comandi.

### Esempio 5: Associare/dissociare un gruppo di sicurezza di rete a un'interfaccia di rete
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

Il primo comando ottiene un'interfaccia di rete esistente denominata NetworkInterface1 e la archivia nella $nic variabile. Il secondo comando ottiene un gruppo di sicurezza di rete esistente denominato MyNSG e lo archivia nella $nsg variabile. Il terzo comando assegna la $nsg alla $nic. Infine, il comando applica le modifiche all'interfaccia di rete. Per dissociare i gruppi di sicurezza di rete da un'interfaccia di rete, è possibile sostituire $nsg nel terzo comando con $null.

## PARAMETERS

### -AsJob
Eseguire il cmdlet in background

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

### -NetworkInterface
Specifica un oggetto interfaccia di rete che rappresenta lo stato su cui deve essere impostata l'interfaccia di rete.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
