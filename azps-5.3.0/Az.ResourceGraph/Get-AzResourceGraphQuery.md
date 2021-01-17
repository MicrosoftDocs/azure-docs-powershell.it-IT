---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475712"
---
# <span data-ttu-id="aae15-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="aae15-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="aae15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aae15-102">SYNOPSIS</span></span>
<span data-ttu-id="aae15-103">Ottenere una query a singolo grafico in base alla relativa resourceName.</span><span class="sxs-lookup"><span data-stu-id="aae15-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="aae15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aae15-104">SYNTAX</span></span>

### <span data-ttu-id="aae15-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aae15-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="aae15-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="aae15-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aae15-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aae15-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="aae15-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aae15-108">DESCRIPTION</span></span>
<span data-ttu-id="aae15-109">Ottenere una query a singolo grafico in base alla relativa resourceName.</span><span class="sxs-lookup"><span data-stu-id="aae15-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="aae15-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aae15-110">EXAMPLES</span></span>

### <span data-ttu-id="aae15-111">Esempio 1: ottenere tutte le query del grafico risorse in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="aae15-111">Example 1: Get all resource graph query under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="aae15-112">Questo comando consente di ottenere tutte le query del grafico risorse in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aae15-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="aae15-113">Esempio 2: ottenere una query del grafico delle risorse per nome</span><span class="sxs-lookup"><span data-stu-id="aae15-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="aae15-114">Questo comando ottiene una query per il grafico delle risorse per nome.</span><span class="sxs-lookup"><span data-stu-id="aae15-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="aae15-115">Esempio 2: ottenere una query del grafico delle risorse in base a objecy</span><span class="sxs-lookup"><span data-stu-id="aae15-115">Example 2: Get a resource graph query by objecy</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="aae15-116">Questo comando ottiene una query del grafico delle risorse per oggetto.</span><span class="sxs-lookup"><span data-stu-id="aae15-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="aae15-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aae15-117">PARAMETERS</span></span>

### <span data-ttu-id="aae15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae15-118">-DefaultProfile</span></span>
<span data-ttu-id="aae15-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aae15-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aae15-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aae15-120">-InputObject</span></span>
<span data-ttu-id="aae15-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="aae15-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aae15-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="aae15-122">-Name</span></span>
<span data-ttu-id="aae15-123">Il nome della risorsa query del grafico.</span><span class="sxs-lookup"><span data-stu-id="aae15-123">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="aae15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aae15-124">-ResourceGroupName</span></span>
<span data-ttu-id="aae15-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aae15-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="aae15-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aae15-126">-SubscriptionId</span></span>
<span data-ttu-id="aae15-127">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="aae15-127">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="aae15-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae15-128">CommonParameters</span></span>
<span data-ttu-id="aae15-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae15-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae15-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aae15-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae15-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aae15-131">INPUTS</span></span>

### <span data-ttu-id="aae15-132">Microsoft. Azure. PowerShell. Cmdlets. ResourceGraph. Models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="aae15-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="aae15-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aae15-133">OUTPUTS</span></span>

### <span data-ttu-id="aae15-134">Microsoft. Azure. PowerShell. Cmdlets. ResourceGraph. Models. Api20180901Preview. IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="aae15-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="aae15-135">Note</span><span class="sxs-lookup"><span data-stu-id="aae15-135">NOTES</span></span>

<span data-ttu-id="aae15-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="aae15-136">ALIASES</span></span>

<span data-ttu-id="aae15-137">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aae15-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aae15-138">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="aae15-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aae15-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aae15-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aae15-140">INPUTOBJECT <IResourceGraphIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="aae15-140">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aae15-141">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="aae15-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aae15-142">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aae15-142">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="aae15-143">`[ResourceName <String>]`: Nome della risorsa query del grafico.</span><span class="sxs-lookup"><span data-stu-id="aae15-143">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="aae15-144">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="aae15-144">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="aae15-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aae15-145">RELATED LINKS</span></span>

