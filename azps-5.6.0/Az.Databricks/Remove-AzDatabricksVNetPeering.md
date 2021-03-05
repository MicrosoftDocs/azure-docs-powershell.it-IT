---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 986bea9de45ea8a628cea8eda4d8a63ec74d46fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980765"
---
# <span data-ttu-id="bf306-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="bf306-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="bf306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf306-102">SYNOPSIS</span></span>
<span data-ttu-id="bf306-103">Elimina l'area di lavoro vNetApplicationing.</span><span class="sxs-lookup"><span data-stu-id="bf306-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="bf306-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf306-104">SYNTAX</span></span>

### <span data-ttu-id="bf306-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bf306-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bf306-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bf306-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bf306-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bf306-107">DESCRIPTION</span></span>
<span data-ttu-id="bf306-108">Elimina l'area di lavoro vNetApplicationing.</span><span class="sxs-lookup"><span data-stu-id="bf306-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="bf306-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf306-109">EXAMPLES</span></span>

### <span data-ttu-id="bf306-110">Esempio 1: Rimuovere un peering vnet dei databrick in base al nome</span><span class="sxs-lookup"><span data-stu-id="bf306-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="bf306-111">Questo comando rimuove un peering vnet dei databrick in base al nome</span><span class="sxs-lookup"><span data-stu-id="bf306-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="bf306-112">Esempio 2: Rimuovere un peering vnet dei dati in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="bf306-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="bf306-113">Questo comando rimuove un peering vnet dei dati in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="bf306-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="bf306-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf306-114">PARAMETERS</span></span>

### <span data-ttu-id="bf306-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf306-115">-AsJob</span></span>
<span data-ttu-id="bf306-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="bf306-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bf306-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf306-117">-DefaultProfile</span></span>
<span data-ttu-id="bf306-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf306-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf306-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf306-119">-InputObject</span></span>
<span data-ttu-id="bf306-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bf306-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bf306-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bf306-121">-Name</span></span>
<span data-ttu-id="bf306-122">Nome del peering vNet dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bf306-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="bf306-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bf306-123">-NoWait</span></span>
<span data-ttu-id="bf306-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="bf306-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bf306-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf306-125">-PassThru</span></span>
<span data-ttu-id="bf306-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="bf306-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bf306-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf306-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf306-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bf306-128">The name of the resource group.</span></span>
<span data-ttu-id="bf306-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bf306-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bf306-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf306-130">-SubscriptionId</span></span>
<span data-ttu-id="bf306-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bf306-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bf306-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bf306-132">-WorkspaceName</span></span>
<span data-ttu-id="bf306-133">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bf306-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="bf306-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf306-134">-Confirm</span></span>
<span data-ttu-id="bf306-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf306-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf306-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf306-136">-WhatIf</span></span>
<span data-ttu-id="bf306-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf306-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf306-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf306-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf306-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf306-139">CommonParameters</span></span>
<span data-ttu-id="bf306-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf306-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf306-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bf306-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf306-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="bf306-142">INPUTS</span></span>

### <span data-ttu-id="bf306-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="bf306-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="bf306-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf306-144">OUTPUTS</span></span>

### <span data-ttu-id="bf306-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf306-145">System.Boolean</span></span>

## <span data-ttu-id="bf306-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="bf306-146">NOTES</span></span>

<span data-ttu-id="bf306-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bf306-147">ALIASES</span></span>

<span data-ttu-id="bf306-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="bf306-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bf306-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bf306-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bf306-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bf306-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bf306-151">INPUTOBJECT <IDatabricksIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="bf306-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bf306-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="bf306-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bf306-153">`[PeeringName <String>]`: nome del peering vNet dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bf306-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="bf306-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bf306-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bf306-155">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bf306-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="bf306-156">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bf306-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bf306-157">`[WorkspaceName <String>]`: nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bf306-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="bf306-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf306-158">RELATED LINKS</span></span>

