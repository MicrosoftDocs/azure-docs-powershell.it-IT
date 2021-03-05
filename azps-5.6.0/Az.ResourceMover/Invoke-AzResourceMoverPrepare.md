---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 95ad5dad6bd375595a452881e1dfe72a9f314207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999934"
---
# <span data-ttu-id="e6a62-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="e6a62-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="e6a62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6a62-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a62-103">Avvia la preparazione per il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="e6a62-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="e6a62-104">L'operazione di preparazione si trova su moveResources che si trova in moveState 'PreparePending' o 'PrepareFailed', al completamento di moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="e6a62-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="e6a62-105">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="e6a62-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="e6a62-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6a62-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e6a62-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6a62-107">DESCRIPTION</span></span>
<span data-ttu-id="e6a62-108">Avvia la preparazione per il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="e6a62-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="e6a62-109">L'operazione di preparazione si trova su moveResources che si trova in moveState 'PreparePending' o 'PrepareFailed', al completamento di moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="e6a62-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="e6a62-110">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="e6a62-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="e6a62-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6a62-111">EXAMPLES</span></span>

### <span data-ttu-id="e6a62-112">Esempio 1: Convalidare le dipendenze prima di preparare le risorse.</span><span class="sxs-lookup"><span data-stu-id="e6a62-112">Example 1: Validate the dependecies before prepare of the resources.</span></span> <span data-ttu-id="e6a62-113">Ottenere le risorse dipendenti necessarie che devono essere preparate.</span><span class="sxs-lookup"><span data-stu-id="e6a62-113">Get the required dependent resources that also need to be prepared.</span></span>
```powershell
PS C:\> $resp = Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 2/9/2021 9:04:15 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/PS-centralus-westcentralus-demoRMS/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 9:04:14 AM
Status         : Failed

PS C:> $resp.Code
MoveCollectionMissingRequiredDependentResources

PS C:> $resp.AdditionalInfo[0].InfoMoveResource

SourceId                                                                                                                                  
--------                                                                                                                                  
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg

```

<span data-ttu-id="e6a62-114">Verificare le dipendenze prima di preparare le risorse.</span><span class="sxs-lookup"><span data-stu-id="e6a62-114">Validate the dependecies before prepare of the resources.</span></span>
<span data-ttu-id="e6a62-115">Ottenere le risorse dipendenti necessarie che devono essere preparate.</span><span class="sxs-lookup"><span data-stu-id="e6a62-115">Get the required dependent resources that also need to be prepared.</span></span>

### <span data-ttu-id="e6a62-116">Esempio 2: Iniziare a preparare il set di risorse nella raccolta di spostamento usando "MoveResource Name" come input.</span><span class="sxs-lookup"><span data-stu-id="e6a62-116">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM','psdemovm111', 'PSDemoRM-vnet','PSDemoVM-nsg')

AAdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/9/2021 11:25:13 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/49e4429
                 4-24ac-4eac-93da-e7e1c815554d
Message        : 
Name           : 49e44294-24ac-4eac-93da-e7e1c815554d
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 10:55:53 AM
Status         : Succeeded
```

<span data-ttu-id="e6a62-117">Iniziare a preparare l'insieme di risorse nella raccolta di spostamento usando "MoveResource Name" come input.</span><span class="sxs-lookup"><span data-stu-id="e6a62-117">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="e6a62-118">Esempio 3: Iniziare a preparare il set di risorse nella raccolta di spostamento usando "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="e6a62-118">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRMS/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 2/9/2021 11:09:30 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRMS/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 11:05:27 AM
Status         : Succeeded

```

<span data-ttu-id="e6a62-119">Iniziare a preparare l'insieme di risorse nella raccolta di spostamento usando "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="e6a62-119">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="e6a62-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6a62-120">PARAMETERS</span></span>

### <span data-ttu-id="e6a62-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6a62-121">-AsJob</span></span>
<span data-ttu-id="e6a62-122">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e6a62-122">Run the command as a job</span></span>

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

### <span data-ttu-id="e6a62-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a62-123">-DefaultProfile</span></span>
<span data-ttu-id="e6a62-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a62-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6a62-125">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="e6a62-125">-MoveCollectionName</span></span>
<span data-ttu-id="e6a62-126">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="e6a62-126">The Move Collection Name.</span></span>

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

### <span data-ttu-id="e6a62-127">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="e6a62-127">-MoveResource</span></span>
<span data-ttu-id="e6a62-128">Ottiene o imposta l'elenco di ID della risorsa, per impostazione predefinita accetta id della risorsa di spostamento, a meno che il tipo di input non venga spostato tramite la proprietà moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="e6a62-128">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a62-129">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="e6a62-129">-MoveResourceInputType</span></span>
<span data-ttu-id="e6a62-130">Definisce il tipo di input della risorsa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="e6a62-130">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a62-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e6a62-131">-NoWait</span></span>
<span data-ttu-id="e6a62-132">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e6a62-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e6a62-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a62-133">-ResourceGroupName</span></span>
<span data-ttu-id="e6a62-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e6a62-134">The Resource Group Name.</span></span>

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

### <span data-ttu-id="e6a62-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6a62-135">-SubscriptionId</span></span>
<span data-ttu-id="e6a62-136">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e6a62-136">The Subscription ID.</span></span>

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

### <span data-ttu-id="e6a62-137">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="e6a62-137">-ValidateOnly</span></span>
<span data-ttu-id="e6a62-138">Ottiene o imposta un valore che indica se l'operazione deve eseguire solo i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="e6a62-138">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="e6a62-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6a62-139">-Confirm</span></span>
<span data-ttu-id="e6a62-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6a62-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a62-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a62-141">-WhatIf</span></span>
<span data-ttu-id="e6a62-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6a62-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6a62-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6a62-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a62-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a62-144">CommonParameters</span></span>
<span data-ttu-id="e6a62-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a62-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a62-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6a62-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a62-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6a62-147">INPUTS</span></span>

## <span data-ttu-id="e6a62-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6a62-148">OUTPUTS</span></span>

### <span data-ttu-id="e6a62-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="e6a62-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="e6a62-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6a62-150">NOTES</span></span>

<span data-ttu-id="e6a62-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e6a62-151">ALIASES</span></span>

## <span data-ttu-id="e6a62-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6a62-152">RELATED LINKS</span></span>

