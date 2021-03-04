---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 630e0a6759e278e4da2d6d56cf34bb5fa5812595
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953998"
---
# <span data-ttu-id="bdff0-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bdff0-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="bdff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdff0-102">SYNOPSIS</span></span>
<span data-ttu-id="bdff0-103">Ottiene un elemento VirtualHub di Azure in base al nome e a ResourceGroupName oppure elenca tutti gli hub virtuali in base a ResourceGroupName/Subscription.</span><span class="sxs-lookup"><span data-stu-id="bdff0-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="bdff0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdff0-104">SYNTAX</span></span>

### <span data-ttu-id="bdff0-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bdff0-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdff0-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdff0-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdff0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bdff0-107">DESCRIPTION</span></span>
<span data-ttu-id="bdff0-108">Ottiene un elemento VirtualHub di Azure in base al nome e a ResourceGroupName oppure elenca tutti gli hub virtuali in base a ResourceGroupName/Subscription.</span><span class="sxs-lookup"><span data-stu-id="bdff0-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="bdff0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdff0-109">EXAMPLES</span></span>

### <span data-ttu-id="bdff0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bdff0-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="bdff0-111">La procedura descritta sopra consente di creare un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale negli Stati Uniti occidentali in tale gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="bdff0-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="bdff0-112">L'hub virtuale avrà lo spazio di indirizzi "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="bdff0-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="bdff0-113">Ottiene quindi l'hub virtuale usando i relativi ResourceGroupName e ResourceName.</span><span class="sxs-lookup"><span data-stu-id="bdff0-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="bdff0-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bdff0-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualHub -Name westushub*

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub1
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub1
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub2
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub2
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="bdff0-115">Questo cmdlet ottiene l'hub virtuale usando i filtri.</span><span class="sxs-lookup"><span data-stu-id="bdff0-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="bdff0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdff0-116">PARAMETERS</span></span>

### <span data-ttu-id="bdff0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdff0-117">-DefaultProfile</span></span>
<span data-ttu-id="bdff0-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bdff0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdff0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bdff0-119">-Name</span></span>
<span data-ttu-id="bdff0-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bdff0-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="bdff0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdff0-121">-ResourceGroupName</span></span>
<span data-ttu-id="bdff0-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bdff0-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="bdff0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdff0-123">CommonParameters</span></span>
<span data-ttu-id="bdff0-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdff0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdff0-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bdff0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdff0-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="bdff0-126">INPUTS</span></span>

### <span data-ttu-id="bdff0-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bdff0-127">None</span></span>

## <span data-ttu-id="bdff0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdff0-128">OUTPUTS</span></span>

### <span data-ttu-id="bdff0-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bdff0-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="bdff0-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="bdff0-130">NOTES</span></span>

## <span data-ttu-id="bdff0-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdff0-131">RELATED LINKS</span></span>

[<span data-ttu-id="bdff0-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bdff0-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="bdff0-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bdff0-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="bdff0-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bdff0-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
