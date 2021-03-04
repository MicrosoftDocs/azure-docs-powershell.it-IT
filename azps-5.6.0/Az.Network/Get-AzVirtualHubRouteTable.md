---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: 56f0eb8362cef287cea326ea30a559d7efc70573
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953950"
---
# <span data-ttu-id="bc376-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc376-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="bc376-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc376-102">SYNOPSIS</span></span>
<span data-ttu-id="bc376-103">Ottiene una tabella delle route dell'hub virtuale in un hub virtuale o elenca tutte le tabelle di route in un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc376-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="bc376-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc376-104">SYNTAX</span></span>

### <span data-ttu-id="bc376-105">ByVirtualHubName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bc376-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc376-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="bc376-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc376-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="bc376-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc376-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bc376-108">DESCRIPTION</span></span>
<span data-ttu-id="bc376-109">Ottiene una tabella delle route dell'hub virtuale in un hub virtuale o elenca tutte le tabelle di route in un hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc376-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="bc376-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc376-110">EXAMPLES</span></span>

### <span data-ttu-id="bc376-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc376-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="bc376-112">Questo cmdlet recupera una risorsa della tabella di route usando il nome del gruppo di risorse, il nome dell'hub e il nome della tabella di route.</span><span class="sxs-lookup"><span data-stu-id="bc376-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="bc376-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bc376-113">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded

Name                : routeTable2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable2
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Branches}
ProvisioningState   : Succeeded
```

<span data-ttu-id="bc376-114">Questo cmdlet elenca tutte le tabelle di route presenti in un hub virtuale usando il nome del gruppo di risorse e il nome dell'hub.</span><span class="sxs-lookup"><span data-stu-id="bc376-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="bc376-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc376-115">PARAMETERS</span></span>

### <span data-ttu-id="bc376-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc376-116">-DefaultProfile</span></span>
<span data-ttu-id="bc376-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc376-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc376-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="bc376-118">-HubName</span></span>
<span data-ttu-id="bc376-119">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="bc376-119">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc376-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bc376-120">-Name</span></span>
<span data-ttu-id="bc376-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bc376-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc376-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bc376-122">-ParentResourceId</span></span>
<span data-ttu-id="bc376-123">ID risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="bc376-123">The parent resource id.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc376-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc376-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc376-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bc376-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc376-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="bc376-126">-VirtualHub</span></span>
<span data-ttu-id="bc376-127">La risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="bc376-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentObject, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc376-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc376-128">CommonParameters</span></span>
<span data-ttu-id="bc376-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc376-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc376-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bc376-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc376-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="bc376-131">INPUTS</span></span>

### <span data-ttu-id="bc376-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bc376-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="bc376-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bc376-133">System.String</span></span>

## <span data-ttu-id="bc376-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc376-134">OUTPUTS</span></span>

### <span data-ttu-id="bc376-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc376-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="bc376-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="bc376-136">NOTES</span></span>

## <span data-ttu-id="bc376-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc376-137">RELATED LINKS</span></span>
