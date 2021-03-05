---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 317614d67138b185dc58334d398bb368fc85911e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999886"
---
# <span data-ttu-id="580b4-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="580b4-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="580b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="580b4-102">SYNOPSIS</span></span>
<span data-ttu-id="580b4-103">Crea o aggiorna una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="580b4-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="580b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="580b4-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="580b4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="580b4-105">DESCRIPTION</span></span>
<span data-ttu-id="580b4-106">Crea o aggiorna una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="580b4-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="580b4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="580b4-107">EXAMPLES</span></span>

### <span data-ttu-id="580b4-108">Esempio 1: Creare una nuova raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="580b4-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name "PS-centralus-westcentralus-demoRMS"  -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceRegion "centralus" -TargetRegion "westcentralus" -Location "centraluseuap" -IdentityType "SystemAssigned"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"0200d92f-0000-3300-0000-6021e9ec0000" centraluseuap PS-centralus-westcentralus-demoRMs Microsoft.Migrate/moveCollections
```

<span data-ttu-id="580b4-109">Creare una nuova raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="580b4-109">Create a new Move Collection.</span></span>

## <span data-ttu-id="580b4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="580b4-110">PARAMETERS</span></span>

### <span data-ttu-id="580b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="580b4-111">-DefaultProfile</span></span>
<span data-ttu-id="580b4-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="580b4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="580b4-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="580b4-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="580b4-114">Ottiene o imposta l'ID entità.</span><span class="sxs-lookup"><span data-stu-id="580b4-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="580b4-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="580b4-115">-IdentityTenantId</span></span>
<span data-ttu-id="580b4-116">Ottiene o imposta l'ID tenant.</span><span class="sxs-lookup"><span data-stu-id="580b4-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="580b4-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="580b4-117">-IdentityType</span></span>
<span data-ttu-id="580b4-118">Tipo di identità usato per il servizio di spostamento delle risorse.</span><span class="sxs-lookup"><span data-stu-id="580b4-118">The type of identity used for the resource mover service.</span></span>

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

### <span data-ttu-id="580b4-119">-Location</span><span class="sxs-lookup"><span data-stu-id="580b4-119">-Location</span></span>
<span data-ttu-id="580b4-120">Posizione geografica in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="580b4-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="580b4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="580b4-121">-Name</span></span>
<span data-ttu-id="580b4-122">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="580b4-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="580b4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="580b4-123">-ResourceGroupName</span></span>
<span data-ttu-id="580b4-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="580b4-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="580b4-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="580b4-125">-SourceRegion</span></span>
<span data-ttu-id="580b4-126">Ottiene o imposta l'area di origine.</span><span class="sxs-lookup"><span data-stu-id="580b4-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="580b4-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="580b4-127">-SubscriptionId</span></span>
<span data-ttu-id="580b4-128">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="580b4-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="580b4-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="580b4-129">-Tag</span></span>
<span data-ttu-id="580b4-130">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="580b4-130">Resource tags.</span></span>

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

### <span data-ttu-id="580b4-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="580b4-131">-TargetRegion</span></span>
<span data-ttu-id="580b4-132">Ottiene o imposta l'area di destinazione.</span><span class="sxs-lookup"><span data-stu-id="580b4-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="580b4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="580b4-133">-Confirm</span></span>
<span data-ttu-id="580b4-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="580b4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="580b4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="580b4-135">-WhatIf</span></span>
<span data-ttu-id="580b4-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="580b4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="580b4-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="580b4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="580b4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="580b4-138">CommonParameters</span></span>
<span data-ttu-id="580b4-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="580b4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="580b4-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="580b4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="580b4-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="580b4-141">INPUTS</span></span>

## <span data-ttu-id="580b4-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="580b4-142">OUTPUTS</span></span>

### <span data-ttu-id="580b4-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="580b4-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="580b4-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="580b4-144">NOTES</span></span>

<span data-ttu-id="580b4-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="580b4-145">ALIASES</span></span>

## <span data-ttu-id="580b4-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="580b4-146">RELATED LINKS</span></span>

