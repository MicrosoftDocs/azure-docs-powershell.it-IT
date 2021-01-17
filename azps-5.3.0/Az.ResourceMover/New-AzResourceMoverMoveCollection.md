---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474330"
---
# <span data-ttu-id="a4dec-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="a4dec-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="a4dec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4dec-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dec-103">Crea o aggiorna una raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="a4dec-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="a4dec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4dec-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a4dec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4dec-105">DESCRIPTION</span></span>
<span data-ttu-id="a4dec-106">Crea o aggiorna una raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="a4dec-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="a4dec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4dec-107">EXAMPLES</span></span>

### <span data-ttu-id="a4dec-108">Esempio 1: creare una nuova raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="a4dec-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="a4dec-109">Creare una nuova raccolta di mosse all'interno di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a4dec-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="a4dec-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4dec-110">PARAMETERS</span></span>

### <span data-ttu-id="a4dec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4dec-111">-DefaultProfile</span></span>
<span data-ttu-id="a4dec-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4dec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4dec-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="a4dec-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="a4dec-114">Ottiene o imposta l'ID principale.</span><span class="sxs-lookup"><span data-stu-id="a4dec-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="a4dec-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="a4dec-115">-IdentityTenantId</span></span>
<span data-ttu-id="a4dec-116">Ottiene o imposta l'ID tenant.</span><span class="sxs-lookup"><span data-stu-id="a4dec-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="a4dec-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a4dec-117">-IdentityType</span></span>
<span data-ttu-id="a4dec-118">Il tipo di identità utilizzata per il servizio di trasferimento dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="a4dec-118">The type of identity used for the region move service.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.ResourceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4dec-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a4dec-119">-Location</span></span>
<span data-ttu-id="a4dec-120">Posizione geografica in cui vive la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a4dec-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="a4dec-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4dec-121">-Name</span></span>
<span data-ttu-id="a4dec-122">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="a4dec-122">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4dec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4dec-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4dec-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4dec-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="a4dec-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="a4dec-125">-SourceRegion</span></span>
<span data-ttu-id="a4dec-126">Ottiene o imposta l'area di origine.</span><span class="sxs-lookup"><span data-stu-id="a4dec-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="a4dec-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4dec-127">-SubscriptionId</span></span>
<span data-ttu-id="a4dec-128">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a4dec-128">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4dec-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="a4dec-129">-Tag</span></span>
<span data-ttu-id="a4dec-130">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a4dec-130">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4dec-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="a4dec-131">-TargetRegion</span></span>
<span data-ttu-id="a4dec-132">Ottiene o imposta l'area di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a4dec-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="a4dec-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4dec-133">-Confirm</span></span>
<span data-ttu-id="a4dec-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4dec-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4dec-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4dec-135">-WhatIf</span></span>
<span data-ttu-id="a4dec-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4dec-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4dec-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4dec-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4dec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dec-138">CommonParameters</span></span>
<span data-ttu-id="a4dec-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4dec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dec-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4dec-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dec-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4dec-141">INPUTS</span></span>

## <span data-ttu-id="a4dec-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4dec-142">OUTPUTS</span></span>

### <span data-ttu-id="a4dec-143">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="a4dec-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="a4dec-144">Note</span><span class="sxs-lookup"><span data-stu-id="a4dec-144">NOTES</span></span>

<span data-ttu-id="a4dec-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a4dec-145">ALIASES</span></span>

## <span data-ttu-id="a4dec-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4dec-146">RELATED LINKS</span></span>

