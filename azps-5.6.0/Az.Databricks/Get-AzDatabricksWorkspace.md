---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: ec44b1ace55a36ebaa56c8b0242db485581c5e10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966462"
---
# <span data-ttu-id="e4933-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="e4933-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="e4933-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4933-102">SYNOPSIS</span></span>
<span data-ttu-id="e4933-103">Ottiene l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e4933-103">Gets the workspace.</span></span>

## <span data-ttu-id="e4933-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4933-104">SYNTAX</span></span>

### <span data-ttu-id="e4933-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4933-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e4933-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="e4933-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e4933-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e4933-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e4933-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="e4933-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e4933-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4933-109">DESCRIPTION</span></span>
<span data-ttu-id="e4933-110">Ottiene l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e4933-110">Gets the workspace.</span></span>

## <span data-ttu-id="e4933-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4933-111">EXAMPLES</span></span>

### <span data-ttu-id="e4933-112">Esempio 1: Ottenere un'area di lavoro Databricks con il nome</span><span class="sxs-lookup"><span data-stu-id="e4933-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="e4933-113">Questo comando recupera un'area di lavoro Databricks in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4933-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="e4933-114">Esempio 2: Elencare tutte le aree di lavoro Databricks in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="e4933-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="e4933-115">Questo comando elenca tutte le aree di lavoro Databricks in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e4933-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="e4933-116">Esempio 3: Elencare tutte le aree di lavoro Databricks in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e4933-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="e4933-117">Questo comando elenca tutte le aree di lavoro Databricks in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4933-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="e4933-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4933-118">PARAMETERS</span></span>

### <span data-ttu-id="e4933-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4933-119">-DefaultProfile</span></span>
<span data-ttu-id="e4933-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4933-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4933-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4933-121">-InputObject</span></span>
<span data-ttu-id="e4933-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e4933-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4933-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e4933-123">-Name</span></span>
<span data-ttu-id="e4933-124">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e4933-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="e4933-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4933-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4933-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4933-126">The name of the resource group.</span></span>
<span data-ttu-id="e4933-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e4933-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e4933-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4933-128">-SubscriptionId</span></span>
<span data-ttu-id="e4933-129">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e4933-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e4933-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4933-130">CommonParameters</span></span>
<span data-ttu-id="e4933-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4933-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4933-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e4933-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4933-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4933-133">INPUTS</span></span>

### <span data-ttu-id="e4933-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="e4933-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="e4933-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4933-135">OUTPUTS</span></span>

### <span data-ttu-id="e4933-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="e4933-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="e4933-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4933-137">NOTES</span></span>

<span data-ttu-id="e4933-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e4933-138">ALIASES</span></span>

<span data-ttu-id="e4933-139">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e4933-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4933-140">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e4933-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4933-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4933-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4933-142">INPUTOBJECT <IDatabricksIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e4933-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4933-143">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="e4933-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4933-144">`[PeeringName <String>]`: nome del peering vNet dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e4933-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="e4933-145">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4933-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e4933-146">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e4933-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="e4933-147">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e4933-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e4933-148">`[WorkspaceName <String>]`: nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e4933-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="e4933-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4933-149">RELATED LINKS</span></span>

