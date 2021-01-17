---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 3fc5c493f94b6da371a4249479e397ea6e2362f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377915"
---
# <span data-ttu-id="a4797-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="a4797-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="a4797-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4797-102">SYNOPSIS</span></span>
<span data-ttu-id="a4797-103">Eliminare una query di grafico.</span><span class="sxs-lookup"><span data-stu-id="a4797-103">Delete a graph query.</span></span>

## <span data-ttu-id="a4797-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4797-104">SYNTAX</span></span>

### <span data-ttu-id="a4797-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4797-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a4797-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4797-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a4797-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4797-107">DESCRIPTION</span></span>
<span data-ttu-id="a4797-108">Eliminare una query di grafico.</span><span class="sxs-lookup"><span data-stu-id="a4797-108">Delete a graph query.</span></span>

## <span data-ttu-id="a4797-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4797-109">EXAMPLES</span></span>

### <span data-ttu-id="a4797-110">Esempio 1: rimuovere una query del grafico risorse per nome</span><span class="sxs-lookup"><span data-stu-id="a4797-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="a4797-111">Questo comando consente di rimuovere una query del grafico risorse per nome.</span><span class="sxs-lookup"><span data-stu-id="a4797-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="a4797-112">Esempio 2: rimuovere una query del grafico risorse per oggetto</span><span class="sxs-lookup"><span data-stu-id="a4797-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="a4797-113">Questo comando consente di rimuovere una query del grafico risorse per oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4797-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="a4797-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4797-114">PARAMETERS</span></span>

### <span data-ttu-id="a4797-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4797-115">-DefaultProfile</span></span>
<span data-ttu-id="a4797-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4797-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4797-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4797-117">-InputObject</span></span>
<span data-ttu-id="a4797-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a4797-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a4797-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4797-119">-Name</span></span>
<span data-ttu-id="a4797-120">Il nome della risorsa query del grafico.</span><span class="sxs-lookup"><span data-stu-id="a4797-120">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="a4797-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4797-121">-PassThru</span></span>
<span data-ttu-id="a4797-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="a4797-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a4797-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4797-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4797-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4797-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4797-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4797-125">-SubscriptionId</span></span>
<span data-ttu-id="a4797-126">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4797-126">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="a4797-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4797-127">-Confirm</span></span>
<span data-ttu-id="a4797-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4797-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4797-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4797-129">-WhatIf</span></span>
<span data-ttu-id="a4797-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4797-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4797-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4797-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4797-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4797-132">CommonParameters</span></span>
<span data-ttu-id="a4797-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4797-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4797-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4797-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4797-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4797-135">INPUTS</span></span>

### <span data-ttu-id="a4797-136">Microsoft. Azure. PowerShell. Cmdlets. ResourceGraph. Models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="a4797-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="a4797-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4797-137">OUTPUTS</span></span>

### <span data-ttu-id="a4797-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4797-138">System.Boolean</span></span>

## <span data-ttu-id="a4797-139">Note</span><span class="sxs-lookup"><span data-stu-id="a4797-139">NOTES</span></span>

<span data-ttu-id="a4797-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a4797-140">ALIASES</span></span>

<span data-ttu-id="a4797-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4797-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4797-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a4797-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4797-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4797-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4797-144">INPUTOBJECT <IResourceGraphIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a4797-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4797-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a4797-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4797-146">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4797-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a4797-147">`[ResourceName <String>]`: Nome della risorsa query del grafico.</span><span class="sxs-lookup"><span data-stu-id="a4797-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="a4797-148">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="a4797-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="a4797-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4797-149">RELATED LINKS</span></span>

