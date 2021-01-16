---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377019"
---
# <span data-ttu-id="ec7eb-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="ec7eb-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="ec7eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7eb-103">Ottiene l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-103">Gets the workspace.</span></span>

## <span data-ttu-id="ec7eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec7eb-104">SYNTAX</span></span>

### <span data-ttu-id="ec7eb-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec7eb-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ec7eb-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ec7eb-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ec7eb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ec7eb-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ec7eb-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="ec7eb-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ec7eb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec7eb-109">DESCRIPTION</span></span>
<span data-ttu-id="ec7eb-110">Ottiene l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-110">Gets the workspace.</span></span>

## <span data-ttu-id="ec7eb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec7eb-111">EXAMPLES</span></span>

### <span data-ttu-id="ec7eb-112">Esempio 1: ottenere un'area di lavoro databricks con il nome</span><span class="sxs-lookup"><span data-stu-id="ec7eb-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="ec7eb-113">Questo comando consente di ottenere un'area di lavoro databricks in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="ec7eb-114">Esempio 2: elencare tutte le aree di lavoro di databricks in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="ec7eb-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="ec7eb-115">Questo comando elenca tutte le aree di lavoro databricks in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="ec7eb-116">Esempio 3: elencare tutte le aree di lavoro databricks in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ec7eb-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="ec7eb-117">Questo comando elenca tutte le aree di lavoro databricks in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="ec7eb-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec7eb-118">PARAMETERS</span></span>

### <span data-ttu-id="ec7eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec7eb-119">-DefaultProfile</span></span>
<span data-ttu-id="ec7eb-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec7eb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec7eb-121">-InputObject</span></span>
<span data-ttu-id="ec7eb-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7eb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec7eb-123">-Name</span></span>
<span data-ttu-id="ec7eb-124">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-124">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7eb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec7eb-125">-ResourceGroupName</span></span>
<span data-ttu-id="ec7eb-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-126">The name of the resource group.</span></span>
<span data-ttu-id="ec7eb-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ec7eb-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec7eb-128">-SubscriptionId</span></span>
<span data-ttu-id="ec7eb-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7eb-130">CommonParameters</span></span>
<span data-ttu-id="ec7eb-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7eb-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec7eb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7eb-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec7eb-133">INPUTS</span></span>

### <span data-ttu-id="ec7eb-134">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="ec7eb-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="ec7eb-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec7eb-135">OUTPUTS</span></span>

### <span data-ttu-id="ec7eb-136">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="ec7eb-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="ec7eb-137">Note</span><span class="sxs-lookup"><span data-stu-id="ec7eb-137">NOTES</span></span>

<span data-ttu-id="ec7eb-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ec7eb-138">ALIASES</span></span>

<span data-ttu-id="ec7eb-139">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec7eb-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec7eb-140">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec7eb-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec7eb-142">INPUTOBJECT <IDatabricksIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ec7eb-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec7eb-143">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ec7eb-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec7eb-144">`[PeeringName <String>]`: Nome dell'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="ec7eb-145">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ec7eb-146">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="ec7eb-147">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ec7eb-148">`[WorkspaceName <String>]`: Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ec7eb-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="ec7eb-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec7eb-149">RELATED LINKS</span></span>

