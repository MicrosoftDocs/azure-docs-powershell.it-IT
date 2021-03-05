---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 46f59df272a62ca9cd6b517d3672436a01a75ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000157"
---
# <span data-ttu-id="b79a3-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="b79a3-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="b79a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b79a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b79a3-103">Ottenere una query con un singolo grafico in base al valore resourceName.</span><span class="sxs-lookup"><span data-stu-id="b79a3-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="b79a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b79a3-104">SYNTAX</span></span>

### <span data-ttu-id="b79a3-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b79a3-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b79a3-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b79a3-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b79a3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b79a3-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b79a3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b79a3-108">DESCRIPTION</span></span>
<span data-ttu-id="b79a3-109">Ottenere una query con un singolo grafico in base al valore resourceName.</span><span class="sxs-lookup"><span data-stu-id="b79a3-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="b79a3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b79a3-110">EXAMPLES</span></span>

### <span data-ttu-id="b79a3-111">Esempio 1: Ottenere tutte le query del diagramma risorse in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b79a3-111">Example 1: Get all resource graph queries under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="b79a3-112">Questo comando recupera tutte le query del diagramma risorse in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b79a3-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="b79a3-113">Esempio 2: Ottenere una query del grafico delle risorse in base al nome</span><span class="sxs-lookup"><span data-stu-id="b79a3-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="b79a3-114">Questo comando recupera una query del grafico risorse in base al nome.</span><span class="sxs-lookup"><span data-stu-id="b79a3-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="b79a3-115">Esempio 2: Ottenere una query del grafico delle risorse per oggetto</span><span class="sxs-lookup"><span data-stu-id="b79a3-115">Example 2: Get a resource graph query by object</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="b79a3-116">Questo comando recupera una query del grafico delle risorse per oggetto.</span><span class="sxs-lookup"><span data-stu-id="b79a3-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="b79a3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b79a3-117">PARAMETERS</span></span>

### <span data-ttu-id="b79a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b79a3-118">-DefaultProfile</span></span>
<span data-ttu-id="b79a3-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b79a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b79a3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b79a3-120">-InputObject</span></span>
<span data-ttu-id="b79a3-121">Parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b79a3-121">Identity Parameter</span></span>

<span data-ttu-id="b79a3-122">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b79a3-122">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b79a3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b79a3-123">-Name</span></span>
<span data-ttu-id="b79a3-124">Nome della risorsa Query grafico.</span><span class="sxs-lookup"><span data-stu-id="b79a3-124">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b79a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="b79a3-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b79a3-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79a3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b79a3-127">-SubscriptionId</span></span>
<span data-ttu-id="b79a3-128">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b79a3-128">The Azure subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b79a3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b79a3-129">CommonParameters</span></span>
<span data-ttu-id="b79a3-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b79a3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b79a3-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b79a3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b79a3-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="b79a3-132">INPUTS</span></span>

### <span data-ttu-id="b79a3-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="b79a3-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="b79a3-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b79a3-134">OUTPUTS</span></span>

### <span data-ttu-id="b79a3-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="b79a3-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="b79a3-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="b79a3-136">NOTES</span></span>

<span data-ttu-id="b79a3-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b79a3-137">ALIASES</span></span>

<span data-ttu-id="b79a3-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b79a3-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b79a3-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b79a3-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b79a3-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b79a3-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b79a3-141">INPUTOBJECT <IResourceGraphIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b79a3-141">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b79a3-142">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b79a3-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b79a3-143">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b79a3-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b79a3-144">`[ResourceName <String>]`: nome della risorsa Query grafico.</span><span class="sxs-lookup"><span data-stu-id="b79a3-144">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="b79a3-145">`[SubscriptionId <String>]`: l'ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b79a3-145">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="b79a3-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b79a3-146">RELATED LINKS</span></span>

