---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302539"
---
# <span data-ttu-id="72a86-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="72a86-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="72a86-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72a86-102">SYNOPSIS</span></span>
<span data-ttu-id="72a86-103">Ottiene la raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="72a86-103">Gets the move collection.</span></span>

## <span data-ttu-id="72a86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72a86-104">SYNTAX</span></span>

### <span data-ttu-id="72a86-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72a86-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="72a86-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="72a86-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72a86-107">List1</span><span class="sxs-lookup"><span data-stu-id="72a86-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="72a86-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72a86-108">DESCRIPTION</span></span>
<span data-ttu-id="72a86-109">Ottiene la raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="72a86-109">Gets the move collection.</span></span>

## <span data-ttu-id="72a86-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72a86-110">EXAMPLES</span></span>

### <span data-ttu-id="72a86-111">Esempio 1: ottenere informazioni dettagliate su tutte le raccolte di mosse nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="72a86-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="72a86-112">Ottenere informazioni dettagliate su tutte le raccolte di mosse nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="72a86-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="72a86-113">Esempio 2: ottenere informazioni dettagliate sulla raccolta di mosse con un nome di raccolta di mosse specificato nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="72a86-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="72a86-114">Ottenere i dettagli della raccolta di mosse con un nome di raccolta di mosse specificato nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="72a86-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="72a86-115">Esempio 3: ottenere informazioni dettagliate sulla raccolta di mosse con il nome di un gruppo di risorse specificato nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="72a86-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="72a86-116">Ottenere informazioni dettagliate sulla raccolta di mosse con il nome di un gruppo di risorse specificato nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="72a86-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="72a86-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72a86-117">PARAMETERS</span></span>

### <span data-ttu-id="72a86-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a86-118">-DefaultProfile</span></span>
<span data-ttu-id="72a86-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72a86-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72a86-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="72a86-120">-Name</span></span>
<span data-ttu-id="72a86-121">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="72a86-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="72a86-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72a86-122">-ResourceGroupName</span></span>
<span data-ttu-id="72a86-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72a86-123">The Resource Group Name.</span></span>

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

### <span data-ttu-id="72a86-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72a86-124">-SubscriptionId</span></span>
<span data-ttu-id="72a86-125">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="72a86-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="72a86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a86-126">CommonParameters</span></span>
<span data-ttu-id="72a86-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72a86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a86-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72a86-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a86-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72a86-129">INPUTS</span></span>

## <span data-ttu-id="72a86-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72a86-130">OUTPUTS</span></span>

### <span data-ttu-id="72a86-131">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="72a86-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="72a86-132">Note</span><span class="sxs-lookup"><span data-stu-id="72a86-132">NOTES</span></span>

<span data-ttu-id="72a86-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="72a86-133">ALIASES</span></span>

## <span data-ttu-id="72a86-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72a86-134">RELATED LINKS</span></span>

