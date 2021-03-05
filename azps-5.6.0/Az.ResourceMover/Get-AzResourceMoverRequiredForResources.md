---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverrequiredforresources
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
ms.openlocfilehash: 9aa09de52a6b731fbf57b309fb605c0ba07325da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000013"
---
# <span data-ttu-id="044e0-101">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="044e0-101">Get-AzResourceMoverRequiredForResources</span></span>

## <span data-ttu-id="044e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="044e0-102">SYNOPSIS</span></span>
<span data-ttu-id="044e0-103">Elenco delle risorse di spostamento per cui è necessaria una risorsa arm.</span><span class="sxs-lookup"><span data-stu-id="044e0-103">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="044e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="044e0-104">SYNTAX</span></span>

```
Get-AzResourceMoverRequiredForResources -MoveCollectionName <String> -ResourceGroupName <String>
 -SourceId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="044e0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="044e0-105">DESCRIPTION</span></span>
<span data-ttu-id="044e0-106">Elenco delle risorse di spostamento per cui è necessaria una risorsa arm.</span><span class="sxs-lookup"><span data-stu-id="044e0-106">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="044e0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="044e0-107">EXAMPLES</span></span>

### <span data-ttu-id="044e0-108">Esempio 1: Ottenere un elenco degli ANNID delle risorse obbligatori che è necessario aggiungere per aggiungere la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="044e0-108">Example 1: Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>
```powershell
PS C:\> Get-AzResourceMoverRequiredForResources -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups"

/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="044e0-109">Ottenere un elenco degli SID delle risorse obbligatori che devono essere aggiunti per aggiungere la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="044e0-109">Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>

## <span data-ttu-id="044e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="044e0-110">PARAMETERS</span></span>

### <span data-ttu-id="044e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044e0-111">-DefaultProfile</span></span>
<span data-ttu-id="044e0-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="044e0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="044e0-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="044e0-113">-MoveCollectionName</span></span>
<span data-ttu-id="044e0-114">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="044e0-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="044e0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="044e0-115">-ResourceGroupName</span></span>
<span data-ttu-id="044e0-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="044e0-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="044e0-117">-SourceId</span><span class="sxs-lookup"><span data-stu-id="044e0-117">-SourceId</span></span>
<span data-ttu-id="044e0-118">SourceId per cui viene richiamata l'api.</span><span class="sxs-lookup"><span data-stu-id="044e0-118">The sourceId for which the api is invoked.</span></span>

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

### <span data-ttu-id="044e0-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="044e0-119">-SubscriptionId</span></span>
<span data-ttu-id="044e0-120">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="044e0-120">The Subscription ID.</span></span>

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

### <span data-ttu-id="044e0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044e0-121">CommonParameters</span></span>
<span data-ttu-id="044e0-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="044e0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044e0-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="044e0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044e0-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="044e0-124">INPUTS</span></span>

## <span data-ttu-id="044e0-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="044e0-125">OUTPUTS</span></span>

### <span data-ttu-id="044e0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="044e0-126">System.String</span></span>

## <span data-ttu-id="044e0-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="044e0-127">NOTES</span></span>

<span data-ttu-id="044e0-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="044e0-128">ALIASES</span></span>

## <span data-ttu-id="044e0-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="044e0-129">RELATED LINKS</span></span>

