---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: d4945c93fdfb402e56e1822229a1bb9592951d20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853653"
---
# <span data-ttu-id="17b81-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17b81-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="17b81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17b81-102">SYNOPSIS</span></span>
<span data-ttu-id="17b81-103">Ottiene un Azure VirtualHub per nome e ResourceGroupName o elenca tutti gli hub virtuali per ResourceGroupName/abbonamento.</span><span class="sxs-lookup"><span data-stu-id="17b81-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="17b81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17b81-104">SYNTAX</span></span>

### <span data-ttu-id="17b81-105">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17b81-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17b81-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b81-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17b81-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17b81-107">DESCRIPTION</span></span>
<span data-ttu-id="17b81-108">Ottiene un Azure VirtualHub per nome e ResourceGroupName o elenca tutti gli hub virtuali per ResourceGroupName/abbonamento.</span><span class="sxs-lookup"><span data-stu-id="17b81-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="17b81-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17b81-109">EXAMPLES</span></span>

### <span data-ttu-id="17b81-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17b81-110">Example 1</span></span>

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

<span data-ttu-id="17b81-111">Quanto sopra creerà un gruppo di risorse "testRG", una WAN virtuale e un hub virtuale in West US nel gruppo di risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="17b81-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="17b81-112">L'hub virtuale avrà lo spazio indirizzo "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="17b81-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="17b81-113">Ottiene quindi l'hub virtuale usando il relativo ResourceGroupName e il resourceName.</span><span class="sxs-lookup"><span data-stu-id="17b81-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="17b81-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="17b81-114">Example 2</span></span>

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

<span data-ttu-id="17b81-115">Questo cmdlet consente di ottenere l'hub virtuale usando il filtro.</span><span class="sxs-lookup"><span data-stu-id="17b81-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="17b81-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17b81-116">PARAMETERS</span></span>

### <span data-ttu-id="17b81-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b81-117">-DefaultProfile</span></span>
<span data-ttu-id="17b81-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17b81-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17b81-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="17b81-119">-Name</span></span>
<span data-ttu-id="17b81-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="17b81-120">The resource name.</span></span>

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

### <span data-ttu-id="17b81-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b81-121">-ResourceGroupName</span></span>
<span data-ttu-id="17b81-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="17b81-122">The resource group name.</span></span>

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

### <span data-ttu-id="17b81-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b81-123">CommonParameters</span></span>
<span data-ttu-id="17b81-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b81-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b81-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17b81-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b81-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17b81-126">INPUTS</span></span>

### <span data-ttu-id="17b81-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="17b81-127">None</span></span>

## <span data-ttu-id="17b81-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17b81-128">OUTPUTS</span></span>

### <span data-ttu-id="17b81-129">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17b81-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="17b81-130">Note</span><span class="sxs-lookup"><span data-stu-id="17b81-130">NOTES</span></span>

## <span data-ttu-id="17b81-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17b81-131">RELATED LINKS</span></span>

[<span data-ttu-id="17b81-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17b81-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="17b81-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17b81-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="17b81-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17b81-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
