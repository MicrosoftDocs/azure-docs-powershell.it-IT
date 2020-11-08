---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189397"
---
# <span data-ttu-id="c2094-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="c2094-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="c2094-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2094-102">SYNOPSIS</span></span>
<span data-ttu-id="c2094-103">Ottiene un elenco di dipendenze non risolte.</span><span class="sxs-lookup"><span data-stu-id="c2094-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="c2094-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2094-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c2094-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2094-105">DESCRIPTION</span></span>
<span data-ttu-id="c2094-106">Ottiene un elenco di dipendenze non risolte.</span><span class="sxs-lookup"><span data-stu-id="c2094-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="c2094-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2094-107">EXAMPLES</span></span>

### <span data-ttu-id="c2094-108">Esempio 1: ottenere l'elenco delle risorse dipendenti non risolte</span><span class="sxs-lookup"><span data-stu-id="c2094-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="c2094-109">Ottenere l'elenco delle risorse dipendenti non risolte per una raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="c2094-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="c2094-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2094-110">PARAMETERS</span></span>

### <span data-ttu-id="c2094-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2094-111">-DefaultProfile</span></span>
<span data-ttu-id="c2094-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2094-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2094-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="c2094-113">-MoveCollectionName</span></span>
<span data-ttu-id="c2094-114">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="c2094-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c2094-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2094-115">-ResourceGroupName</span></span>
<span data-ttu-id="c2094-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2094-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c2094-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2094-117">-SubscriptionId</span></span>
<span data-ttu-id="c2094-118">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c2094-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="c2094-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2094-119">CommonParameters</span></span>
<span data-ttu-id="c2094-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2094-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2094-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2094-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2094-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2094-122">INPUTS</span></span>

## <span data-ttu-id="c2094-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2094-123">OUTPUTS</span></span>

### <span data-ttu-id="c2094-124">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="c2094-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="c2094-125">Note</span><span class="sxs-lookup"><span data-stu-id="c2094-125">NOTES</span></span>

<span data-ttu-id="c2094-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c2094-126">ALIASES</span></span>

## <span data-ttu-id="c2094-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2094-127">RELATED LINKS</span></span>

