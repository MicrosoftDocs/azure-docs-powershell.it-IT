---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365298"
---
# <span data-ttu-id="2b324-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="2b324-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="2b324-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b324-102">SYNOPSIS</span></span>
<span data-ttu-id="2b324-103">Ottiene un elenco di dipendenze non risolte.</span><span class="sxs-lookup"><span data-stu-id="2b324-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="2b324-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b324-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2b324-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b324-105">DESCRIPTION</span></span>
<span data-ttu-id="2b324-106">Ottiene un elenco di dipendenze non risolte.</span><span class="sxs-lookup"><span data-stu-id="2b324-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="2b324-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b324-107">EXAMPLES</span></span>

### <span data-ttu-id="2b324-108">Esempio 1: ottenere l'elenco delle risorse dipendenti non risolte</span><span class="sxs-lookup"><span data-stu-id="2b324-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="2b324-109">Ottenere l'elenco delle risorse dipendenti non risolte per una raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="2b324-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="2b324-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b324-110">PARAMETERS</span></span>

### <span data-ttu-id="2b324-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b324-111">-DefaultProfile</span></span>
<span data-ttu-id="2b324-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b324-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b324-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="2b324-113">-MoveCollectionName</span></span>
<span data-ttu-id="2b324-114">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="2b324-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="2b324-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b324-115">-ResourceGroupName</span></span>
<span data-ttu-id="2b324-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b324-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="2b324-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b324-117">-SubscriptionId</span></span>
<span data-ttu-id="2b324-118">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2b324-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="2b324-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b324-119">CommonParameters</span></span>
<span data-ttu-id="2b324-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b324-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b324-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b324-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b324-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b324-122">INPUTS</span></span>

## <span data-ttu-id="2b324-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b324-123">OUTPUTS</span></span>

### <span data-ttu-id="2b324-124">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="2b324-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="2b324-125">Note</span><span class="sxs-lookup"><span data-stu-id="2b324-125">NOTES</span></span>

<span data-ttu-id="2b324-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2b324-126">ALIASES</span></span>

## <span data-ttu-id="2b324-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b324-127">RELATED LINKS</span></span>

