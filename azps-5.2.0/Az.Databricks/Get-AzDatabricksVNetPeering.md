---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350392"
---
# <span data-ttu-id="bd088-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="bd088-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="bd088-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd088-102">SYNOPSIS</span></span>
<span data-ttu-id="bd088-103">Ottiene l'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="bd088-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="bd088-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd088-104">SYNTAX</span></span>

### <span data-ttu-id="bd088-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bd088-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bd088-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="bd088-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="bd088-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bd088-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="bd088-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd088-108">DESCRIPTION</span></span>
<span data-ttu-id="bd088-109">Ottiene l'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="bd088-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="bd088-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd088-110">EXAMPLES</span></span>

### <span data-ttu-id="bd088-111">Esempio 1: elenca tutti i peering di VNET in un databricks</span><span class="sxs-lookup"><span data-stu-id="bd088-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="bd088-112">Questo comando elenca tutti i peering di VNET in un databricks.</span><span class="sxs-lookup"><span data-stu-id="bd088-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="bd088-113">Esempio 2: ottenere un peering di VNET</span><span class="sxs-lookup"><span data-stu-id="bd088-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="bd088-114">Questo comando ottiene un peering vnet.</span><span class="sxs-lookup"><span data-stu-id="bd088-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="bd088-115">Esempio 3: ottenere un peering di VNET per oggetto</span><span class="sxs-lookup"><span data-stu-id="bd088-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="bd088-116">Questo comando ottiene un peering VNET per oggetto.</span><span class="sxs-lookup"><span data-stu-id="bd088-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="bd088-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd088-117">PARAMETERS</span></span>

### <span data-ttu-id="bd088-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd088-118">-DefaultProfile</span></span>
<span data-ttu-id="bd088-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd088-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd088-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd088-120">-InputObject</span></span>
<span data-ttu-id="bd088-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bd088-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bd088-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd088-122">-Name</span></span>
<span data-ttu-id="bd088-123">Nome dell'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="bd088-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="bd088-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd088-124">-PassThru</span></span>
<span data-ttu-id="bd088-125">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="bd088-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd088-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd088-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd088-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bd088-127">The name of the resource group.</span></span>
<span data-ttu-id="bd088-128">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bd088-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bd088-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd088-129">-SubscriptionId</span></span>
<span data-ttu-id="bd088-130">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bd088-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bd088-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bd088-131">-WorkspaceName</span></span>
<span data-ttu-id="bd088-132">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bd088-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="bd088-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd088-133">CommonParameters</span></span>
<span data-ttu-id="bd088-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd088-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd088-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd088-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd088-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd088-136">INPUTS</span></span>

### <span data-ttu-id="bd088-137">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="bd088-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="bd088-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd088-138">OUTPUTS</span></span>

### <span data-ttu-id="bd088-139">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="bd088-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="bd088-140">Note</span><span class="sxs-lookup"><span data-stu-id="bd088-140">NOTES</span></span>

<span data-ttu-id="bd088-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bd088-141">ALIASES</span></span>

<span data-ttu-id="bd088-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd088-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bd088-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bd088-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bd088-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bd088-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bd088-145">INPUTOBJECT <IDatabricksIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="bd088-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bd088-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="bd088-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bd088-147">`[PeeringName <String>]`: Nome dell'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="bd088-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="bd088-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bd088-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bd088-149">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bd088-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="bd088-150">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bd088-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bd088-151">`[WorkspaceName <String>]`: Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bd088-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="bd088-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd088-152">RELATED LINKS</span></span>

