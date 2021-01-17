---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479291"
---
# <span data-ttu-id="3b450-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="3b450-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="3b450-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b450-102">SYNOPSIS</span></span>
<span data-ttu-id="3b450-103">Elimina l'area di lavoro vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="3b450-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="3b450-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b450-104">SYNTAX</span></span>

### <span data-ttu-id="3b450-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b450-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3b450-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3b450-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3b450-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b450-107">DESCRIPTION</span></span>
<span data-ttu-id="3b450-108">Elimina l'area di lavoro vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="3b450-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="3b450-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b450-109">EXAMPLES</span></span>

### <span data-ttu-id="3b450-110">Esempio 1: rimuovere un peering VNET di databricks per nome</span><span class="sxs-lookup"><span data-stu-id="3b450-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="3b450-111">Questo comando rimuove un peering VNET di databricks per nome</span><span class="sxs-lookup"><span data-stu-id="3b450-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="3b450-112">Esempio 2: rimuovere un peering VNET di databricks per oggetto</span><span class="sxs-lookup"><span data-stu-id="3b450-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="3b450-113">Questo comando rimuove un peering VNET di databricks per oggetto</span><span class="sxs-lookup"><span data-stu-id="3b450-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="3b450-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b450-114">PARAMETERS</span></span>

### <span data-ttu-id="3b450-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b450-115">-AsJob</span></span>
<span data-ttu-id="3b450-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="3b450-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3b450-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b450-117">-DefaultProfile</span></span>
<span data-ttu-id="3b450-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b450-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b450-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b450-119">-InputObject</span></span>
<span data-ttu-id="3b450-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3b450-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3b450-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b450-121">-Name</span></span>
<span data-ttu-id="3b450-122">Nome dell'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="3b450-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="3b450-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="3b450-123">-NoWait</span></span>
<span data-ttu-id="3b450-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="3b450-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3b450-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b450-125">-PassThru</span></span>
<span data-ttu-id="3b450-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="3b450-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3b450-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b450-127">-ResourceGroupName</span></span>
<span data-ttu-id="3b450-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b450-128">The name of the resource group.</span></span>
<span data-ttu-id="3b450-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3b450-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3b450-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b450-130">-SubscriptionId</span></span>
<span data-ttu-id="3b450-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3b450-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3b450-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3b450-132">-WorkspaceName</span></span>
<span data-ttu-id="3b450-133">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3b450-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="3b450-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b450-134">-Confirm</span></span>
<span data-ttu-id="3b450-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b450-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b450-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b450-136">-WhatIf</span></span>
<span data-ttu-id="3b450-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b450-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b450-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b450-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b450-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b450-139">CommonParameters</span></span>
<span data-ttu-id="3b450-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b450-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b450-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b450-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b450-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b450-142">INPUTS</span></span>

### <span data-ttu-id="3b450-143">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="3b450-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="3b450-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b450-144">OUTPUTS</span></span>

### <span data-ttu-id="3b450-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b450-145">System.Boolean</span></span>

## <span data-ttu-id="3b450-146">Note</span><span class="sxs-lookup"><span data-stu-id="3b450-146">NOTES</span></span>

<span data-ttu-id="3b450-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3b450-147">ALIASES</span></span>

<span data-ttu-id="3b450-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b450-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b450-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3b450-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b450-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b450-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b450-151">INPUTOBJECT <IDatabricksIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="3b450-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b450-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="3b450-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b450-153">`[PeeringName <String>]`: Nome dell'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="3b450-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="3b450-154">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b450-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3b450-155">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3b450-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="3b450-156">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3b450-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3b450-157">`[WorkspaceName <String>]`: Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3b450-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="3b450-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b450-158">RELATED LINKS</span></span>

