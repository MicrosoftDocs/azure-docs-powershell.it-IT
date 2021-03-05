---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 34cae1bcc6020e2e0c2a8b2f6b70e302c8576f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999997"
---
# <span data-ttu-id="81b69-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="81b69-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="81b69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81b69-102">SYNOPSIS</span></span>
<span data-ttu-id="81b69-103">Ottiene un elenco di dipendenze non risolte.</span><span class="sxs-lookup"><span data-stu-id="81b69-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="81b69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81b69-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DependencyLevel <DependencyLevel>] [-Filter <String>] [-Orderby <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="81b69-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="81b69-105">DESCRIPTION</span></span>
<span data-ttu-id="81b69-106">Ottiene un elenco di dipendenze non risolte.</span><span class="sxs-lookup"><span data-stu-id="81b69-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="81b69-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81b69-107">EXAMPLES</span></span>

### <span data-ttu-id="81b69-108">Esempio 1: Ottenere l'elenco delle risorse dipendenti non risolte per una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="81b69-108">Example 1: Get list of unresolved dependent resources for a Move Collection.</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -DependencyLevel Descendant
Count Id                                                                                                                                        
----- --                                                                                                                                        
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111   
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
    3 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm
```

<span data-ttu-id="81b69-109">Ottenere un elenco di risorse dipendenti non risolte per una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="81b69-109">Get a list of unresolved dependent resources for a Move Collection.</span></span>

## <span data-ttu-id="81b69-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81b69-110">PARAMETERS</span></span>

### <span data-ttu-id="81b69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b69-111">-DefaultProfile</span></span>
<span data-ttu-id="81b69-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81b69-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b69-113">-DependencyLevel</span><span class="sxs-lookup"><span data-stu-id="81b69-113">-DependencyLevel</span></span>
<span data-ttu-id="81b69-114">Definisce il livello di dipendenza.</span><span class="sxs-lookup"><span data-stu-id="81b69-114">Defines the dependency level.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.DependencyLevel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b69-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="81b69-115">-Filter</span></span>
<span data-ttu-id="81b69-116">Filtro da applicare all'operazione.</span><span class="sxs-lookup"><span data-stu-id="81b69-116">The filter to apply on the operation.</span></span>
<span data-ttu-id="81b69-117">Ad esempio, $apply=filtro(conteggio eq 2).</span><span class="sxs-lookup"><span data-stu-id="81b69-117">For example, $apply=filter(count eq 2).</span></span>

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

### <span data-ttu-id="81b69-118">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="81b69-118">-MoveCollectionName</span></span>
<span data-ttu-id="81b69-119">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="81b69-119">The Move Collection Name.</span></span>

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

### <span data-ttu-id="81b69-120">-Orderby</span><span class="sxs-lookup"><span data-stu-id="81b69-120">-Orderby</span></span>
<span data-ttu-id="81b69-121">Ordine OData in base all'opzione della query.</span><span class="sxs-lookup"><span data-stu-id="81b69-121">OData order by query option.</span></span>
<span data-ttu-id="81b69-122">Ad esempio, è possibile usare $orderby=Count desc.</span><span class="sxs-lookup"><span data-stu-id="81b69-122">For example, you can use $orderby=Count desc.</span></span>

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

### <span data-ttu-id="81b69-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81b69-123">-ResourceGroupName</span></span>
<span data-ttu-id="81b69-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="81b69-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="81b69-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81b69-125">-SubscriptionId</span></span>
<span data-ttu-id="81b69-126">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="81b69-126">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b69-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b69-127">CommonParameters</span></span>
<span data-ttu-id="81b69-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b69-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b69-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="81b69-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b69-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="81b69-130">INPUTS</span></span>

## <span data-ttu-id="81b69-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81b69-131">OUTPUTS</span></span>

### <span data-ttu-id="81b69-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolved Miningy</span><span class="sxs-lookup"><span data-stu-id="81b69-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span></span>

## <span data-ttu-id="81b69-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="81b69-133">NOTES</span></span>

<span data-ttu-id="81b69-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="81b69-134">ALIASES</span></span>

## <span data-ttu-id="81b69-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81b69-135">RELATED LINKS</span></span>

