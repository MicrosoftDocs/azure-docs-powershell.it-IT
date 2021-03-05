---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 60dcb163e480371fe211651cc929b6335877490b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000094"
---
# <span data-ttu-id="15cdf-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="15cdf-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="15cdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="15cdf-103">Aggiorna una query grafico già aggiunta.</span><span class="sxs-lookup"><span data-stu-id="15cdf-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="15cdf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15cdf-104">SYNTAX</span></span>

### <span data-ttu-id="15cdf-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="15cdf-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="15cdf-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="15cdf-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15cdf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="15cdf-107">DESCRIPTION</span></span>
<span data-ttu-id="15cdf-108">Aggiorna una query grafico già aggiunta.</span><span class="sxs-lookup"><span data-stu-id="15cdf-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="15cdf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15cdf-109">EXAMPLES</span></span>

### <span data-ttu-id="15cdf-110">Esempio 1: Aggiornare la query con parametri e il tag in base al nome</span><span class="sxs-lookup"><span data-stu-id="15cdf-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="15cdf-111">Questo comando aggiorna la query con parametri e il tag in base al nome.</span><span class="sxs-lookup"><span data-stu-id="15cdf-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="15cdf-112">Esempio 2: Aggiornare il file di parametri in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="15cdf-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="15cdf-113">Questo comando aggiorna la query con parametri e il tag in base all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="15cdf-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="15cdf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15cdf-114">PARAMETERS</span></span>

### <span data-ttu-id="15cdf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15cdf-115">-DefaultProfile</span></span>
<span data-ttu-id="15cdf-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15cdf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15cdf-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="15cdf-117">-Description</span></span>
<span data-ttu-id="15cdf-118">Descrizione di una query grafico.</span><span class="sxs-lookup"><span data-stu-id="15cdf-118">The description of a graph query.</span></span>

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

### <span data-ttu-id="15cdf-119">-File</span><span class="sxs-lookup"><span data-stu-id="15cdf-119">-File</span></span>
<span data-ttu-id="15cdf-120">Il contenuto del file verrà passato al parametro della query.</span><span class="sxs-lookup"><span data-stu-id="15cdf-120">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="15cdf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15cdf-121">-InputObject</span></span>
<span data-ttu-id="15cdf-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="15cdf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15cdf-123">-Name</span><span class="sxs-lookup"><span data-stu-id="15cdf-123">-Name</span></span>
<span data-ttu-id="15cdf-124">Nome della risorsa Query grafico.</span><span class="sxs-lookup"><span data-stu-id="15cdf-124">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="15cdf-125">-Query</span><span class="sxs-lookup"><span data-stu-id="15cdf-125">-Query</span></span>
<span data-ttu-id="15cdf-126">Query KQL che verrà tracciata.</span><span class="sxs-lookup"><span data-stu-id="15cdf-126">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="15cdf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15cdf-127">-ResourceGroupName</span></span>
<span data-ttu-id="15cdf-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15cdf-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="15cdf-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15cdf-129">-SubscriptionId</span></span>
<span data-ttu-id="15cdf-130">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="15cdf-130">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="15cdf-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="15cdf-131">-Tag</span></span>
<span data-ttu-id="15cdf-132">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="15cdf-132">Resource tags</span></span>

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

### <span data-ttu-id="15cdf-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15cdf-133">-Confirm</span></span>
<span data-ttu-id="15cdf-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15cdf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15cdf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15cdf-135">-WhatIf</span></span>
<span data-ttu-id="15cdf-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15cdf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15cdf-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15cdf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15cdf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15cdf-138">CommonParameters</span></span>
<span data-ttu-id="15cdf-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15cdf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15cdf-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="15cdf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15cdf-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="15cdf-141">INPUTS</span></span>

### <span data-ttu-id="15cdf-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="15cdf-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="15cdf-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15cdf-143">OUTPUTS</span></span>

### <span data-ttu-id="15cdf-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="15cdf-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="15cdf-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="15cdf-145">NOTES</span></span>

<span data-ttu-id="15cdf-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="15cdf-146">ALIASES</span></span>

<span data-ttu-id="15cdf-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="15cdf-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15cdf-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="15cdf-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15cdf-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="15cdf-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15cdf-150">INPUTOBJECT <IResourceGraphIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="15cdf-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15cdf-151">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="15cdf-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15cdf-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15cdf-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="15cdf-153">`[ResourceName <String>]`: nome della risorsa Query grafico.</span><span class="sxs-lookup"><span data-stu-id="15cdf-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="15cdf-154">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="15cdf-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="15cdf-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15cdf-155">RELATED LINKS</span></span>

