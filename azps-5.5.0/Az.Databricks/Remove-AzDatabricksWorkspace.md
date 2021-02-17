---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180814"
---
# <span data-ttu-id="85046-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="85046-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="85046-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85046-102">SYNOPSIS</span></span>
<span data-ttu-id="85046-103">Elimina l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="85046-103">Deletes the workspace.</span></span>

## <span data-ttu-id="85046-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85046-104">SYNTAX</span></span>

### <span data-ttu-id="85046-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85046-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="85046-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="85046-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="85046-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="85046-107">DESCRIPTION</span></span>
<span data-ttu-id="85046-108">Elimina l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="85046-108">Deletes the workspace.</span></span>

## <span data-ttu-id="85046-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85046-109">EXAMPLES</span></span>

### <span data-ttu-id="85046-110">Esempio 1: Rimuovere un'area di lavoro Databricks</span><span class="sxs-lookup"><span data-stu-id="85046-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="85046-111">Questo comando rimuove un'area di lavoro Databricks da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85046-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="85046-112">Esempio 2: Rimuovere un'area di lavoro Databricks in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="85046-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="85046-113">Questo comando rimuove un'area di lavoro Databricks da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85046-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="85046-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85046-114">PARAMETERS</span></span>

### <span data-ttu-id="85046-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85046-115">-AsJob</span></span>
<span data-ttu-id="85046-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="85046-116">Run the command as a job</span></span>

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

### <span data-ttu-id="85046-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85046-117">-DefaultProfile</span></span>
<span data-ttu-id="85046-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85046-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85046-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85046-119">-InputObject</span></span>
<span data-ttu-id="85046-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="85046-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85046-121">-Name</span><span class="sxs-lookup"><span data-stu-id="85046-121">-Name</span></span>
<span data-ttu-id="85046-122">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="85046-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85046-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="85046-123">-NoWait</span></span>
<span data-ttu-id="85046-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="85046-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="85046-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85046-125">-PassThru</span></span>
<span data-ttu-id="85046-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="85046-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="85046-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85046-127">-ResourceGroupName</span></span>
<span data-ttu-id="85046-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85046-128">The name of the resource group.</span></span>
<span data-ttu-id="85046-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="85046-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85046-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85046-130">-SubscriptionId</span></span>
<span data-ttu-id="85046-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="85046-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85046-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85046-132">-Confirm</span></span>
<span data-ttu-id="85046-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85046-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85046-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85046-134">-WhatIf</span></span>
<span data-ttu-id="85046-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85046-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85046-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85046-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85046-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85046-137">CommonParameters</span></span>
<span data-ttu-id="85046-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85046-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85046-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85046-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85046-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="85046-140">INPUTS</span></span>

### <span data-ttu-id="85046-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="85046-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="85046-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85046-142">OUTPUTS</span></span>

### <span data-ttu-id="85046-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85046-143">System.Boolean</span></span>

## <span data-ttu-id="85046-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="85046-144">NOTES</span></span>

<span data-ttu-id="85046-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="85046-145">ALIASES</span></span>

<span data-ttu-id="85046-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="85046-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="85046-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="85046-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85046-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="85046-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="85046-149">INPUTOBJECT <IDatabricksIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="85046-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="85046-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="85046-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="85046-151">`[PeeringName <String>]`: nome del peering vNet dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="85046-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="85046-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85046-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="85046-153">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="85046-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="85046-154">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="85046-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="85046-155">`[WorkspaceName <String>]`: nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="85046-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="85046-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85046-156">RELATED LINKS</span></span>

