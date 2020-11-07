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
# <span data-ttu-id="37ec7-101">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-101">Get-AzureRmFirewall</span></span>

## <span data-ttu-id="37ec7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="37ec7-103">Ottiene un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="37ec7-103">Gets a Azure Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37ec7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37ec7-104">SYNTAX</span></span>

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37ec7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37ec7-105">DESCRIPTION</span></span>
<span data-ttu-id="37ec7-106">Il cmdlet **Get-AzureRmFirewall** ottiene uno o più firewall in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37ec7-106">The **Get-AzureRmFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="37ec7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37ec7-107">EXAMPLES</span></span>

### <span data-ttu-id="37ec7-108">1: recuperare tutti i firewall in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="37ec7-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

<span data-ttu-id="37ec7-109">Questo esempio recupera tutti i firewall nel gruppo di risorse "rgName".</span><span class="sxs-lookup"><span data-stu-id="37ec7-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="37ec7-110">2: recuperare un firewall per nome</span><span class="sxs-lookup"><span data-stu-id="37ec7-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

<span data-ttu-id="37ec7-111">Questo esempio recupera il firewall denominato "azFw" nel gruppo di risorse "rgName".</span><span class="sxs-lookup"><span data-stu-id="37ec7-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="37ec7-112">3: recuperare un firewall e quindi aggiungere una raccolta di regole applicazione al firewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-112">3:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="37ec7-113">Questo esempio recupera un firewall e quindi aggiunge una raccolta di regole applicazione al firewall chiamando il metodo AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="37ec7-113">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="37ec7-114">4: recuperare un firewall e quindi aggiungere una raccolta di regole di rete al firewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-114">4:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="37ec7-115">Questo esempio recupera un firewall e quindi aggiunge una raccolta di regole di rete al firewall chiamando il metodo AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="37ec7-115">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="37ec7-116">5: recuperare un firewall e quindi recuperare una raccolta di regole applicazione per nome dal firewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-116">5:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="37ec7-117">Questo esempio recupera un firewall e quindi ottiene una raccolta di regole in base al nome, chiamando il metodo GetApplicationRuleCollectionByName sull'oggetto firewall.</span><span class="sxs-lookup"><span data-stu-id="37ec7-117">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="37ec7-118">Il nome della raccolta regole per il metodo GetApplicationRuleCollectionByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="37ec7-118">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="37ec7-119">6: recuperare un firewall e quindi recuperare una raccolta di regole di rete per nome dal firewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-119">6:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="37ec7-120">Questo esempio recupera un firewall e quindi ottiene una raccolta di regole in base al nome, chiamando il metodo GetNetworkRuleCollectionByName sull'oggetto firewall.</span><span class="sxs-lookup"><span data-stu-id="37ec7-120">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="37ec7-121">Il nome della raccolta regole per il metodo GetNetworkRuleCollectionByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="37ec7-121">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="37ec7-122">7: recuperare un firewall e quindi rimuovere una raccolta di regole applicazione per nome dal firewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-122">7:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="37ec7-123">Questo esempio recupera un firewall e quindi rimuove una raccolta di regole in base al nome, chiamando il metodo RemoveApplicationRuleCollectionByName sull'oggetto firewall.</span><span class="sxs-lookup"><span data-stu-id="37ec7-123">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="37ec7-124">Il nome della raccolta regole per il metodo RemoveApplicationRuleCollectionByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="37ec7-124">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="37ec7-125">8: recuperare un firewall e quindi rimuovere una raccolta di regole di rete per nome dal firewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-125">8:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="37ec7-126">Questo esempio recupera un firewall e quindi rimuove una raccolta di regole in base al nome, chiamando il metodo RemoveNetworkRuleCollectionByName sull'oggetto firewall.</span><span class="sxs-lookup"><span data-stu-id="37ec7-126">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="37ec7-127">Il nome della raccolta regole per il metodo RemoveNetworkRuleCollectionByName è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="37ec7-127">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="37ec7-128">9: recuperare un firewall e quindi allocare il firewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-128">9:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="37ec7-129">Questo esempio recupera un firewall e chiama allocate sul firewall per avviare il servizio firewall usando la configurazione (Application and Network Rule Collections) associata al firewall.</span><span class="sxs-lookup"><span data-stu-id="37ec7-129">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="37ec7-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37ec7-130">PARAMETERS</span></span>

### <span data-ttu-id="37ec7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ec7-131">-DefaultProfile</span></span>
<span data-ttu-id="37ec7-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37ec7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37ec7-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="37ec7-133">-Name</span></span>
<span data-ttu-id="37ec7-134">Specifica il nome del firewall ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37ec7-134">Specifies the name of the Firewall that this cmdlet gets.</span></span>

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

### <span data-ttu-id="37ec7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ec7-135">-ResourceGroupName</span></span>
<span data-ttu-id="37ec7-136">Specifica il nome del gruppo di risorse a cui appartiene il firewall.</span><span class="sxs-lookup"><span data-stu-id="37ec7-136">Specifies the name of the resource group that Firewall belongs to.</span></span>

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

### <span data-ttu-id="37ec7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ec7-137">CommonParameters</span></span>
<span data-ttu-id="37ec7-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ec7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ec7-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ec7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ec7-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37ec7-140">INPUTS</span></span>

### <span data-ttu-id="37ec7-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="37ec7-141">None</span></span>
<span data-ttu-id="37ec7-142">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="37ec7-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37ec7-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37ec7-143">OUTPUTS</span></span>

### <span data-ttu-id="37ec7-144">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-144">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="37ec7-145">Note</span><span class="sxs-lookup"><span data-stu-id="37ec7-145">NOTES</span></span>

## <span data-ttu-id="37ec7-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37ec7-146">RELATED LINKS</span></span>

[<span data-ttu-id="37ec7-147">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-147">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="37ec7-148">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-148">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="37ec7-149">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="37ec7-149">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
