---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 3fc5c493f94b6da371a4249479e397ea6e2362f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176431"
---
# <span data-ttu-id="b6b5f-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="b6b5f-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="b6b5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b5f-103">Eliminare una query grafico.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-103">Delete a graph query.</span></span>

## <span data-ttu-id="b6b5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6b5f-104">SYNTAX</span></span>

### <span data-ttu-id="b6b5f-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6b5f-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6b5f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b6b5f-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6b5f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6b5f-107">DESCRIPTION</span></span>
<span data-ttu-id="b6b5f-108">Eliminare una query grafico.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-108">Delete a graph query.</span></span>

## <span data-ttu-id="b6b5f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6b5f-109">EXAMPLES</span></span>

### <span data-ttu-id="b6b5f-110">Esempio 1: Rimuovere una query del grafico delle risorse in base al nome</span><span class="sxs-lookup"><span data-stu-id="b6b5f-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="b6b5f-111">Questo comando rimuove una query del grafico risorse in base al nome.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="b6b5f-112">Esempio 2: Rimuovere una query del grafico delle risorse per oggetto</span><span class="sxs-lookup"><span data-stu-id="b6b5f-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="b6b5f-113">Questo comando rimuove una query del diagramma risorse per oggetto.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="b6b5f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6b5f-114">PARAMETERS</span></span>

### <span data-ttu-id="b6b5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b5f-115">-DefaultProfile</span></span>
<span data-ttu-id="b6b5f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6b5f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6b5f-117">-InputObject</span></span>
<span data-ttu-id="b6b5f-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b5f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b6b5f-119">-Name</span></span>
<span data-ttu-id="b6b5f-120">Nome della risorsa Query grafico.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-120">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="b6b5f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6b5f-121">-PassThru</span></span>
<span data-ttu-id="b6b5f-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="b6b5f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b6b5f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6b5f-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6b5f-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b6b5f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6b5f-125">-SubscriptionId</span></span>
<span data-ttu-id="b6b5f-126">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-126">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="b6b5f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6b5f-127">-Confirm</span></span>
<span data-ttu-id="b6b5f-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6b5f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6b5f-129">-WhatIf</span></span>
<span data-ttu-id="b6b5f-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6b5f-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6b5f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b5f-132">CommonParameters</span></span>
<span data-ttu-id="b6b5f-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b5f-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b5f-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6b5f-135">INPUTS</span></span>

### <span data-ttu-id="b6b5f-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="b6b5f-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="b6b5f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6b5f-137">OUTPUTS</span></span>

### <span data-ttu-id="b6b5f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b6b5f-138">System.Boolean</span></span>

## <span data-ttu-id="b6b5f-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6b5f-139">NOTES</span></span>

<span data-ttu-id="b6b5f-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b6b5f-140">ALIASES</span></span>

<span data-ttu-id="b6b5f-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b6b5f-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6b5f-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6b5f-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6b5f-144">INPUTOBJECT <IResourceGraphIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="b6b5f-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6b5f-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b6b5f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6b5f-146">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b6b5f-147">`[ResourceName <String>]`: nome della risorsa Query grafico.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="b6b5f-148">`[SubscriptionId <String>]`: l'ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="b6b5f-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6b5f-149">RELATED LINKS</span></span>

