---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 1ab3d82b494d5598081ea229a7ae50d486b8ca20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189519"
---
# Set-AzFirewall

## SYNOPSIS
Salva un firewall modificato.

## SINTASSI

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzFirewall** aggiorna un firewall di Azure.

## ESEMPI

### 1: priorità di aggiornamento di una raccolta di regole dell'applicazione firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

Questo esempio aggiorna la priorità di una raccolta di regole esistente di un firewall di Azure.
Presupponendo che "AzureFirewall" del firewall azure nel gruppo di risorse "rg" contenga una raccolta di regole dell'applicazione denominata "ruleCollectionName", i comandi precedenti cambieranno la priorità di quella raccolta di regole e aggiorneranno il firewall di Azure in un secondo momento. Senza il Set-AzFirewall comando, tutte le operazioni eseguite sull'oggetto $azFw locale non si riflettono sul server.

### 2: Creare un firewall di Azure e impostare una raccolta di regole dell'applicazione in un secondo momento
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

In questo esempio viene creato prima un firewall senza raccolte di regole dell'applicazione. Al termine della creazione di una regola dell'applicazione e di una raccolta di regole dell'applicazione, l'oggetto Firewall viene modificato in memoria, senza influire sulla configurazione reale nel cloud. Perché le modifiche si riflettano nel cloud, Set-AzFirewall essere chiamato.

### 3: Aggiornare la modalità di funzionamento di Threat Intel di Azure Firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

Questo esempio aggiorna la modalità di operazione Threat Intel di Azure Firewall "AzureFirewall" nel gruppo di risorse "rg".
Senza il Set-AzFirewall comando, tutte le operazioni eseguite sull'oggetto $azFw locale non si riflettono sul server.

### 4: Deassegnare e allocare il firewall
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
Questo esempio recupera un firewall, deassegna il firewall e lo salva. Il comando Deassegna rimuove il servizio in esecuzione, mantenendo però la configurazione del firewall. Perché le modifiche si riflettano nel cloud, Set-AzFirewall essere chiamato.
Se l'utente vuole avviare di nuovo il servizio, il metodo Allocate deve essere chiamato nel firewall.
La nuova rete virtuale e l'INDIRIZZO IP pubblico devono essere nello stesso gruppo di risorse del firewall. Anche in questo caso, per riflettere le modifiche nel cloud, Set-AzFirewall essere chiamato.

### 5: Eseguire l'assegnazione con un indirizzo IP pubblico di gestione per scenari di tunneling forzato
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
Questo esempio alloca il firewall con un indirizzo IP pubblico di gestione e una subnet per scenari di tunneling forzato. La rete VNet deve contenere una subnet denominata "AzureFirewallManagementSubnet".

### 6: Aggiungere un indirizzo IP pubblico a un firewall di Azure
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

In questo esempio l'indirizzo IP pubblico "azFwPublicIp1" associato al firewall.

### 7: Rimuovere un indirizzo IP pubblico da un firewall di Azure
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

In questo esempio l'indirizzo IP pubblico "azFwPublicIp1" è scollegato dal firewall.

### 8: Modificare l'indirizzo IP pubblico di gestione in un firewall di Azure
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

In questo esempio l'indirizzo IP pubblico di gestione del firewall verrà modificato in "AzFwMgmtPublicIp2"

### 9: Aggiungere la configurazione DNS a un firewall di Azure
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

In questo esempio, la configurazione del server DNS e del proxy DNS è collegata al firewall.

### 10: aggiornare la destinazione di una regola esistente in una raccolta di regole dell'applicazione firewall
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

Questo esempio aggiorna la destinazione di una regola esistente in una raccolta di regole di un firewall di Azure. In questo modo è possibile aggiornare automaticamente le regole quando gli indirizzi IP cambiano dinamicamente.

### 11: Consenti FTP attivo nel firewall di Azure
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

In questo esempio, FTP attivo è consentito nel firewall.

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

### -AzureFirewall
The AzureFirewall

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
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

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## OUTPUT

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
