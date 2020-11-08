---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189907"
---
# <span data-ttu-id="37c5f-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="37c5f-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="37c5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="37c5f-103">Crea o aggiorna una risorsa di movimento nella raccolta Move.</span><span class="sxs-lookup"><span data-stu-id="37c5f-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="37c5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37c5f-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37c5f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="37c5f-106">Crea o aggiorna una risorsa di movimento nella raccolta Move.</span><span class="sxs-lookup"><span data-stu-id="37c5f-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="37c5f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37c5f-107">EXAMPLES</span></span>

### <span data-ttu-id="37c5f-108">Esempio 1: aggiunta di una risorsa alla raccolta Move.</span><span class="sxs-lookup"><span data-stu-id="37c5f-108">Example 1: Adding a resource to the move collection.</span></span>
```powershell
PS C:\> Add-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM" -SourceId "/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM" -Name PSDemoVM -ResourceSettingResourceType "Microsoft.Compute/virtualMachines" -ResourceSettingTargetResourceName PSDemoVM

Output:

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migr
                                          ate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          : DependencyComputationPending
MoveStatusDetail                        : {}
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       : The dependency computation is not completed for resource - /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resou
                                          rceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM.
                                              Possible Causes: Dependency computation is pending for resource.
                                              Recommended Action: Validate dependencies to compute the dependencies.

MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachi
                                          nes/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type          

```

<span data-ttu-id="37c5f-109">Aggiunta di una risorsa alla raccolta di mosse all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="37c5f-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="37c5f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37c5f-110">PARAMETERS</span></span>

### <span data-ttu-id="37c5f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37c5f-111">-AsJob</span></span>
<span data-ttu-id="37c5f-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="37c5f-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c5f-113">-DefaultProfile</span></span>
<span data-ttu-id="37c5f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37c5f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37c5f-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="37c5f-115">-DependsOnOverride</span></span>
<span data-ttu-id="37c5f-116">Ottiene o imposta l'override delle dipendenze delle risorse di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="37c5f-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="37c5f-117">Per costruire, vedere la sezione Note per le proprietà di DEPENDSONOVERRIDE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="37c5f-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResourceDependencyOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c5f-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="37c5f-118">-ExistingTargetId</span></span>
<span data-ttu-id="37c5f-119">Ottiene o imposta l'ID del braccio di destinazione esistente della risorsa.</span><span class="sxs-lookup"><span data-stu-id="37c5f-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="37c5f-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="37c5f-120">-MoveCollectionName</span></span>
<span data-ttu-id="37c5f-121">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="37c5f-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="37c5f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="37c5f-122">-Name</span></span>
<span data-ttu-id="37c5f-123">Il nome della risorsa di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="37c5f-123">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c5f-124">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="37c5f-124">-NoWait</span></span>
<span data-ttu-id="37c5f-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="37c5f-125">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c5f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c5f-126">-ResourceGroupName</span></span>
<span data-ttu-id="37c5f-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37c5f-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="37c5f-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="37c5f-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="37c5f-129">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="37c5f-129">The resource type.</span></span>
<span data-ttu-id="37c5f-130">Ad esempio, il valore può essere Microsoft. Compute/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="37c5f-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="37c5f-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="37c5f-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="37c5f-132">Ottiene o imposta il nome della risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="37c5f-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="37c5f-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="37c5f-133">-SourceId</span></span>
<span data-ttu-id="37c5f-134">Ottiene o imposta l'ID del braccio di origine della risorsa.</span><span class="sxs-lookup"><span data-stu-id="37c5f-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="37c5f-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="37c5f-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="37c5f-136">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="37c5f-136">The resource type.</span></span>
<span data-ttu-id="37c5f-137">Ad esempio, il valore può essere Microsoft. Compute/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="37c5f-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="37c5f-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="37c5f-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="37c5f-139">Ottiene o imposta il nome della risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="37c5f-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="37c5f-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37c5f-140">-SubscriptionId</span></span>
<span data-ttu-id="37c5f-141">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="37c5f-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="37c5f-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37c5f-142">-Confirm</span></span>
<span data-ttu-id="37c5f-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37c5f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c5f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c5f-144">-WhatIf</span></span>
<span data-ttu-id="37c5f-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37c5f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37c5f-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37c5f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c5f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c5f-147">CommonParameters</span></span>
<span data-ttu-id="37c5f-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c5f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c5f-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37c5f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c5f-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37c5f-150">INPUTS</span></span>

## <span data-ttu-id="37c5f-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37c5f-151">OUTPUTS</span></span>

### <span data-ttu-id="37c5f-152">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IMoveResource</span><span class="sxs-lookup"><span data-stu-id="37c5f-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="37c5f-153">Note</span><span class="sxs-lookup"><span data-stu-id="37c5f-153">NOTES</span></span>

<span data-ttu-id="37c5f-154">ALIAS</span><span class="sxs-lookup"><span data-stu-id="37c5f-154">ALIASES</span></span>

<span data-ttu-id="37c5f-155">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37c5f-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37c5f-156">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="37c5f-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37c5f-157">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37c5f-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37c5f-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride [] >: Ottiene o imposta gli override delle dipendenze della risorsa di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="37c5f-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="37c5f-159">`[Id <String>]`: Ottiene o imposta l'ID ARM della risorsa dipendente.</span><span class="sxs-lookup"><span data-stu-id="37c5f-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="37c5f-160">`[TargetId <String>]`: Ottiene o imposta l'ID ARM della risorsa di MoveResource o dell'ID ARM della risorsa della risorsa dipendente.</span><span class="sxs-lookup"><span data-stu-id="37c5f-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="37c5f-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37c5f-161">RELATED LINKS</span></span>
