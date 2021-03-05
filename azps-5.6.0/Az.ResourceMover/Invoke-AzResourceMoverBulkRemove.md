---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverbulkremove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
ms.openlocfilehash: f9815c32526a5ce462a50ec167771d30bc840b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999982"
---
# <span data-ttu-id="aa43e-101">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="aa43e-101">Invoke-AzResourceMoverBulkRemove</span></span>

## <span data-ttu-id="aa43e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa43e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa43e-103">Rimuove il set di risorse di spostamento incluse nel corpo della richiesta dalla raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="aa43e-103">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="aa43e-104">La saturazione viene eseguita dal servizio.</span><span class="sxs-lookup"><span data-stu-id="aa43e-104">The orchestration is done by service.</span></span>
<span data-ttu-id="aa43e-105">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="aa43e-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="aa43e-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa43e-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverBulkRemove -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-MoveResource <String[]>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aa43e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aa43e-107">DESCRIPTION</span></span>
<span data-ttu-id="aa43e-108">Rimuove il set di risorse di spostamento incluse nel corpo della richiesta dalla raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="aa43e-108">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="aa43e-109">La saturazione viene eseguita dal servizio.</span><span class="sxs-lookup"><span data-stu-id="aa43e-109">The orchestration is done by service.</span></span>
<span data-ttu-id="aa43e-110">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="aa43e-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="aa43e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa43e-111">EXAMPLES</span></span>

### <span data-ttu-id="aa43e-112">Esempio 1: Convalidare le dipendenze prima di rimuovere lo spostamento delle risorse dalla raccolta di spostamento</span><span class="sxs-lookup"><span data-stu-id="aa43e-112">Example 1: Validate the dependecies before remove of the Move Resources from Move Collection</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:52:28 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Message        : 
Name           : b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:52:28 PM
Status         : Succeeded

```

<span data-ttu-id="aa43e-113">Verificare le dipendenze prima di rimuovere le risorse di spostamento dalla raccolta spostata.</span><span class="sxs-lookup"><span data-stu-id="aa43e-113">Validate the dependecies before remove of the move resources from Move Collection.</span></span>

### <span data-ttu-id="aa43e-114">Esempio 2: Rimuovere la risorsa di spostamento dalla raccolta di spostamento usando "MoveResource Name" come input</span><span class="sxs-lookup"><span data-stu-id="aa43e-114">Example 2: Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:58:10 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d4827071-b797-45c5-b88c-00ddd7818d42
Message        : 
Name           : d4827071-b797-45c5-b88c-00ddd7818d42
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:57:08 PM
Status         : Succeeded
```

<span data-ttu-id="aa43e-115">Rimuovere la risorsa di spostamento dalla raccolta di spostamento usando "MoveResource Name" come input</span><span class="sxs-lookup"><span data-stu-id="aa43e-115">Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="aa43e-116">Esempio 3: Rimuovere la risorsa di spostamento dalla raccolta con "SourceARMID" come input</span><span class="sxs-lookup"><span data-stu-id="aa43e-116">Example 3: Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:05:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/7b6904e2-fc3f-400d-b248-8908fcb282fb
Message        : 
Name           : 7b6904e2-fc3f-400d-b248-8908fcb282fb
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:05:00 PM
Status         : Succeeded
```

<span data-ttu-id="aa43e-117">Rimuovere la risorsa di spostamento dalla raccolta di spostamento usando "SourceARMID" come input</span><span class="sxs-lookup"><span data-stu-id="aa43e-117">Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="aa43e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa43e-118">PARAMETERS</span></span>

### <span data-ttu-id="aa43e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa43e-119">-AsJob</span></span>
<span data-ttu-id="aa43e-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="aa43e-120">Run the command as a job</span></span>

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

### <span data-ttu-id="aa43e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa43e-121">-DefaultProfile</span></span>
<span data-ttu-id="aa43e-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa43e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa43e-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="aa43e-123">-MoveCollectionName</span></span>
<span data-ttu-id="aa43e-124">.</span><span class="sxs-lookup"><span data-stu-id="aa43e-124">.</span></span>

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

### <span data-ttu-id="aa43e-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="aa43e-125">-MoveResource</span></span>
<span data-ttu-id="aa43e-126">Ottiene o imposta l'elenco di ID della risorsa, per impostazione predefinita accetta id della risorsa di spostamento, a meno che il tipo di input non venga spostato tramite la proprietà moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="aa43e-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa43e-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="aa43e-127">-MoveResourceInputType</span></span>
<span data-ttu-id="aa43e-128">Definisce il tipo di input della risorsa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="aa43e-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="aa43e-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aa43e-129">-NoWait</span></span>
<span data-ttu-id="aa43e-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="aa43e-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aa43e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa43e-131">-ResourceGroupName</span></span>
<span data-ttu-id="aa43e-132">.</span><span class="sxs-lookup"><span data-stu-id="aa43e-132">.</span></span>

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

### <span data-ttu-id="aa43e-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa43e-133">-SubscriptionId</span></span>
<span data-ttu-id="aa43e-134">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="aa43e-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="aa43e-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="aa43e-135">-ValidateOnly</span></span>
<span data-ttu-id="aa43e-136">Ottiene o imposta un valore che indica se l'operazione deve eseguire solo i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="aa43e-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="aa43e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa43e-137">-Confirm</span></span>
<span data-ttu-id="aa43e-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa43e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa43e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa43e-139">-WhatIf</span></span>
<span data-ttu-id="aa43e-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa43e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa43e-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa43e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa43e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa43e-142">CommonParameters</span></span>
<span data-ttu-id="aa43e-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa43e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa43e-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa43e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa43e-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="aa43e-145">INPUTS</span></span>

## <span data-ttu-id="aa43e-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa43e-146">OUTPUTS</span></span>

### <span data-ttu-id="aa43e-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="aa43e-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="aa43e-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="aa43e-148">NOTES</span></span>

<span data-ttu-id="aa43e-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="aa43e-149">ALIASES</span></span>

## <span data-ttu-id="aa43e-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa43e-150">RELATED LINKS</span></span>

