---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688081"
---
# Get-AzureRmFirewall

## Sinossi
Ottiene un firewall di Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmFirewall** ottiene uno o più firewall in un gruppo di risorse.

## ESEMPI

### 1: recuperare tutti i firewall in un gruppo di risorse
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

Questo esempio recupera tutti i firewall nel gruppo di risorse "rgName".

### 2: recuperare un firewall per nome
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

Questo esempio recupera il firewall denominato "azFw" nel gruppo di risorse "rgName".

### 3: recuperare un firewall e quindi aggiungere una raccolta di regole applicazione al firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

Questo esempio recupera un firewall e quindi aggiunge una raccolta di regole applicazione al firewall chiamando il metodo AddApplicationRuleCollection.

### 4: recuperare un firewall e quindi aggiungere una raccolta di regole di rete al firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

Questo esempio recupera un firewall e quindi aggiunge una raccolta di regole di rete al firewall chiamando il metodo AddNetworkRuleCollection.

### 5: recuperare un firewall e quindi recuperare una raccolta di regole applicazione per nome dal firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

Questo esempio recupera un firewall e quindi ottiene una raccolta di regole in base al nome, chiamando il metodo GetApplicationRuleCollectionByName sull'oggetto firewall. Il nome della raccolta regole per il metodo GetApplicationRuleCollectionByName è senza distinzione tra maiuscole e minuscole.

### 6: recuperare un firewall e quindi recuperare una raccolta di regole di rete per nome dal firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

Questo esempio recupera un firewall e quindi ottiene una raccolta di regole in base al nome, chiamando il metodo GetNetworkRuleCollectionByName sull'oggetto firewall. Il nome della raccolta regole per il metodo GetNetworkRuleCollectionByName è senza distinzione tra maiuscole e minuscole.

### 7: recuperare un firewall e quindi rimuovere una raccolta di regole applicazione per nome dal firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

Questo esempio recupera un firewall e quindi rimuove una raccolta di regole in base al nome, chiamando il metodo RemoveApplicationRuleCollectionByName sull'oggetto firewall. Il nome della raccolta regole per il metodo RemoveApplicationRuleCollectionByName è senza distinzione tra maiuscole e minuscole.

### 8: recuperare un firewall e quindi rimuovere una raccolta di regole di rete per nome dal firewall
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

Questo esempio recupera un firewall e quindi rimuove una raccolta di regole in base al nome, chiamando il metodo RemoveNetworkRuleCollectionByName sull'oggetto firewall. Il nome della raccolta regole per il metodo RemoveNetworkRuleCollectionByName è senza distinzione tra maiuscole e minuscole.

### 9: recuperare un firewall e quindi allocare il firewall
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

Questo esempio recupera un firewall e chiama allocate sul firewall per avviare il servizio firewall usando la configurazione (Application and Network Rule Collections) associata al firewall.

## PARAMETRI

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

### -Nome
Specifica il nome del firewall ottenuto da questo cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui appartiene il firewall.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)

[Set-AzureRmFirewall](./Set-AzureRmFirewall.md)
