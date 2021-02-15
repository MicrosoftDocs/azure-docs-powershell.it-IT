---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176422"
---
# <span data-ttu-id="a60ff-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="a60ff-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="a60ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a60ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a60ff-103">Ottenere una query con un singolo grafico in base al valore resourceName.</span><span class="sxs-lookup"><span data-stu-id="a60ff-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="a60ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a60ff-104">SYNTAX</span></span>

### <span data-ttu-id="a60ff-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a60ff-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a60ff-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a60ff-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a60ff-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a60ff-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a60ff-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a60ff-108">DESCRIPTION</span></span>
<span data-ttu-id="a60ff-109">Ottenere una query con un singolo grafico in base al valore resourceName.</span><span class="sxs-lookup"><span data-stu-id="a60ff-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="a60ff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a60ff-110">EXAMPLES</span></span>

### <span data-ttu-id="a60ff-111">Esempio 1: Ottenere la query di tutti i grafici delle risorse in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a60ff-111">Example 1: Get all resource graph query under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="a60ff-112">Questo comando recupera tutte le query del diagramma risorse in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a60ff-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="a60ff-113">Esempio 2: Ottenere una query del grafico delle risorse in base al nome</span><span class="sxs-lookup"><span data-stu-id="a60ff-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="a60ff-114">Questo comando recupera una query del grafico risorse in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a60ff-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="a60ff-115">Esempio 2: Ottenere una query del grafico delle risorse per objecy</span><span class="sxs-lookup"><span data-stu-id="a60ff-115">Example 2: Get a resource graph query by objecy</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="a60ff-116">Questo comando recupera una query del grafico delle risorse per oggetto.</span><span class="sxs-lookup"><span data-stu-id="a60ff-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="a60ff-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a60ff-117">PARAMETERS</span></span>

### <span data-ttu-id="a60ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60ff-118">-DefaultProfile</span></span>
<span data-ttu-id="a60ff-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a60ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a60ff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a60ff-120">-InputObject</span></span>
<span data-ttu-id="a60ff-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a60ff-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a60ff-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a60ff-122">-Name</span></span>
<span data-ttu-id="a60ff-123">Nome della risorsa Query grafico.</span><span class="sxs-lookup"><span data-stu-id="a60ff-123">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="a60ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="a60ff-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a60ff-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a60ff-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a60ff-126">-SubscriptionId</span></span>
<span data-ttu-id="a60ff-127">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a60ff-127">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="a60ff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60ff-128">CommonParameters</span></span>
<span data-ttu-id="a60ff-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a60ff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60ff-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a60ff-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60ff-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="a60ff-131">INPUTS</span></span>

### <span data-ttu-id="a60ff-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="a60ff-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="a60ff-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a60ff-133">OUTPUTS</span></span>

### <span data-ttu-id="a60ff-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="a60ff-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="a60ff-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="a60ff-135">NOTES</span></span>

<span data-ttu-id="a60ff-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a60ff-136">ALIASES</span></span>

<span data-ttu-id="a60ff-137">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a60ff-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a60ff-138">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a60ff-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a60ff-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a60ff-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a60ff-140">INPUTOBJECT <IResourceGraphIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="a60ff-140">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a60ff-141">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a60ff-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a60ff-142">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a60ff-142">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a60ff-143">`[ResourceName <String>]`: nome della risorsa Query grafico.</span><span class="sxs-lookup"><span data-stu-id="a60ff-143">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="a60ff-144">`[SubscriptionId <String>]`: l'ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a60ff-144">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="a60ff-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a60ff-145">RELATED LINKS</span></span>

