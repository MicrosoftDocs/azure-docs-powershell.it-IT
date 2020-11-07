---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 389a34a5b1c34618339bb7a1752031eaafb9efe9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862765"
---
# Set-AzNetworkInterface

## Sinossi
Imposta lo stato obiettivo per un'interfaccia di rete.

## SINTASSI

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
**Set-AzNetworkInterface** imposta lo stato dell'obiettivo per un'interfaccia di rete Azure.

## ESEMPI

### Esempio 1: configurare un'interfaccia di rete
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

Questo esempio configura un'interfaccia di rete.
Il primo comando consente di ottenere un'interfaccia di rete denominata NetworkInterface1 nel gruppo di risorse ResourceGroup1.
Il secondo comando imposta l'indirizzo IP privato della configurazione IP.
Il terzo comando imposta il metodo di allocazione IP privato su static.
Il quarto comando imposta un contrassegno nell'interfaccia di rete.
Il quinto comando usa le informazioni archiviate nella variabile $Nic per impostare l'interfaccia di rete.

### Esempio 2: modificare le impostazioni DNS in un'interfaccia di rete
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

Il primo comando ottiene un'interfaccia di rete denominata NetworkInterface1 che esiste all'interno del gruppo di risorse ResourceGroup1. Il secondo comando aggiunge il server DNS 192.168.1.100 a questa interfaccia. Il terzo comando applica queste modifiche all'interfaccia di rete. Per rimuovere un server DNS, seguire i comandi elencati sopra, ma sostituisci ". Aggiungi "con". Rimuovi "nel secondo comando.

### Esempio 3: abilitare l'forwading IP in un'interfaccia di rete
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

Il primo comando ottiene un'interfaccia di rete esistente denominata NetworkInterface1 e la archivia nella variabile $nic. Il secondo comando cambia il valore di inoltro IP in vero. Infine, il terzo comando applica le modifiche all'interfaccia di rete. Per disabilitare l'inoltro IP in un'interfaccia di rete, seguire l'esempio di campione, ma assicurarsi di cambiare il secondo comando in "$nic. EnableIPForwarding = 0 ".

### Esempio 4: cambiare la subnet di un'interfaccia di rete
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

Il primo comando ottiene l'interfaccia di rete NetworkInterface1 e lo archivia nella variabile $nic. Il secondo comando ottiene la rete virtuale associata alla subnet in cui verrà associata l'interfaccia di rete. Il secondo comando ottiene la subnet e la archivia nella variabile $subnet 2. Il terzo comando associa l'indirizzo IP privato principale dell'interfaccia di rete alla nuova subnet. Infine, l'ultimo comando ha applicato queste modifiche nell'interfaccia di rete.

>[!NOTE] 
>Le configurazioni IP devono essere dinamiche prima di poter modificare la subnet. Se si hanno configurazioni IP statiche, passare alla dinamica prima di procedere. 

>[!NOTE]
>Se l'interfaccia di rete include più configurazioni IP, il comando Forth deve essere eseguito per tutte queste configurazioni IP prima dell'esecuzione del comando Set-AzNetworkInterface finale. Questa operazione può essere eseguita come nel comando avanti, ma sostituendo "0" con il numero appropriato. Se un'interfaccia di rete include configurazioni N IP, è necessario che N-1 di questi comandi sia presente.

### Esempio 5: associare/dissociare un gruppo di sicurezza di rete a un'interfaccia di rete
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

Il primo comando ottiene un'interfaccia di rete esistente denominata NetworkInterface1 e la archivia nella variabile $nic. Il secondo comando ottiene un gruppo di sicurezza di rete esistente denominato MyNSG e lo archivia nella variabile $nsg. Il comando avanti assegna l'$nsg al $nic. Infine, il quinto comando applica le modifiche all'interfaccia di rete. Per dissociare i gruppi di sicurezza di rete da un'interfaccia di rete, è sufficiente sostituire $nsg nel comando avanti con $null.

## PARAMETRI

### -AsJob
Esegui cmdlet in background

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

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkInterface
Specifica un oggetto **NetworkInterface** che rappresenta lo stato dell'obiettivo per un'interfaccia di rete.

```yaml
Type: PSNetworkInterface
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

### PSNetworkInterface
Il parametro ' NetworkInterface ' accetta il valore di tipo ' PSNetworkInterface ' dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSNetworkInterface

## Note

## COLLEGAMENTI CORRELATI

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
