---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: d6657c9402eff46d274d982170e167cd97a29a9a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022043"
---
# <span data-ttu-id="a40ba-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-101">Get-AzFirewall</span></span>

## <span data-ttu-id="a40ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a40ba-102">SYNOPSIS</span></span>
<span data-ttu-id="a40ba-103">Ottiene un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="a40ba-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="a40ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a40ba-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a40ba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a40ba-105">DESCRIPTION</span></span>
<span data-ttu-id="a40ba-106">Il cmdlet **Get-AzFirewall** ottiene uno o più firewall in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a40ba-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="a40ba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a40ba-107">EXAMPLES</span></span>

### <span data-ttu-id="a40ba-108">1: recuperare tutti i firewall in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a40ba-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzFirewall -ResourceGroupName rgName

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="a40ba-109">Questo esempio recupera tutti i firewall nel gruppo di risorse "rgName".</span><span class="sxs-lookup"><span data-stu-id="a40ba-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="a40ba-110">2: recuperare un firewall per nome</span><span class="sxs-lookup"><span data-stu-id="a40ba-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzFirewall -ResourceGroupName rgName -Name azFw

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="a40ba-111">Questo esempio recupera il firewall denominato "azFw" nel gruppo di risorse "rgName".</span><span class="sxs-lookup"><span data-stu-id="a40ba-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="a40ba-112">3: recuperare tutti i firewall con filtro</span><span class="sxs-lookup"><span data-stu-id="a40ba-112">3:  Retrieve all Firewalls with filtering</span></span>
```
Get-AzFirewall -Name azFw*

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="a40ba-113">Questo esempio recupera tutti i firewall che iniziano con "azFw"</span><span class="sxs-lookup"><span data-stu-id="a40ba-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="a40ba-114">4: recuperare un firewall e quindi aggiungere una raccolta di regole applicazione al firewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="a40ba-115">Questo esempio recupera un firewall e quindi aggiunge una raccolta di regole applicazione al firewall chiamando il metodo AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="a40ba-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="a40ba-116">5: recuperare un firewall e quindi aggiungere una raccolta di regole di rete al firewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="a40ba-117">Questo esempio recupera un firewall e quindi aggiunge una raccolta di regole di rete al firewall chiamando il metodo AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="a40ba-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="a40ba-118">6: recuperare un firewall e quindi recuperare una raccolta di regole applicazione per nome dal firewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="a40ba-119">Questo esempio recupera un firewall e quindi ottiene una raccolta di regole in base al nome, chiamando il metodo GetApplicationRuleCollectionByName sull'oggetto firewall.</span><span class="sxs-lookup"><span data-stu-id="a40ba-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a40ba-120">Il nome della raccolta regole per il metodo GetApplicationRuleCollectionByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a40ba-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a40ba-121">7: recuperare un firewall e quindi recuperare una raccolta di regole di rete per nome dal firewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="a40ba-122">Questo esempio recupera un firewall e quindi ottiene una raccolta di regole in base al nome, chiamando il metodo GetNetworkRuleCollectionByName sull'oggetto firewall.</span><span class="sxs-lookup"><span data-stu-id="a40ba-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a40ba-123">Il nome della raccolta regole per il metodo GetNetworkRuleCollectionByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a40ba-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a40ba-124">8: recuperare un firewall e quindi rimuovere una raccolta di regole applicazione per nome dal firewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="a40ba-125">Questo esempio recupera un firewall e quindi rimuove una raccolta di regole in base al nome, chiamando il metodo RemoveApplicationRuleCollectionByName sull'oggetto firewall.</span><span class="sxs-lookup"><span data-stu-id="a40ba-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a40ba-126">Il nome della raccolta regole per il metodo RemoveApplicationRuleCollectionByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a40ba-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a40ba-127">9: recuperare un firewall e quindi rimuovere una raccolta di regole di rete per nome dal firewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="a40ba-128">Questo esempio recupera un firewall e quindi rimuove una raccolta di regole in base al nome, chiamando il metodo RemoveNetworkRuleCollectionByName sull'oggetto firewall.</span><span class="sxs-lookup"><span data-stu-id="a40ba-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a40ba-129">Il nome della raccolta regole per il metodo RemoveNetworkRuleCollectionByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a40ba-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a40ba-130">10: recuperare un firewall e quindi allocare il firewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="a40ba-131">Questo esempio recupera un firewall e chiama allocate sul firewall per avviare il servizio firewall usando la configurazione (Application and Network Rule Collections) associata al firewall.</span><span class="sxs-lookup"><span data-stu-id="a40ba-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="a40ba-132">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a40ba-132">PARAMETERS</span></span>

### <span data-ttu-id="a40ba-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40ba-133">-DefaultProfile</span></span>
<span data-ttu-id="a40ba-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a40ba-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a40ba-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="a40ba-135">-Name</span></span>
<span data-ttu-id="a40ba-136">Specifica il nome del firewall ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a40ba-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a40ba-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a40ba-137">-ResourceGroupName</span></span>
<span data-ttu-id="a40ba-138">Specifica il nome del gruppo di risorse a cui appartiene il firewall.</span><span class="sxs-lookup"><span data-stu-id="a40ba-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a40ba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40ba-139">CommonParameters</span></span>
<span data-ttu-id="a40ba-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40ba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40ba-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40ba-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40ba-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a40ba-142">INPUTS</span></span>

### <span data-ttu-id="a40ba-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a40ba-143">System.String</span></span>

## <span data-ttu-id="a40ba-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a40ba-144">OUTPUTS</span></span>

### <span data-ttu-id="a40ba-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="a40ba-146">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSAzureFirewall, Microsoft. Azure. PowerShell. Cmdlets. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a40ba-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a40ba-147">Note</span><span class="sxs-lookup"><span data-stu-id="a40ba-147">NOTES</span></span>

## <span data-ttu-id="a40ba-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a40ba-148">RELATED LINKS</span></span>

[<span data-ttu-id="a40ba-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a40ba-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="a40ba-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a40ba-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
