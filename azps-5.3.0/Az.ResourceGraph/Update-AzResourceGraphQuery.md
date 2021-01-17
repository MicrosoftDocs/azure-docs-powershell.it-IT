---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 6ae44183a368babb43a93063518dfbf4f3d15e18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377898"
---
# <span data-ttu-id="10538-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="10538-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="10538-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10538-102">SYNOPSIS</span></span>
<span data-ttu-id="10538-103">Aggiorna una query di grafico già aggiunta.</span><span class="sxs-lookup"><span data-stu-id="10538-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="10538-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10538-104">SYNTAX</span></span>

### <span data-ttu-id="10538-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10538-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="10538-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="10538-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="10538-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10538-107">DESCRIPTION</span></span>
<span data-ttu-id="10538-108">Aggiorna una query di grafico già aggiunta.</span><span class="sxs-lookup"><span data-stu-id="10538-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="10538-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10538-109">EXAMPLES</span></span>

### <span data-ttu-id="10538-110">Esempio 1: aggiornare la query di parametro e contrassegnare per nome</span><span class="sxs-lookup"><span data-stu-id="10538-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="10538-111">Questo comando Aggiorna la query di parametro e contrassegna per nome.</span><span class="sxs-lookup"><span data-stu-id="10538-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="10538-112">Esempio 2: aggiornare il file di parametro per oggetto</span><span class="sxs-lookup"><span data-stu-id="10538-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="10538-113">Questo comando Aggiorna la query di parametro e contrassegna per oggetto.</span><span class="sxs-lookup"><span data-stu-id="10538-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="10538-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10538-114">PARAMETERS</span></span>

### <span data-ttu-id="10538-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10538-115">-DefaultProfile</span></span>
<span data-ttu-id="10538-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10538-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10538-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="10538-117">-Description</span></span>
<span data-ttu-id="10538-118">Descrizione di una query di grafico.</span><span class="sxs-lookup"><span data-stu-id="10538-118">The description of a graph query.</span></span>

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

### <span data-ttu-id="10538-119">-File</span><span class="sxs-lookup"><span data-stu-id="10538-119">-File</span></span>
<span data-ttu-id="10538-120">Il contenuto del file verrà passato al parametro di query.</span><span class="sxs-lookup"><span data-stu-id="10538-120">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="10538-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10538-121">-InputObject</span></span>
<span data-ttu-id="10538-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="10538-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10538-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="10538-123">-Name</span></span>
<span data-ttu-id="10538-124">Il nome della risorsa query del grafico.</span><span class="sxs-lookup"><span data-stu-id="10538-124">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10538-125">-Query</span><span class="sxs-lookup"><span data-stu-id="10538-125">-Query</span></span>
<span data-ttu-id="10538-126">Query KQL che sarà Graph.</span><span class="sxs-lookup"><span data-stu-id="10538-126">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="10538-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10538-127">-ResourceGroupName</span></span>
<span data-ttu-id="10538-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10538-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10538-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10538-129">-SubscriptionId</span></span>
<span data-ttu-id="10538-130">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="10538-130">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10538-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="10538-131">-Tag</span></span>
<span data-ttu-id="10538-132">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="10538-132">Resource tags</span></span>

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

### <span data-ttu-id="10538-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="10538-133">-Confirm</span></span>
<span data-ttu-id="10538-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10538-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10538-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10538-135">-WhatIf</span></span>
<span data-ttu-id="10538-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10538-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10538-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10538-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10538-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10538-138">CommonParameters</span></span>
<span data-ttu-id="10538-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10538-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10538-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10538-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10538-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10538-141">INPUTS</span></span>

### <span data-ttu-id="10538-142">Microsoft. Azure. PowerShell. Cmdlets. ResourceGraph. Models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="10538-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="10538-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10538-143">OUTPUTS</span></span>

### <span data-ttu-id="10538-144">Microsoft. Azure. PowerShell. Cmdlets. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="10538-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="10538-145">Note</span><span class="sxs-lookup"><span data-stu-id="10538-145">NOTES</span></span>

<span data-ttu-id="10538-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="10538-146">ALIASES</span></span>

<span data-ttu-id="10538-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10538-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="10538-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="10538-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10538-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="10538-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="10538-150">INPUTOBJECT <IResourceGraphIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="10538-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="10538-151">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="10538-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="10538-152">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10538-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="10538-153">`[ResourceName <String>]`: Nome della risorsa query del grafico.</span><span class="sxs-lookup"><span data-stu-id="10538-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="10538-154">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="10538-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="10538-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10538-155">RELATED LINKS</span></span>

