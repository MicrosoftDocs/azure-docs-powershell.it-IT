---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: a10ac77515b225c5e5ef06335f9cee1e99ecd3b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000045"
---
# <span data-ttu-id="975ff-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="975ff-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="975ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="975ff-102">SYNOPSIS</span></span>
<span data-ttu-id="975ff-103">Ottiene la raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="975ff-103">Gets the move collection.</span></span>

## <span data-ttu-id="975ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="975ff-104">SYNTAX</span></span>

### <span data-ttu-id="975ff-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="975ff-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="975ff-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="975ff-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="975ff-107">Elenco1</span><span class="sxs-lookup"><span data-stu-id="975ff-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="975ff-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="975ff-108">DESCRIPTION</span></span>
<span data-ttu-id="975ff-109">Ottiene la raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="975ff-109">Gets the move collection.</span></span>

## <span data-ttu-id="975ff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="975ff-110">EXAMPLES</span></span>

### <span data-ttu-id="975ff-111">Esempio 1: Ottenere i dettagli di tutte le raccolte di spostamento nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="975ff-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"270119e0-0000-0c00-0000-5f5c94940000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"39015ed4-0000-0c00-0000-5f5ce2760000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections
"1000b505-0000-0c00-0000-5f69db6e0000" centraluseuap MoveCollection-cus-eus-ccy         Microsoft.Migrate/moveCollections


```

<span data-ttu-id="975ff-112">Ottenere informazioni dettagliate su tutte le raccolte di spostamento dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="975ff-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="975ff-113">Esempio 2: Ottenere i dettagli della raccolta di spostamento con un nome di raccolta di spostamento specificato nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="975ff-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PS-centralus-westcentralus-demoRMS"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="975ff-114">Ottenere informazioni dettagliate sulla raccolta di spostamento con un nome di raccolta di spostamento specificato nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="975ff-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="975ff-115">Esempio 3: Ottenere i dettagli della raccolta di spostamento con il nome di un gruppo di risorse specificato nella sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="975ff-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"4e02b0a9-0000-0c00-0000-5fd101cc0000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="975ff-116">Informazioni dettagliate sulla raccolta di spostamento con il nome di un gruppo di risorse specificato nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="975ff-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="975ff-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="975ff-117">PARAMETERS</span></span>

### <span data-ttu-id="975ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975ff-118">-DefaultProfile</span></span>
<span data-ttu-id="975ff-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="975ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="975ff-120">-Name</span><span class="sxs-lookup"><span data-stu-id="975ff-120">-Name</span></span>
<span data-ttu-id="975ff-121">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="975ff-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975ff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="975ff-122">-ResourceGroupName</span></span>
<span data-ttu-id="975ff-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="975ff-123">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975ff-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="975ff-124">-SubscriptionId</span></span>
<span data-ttu-id="975ff-125">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="975ff-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="975ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975ff-126">CommonParameters</span></span>
<span data-ttu-id="975ff-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="975ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975ff-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="975ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975ff-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="975ff-129">INPUTS</span></span>

## <span data-ttu-id="975ff-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="975ff-130">OUTPUTS</span></span>

### <span data-ttu-id="975ff-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="975ff-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="975ff-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="975ff-132">NOTES</span></span>

<span data-ttu-id="975ff-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="975ff-133">ALIASES</span></span>

## <span data-ttu-id="975ff-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="975ff-134">RELATED LINKS</span></span>

