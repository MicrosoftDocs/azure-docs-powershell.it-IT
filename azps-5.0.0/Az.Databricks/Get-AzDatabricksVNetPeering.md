---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297343"
---
# <span data-ttu-id="f1f0b-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="f1f0b-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="f1f0b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f0b-103">Ottiene l'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="f1f0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1f0b-104">SYNTAX</span></span>

### <span data-ttu-id="f1f0b-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f1f0b-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f1f0b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f1f0b-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f1f0b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1f0b-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="f1f0b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1f0b-108">DESCRIPTION</span></span>
<span data-ttu-id="f1f0b-109">Ottiene l'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="f1f0b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1f0b-110">EXAMPLES</span></span>

### <span data-ttu-id="f1f0b-111">Esempio 1: elenca tutti i peering di VNET in un databricks</span><span class="sxs-lookup"><span data-stu-id="f1f0b-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="f1f0b-112">Questo comando elenca tutti i peering di VNET in un databricks.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="f1f0b-113">Esempio 2: ottenere un peering di VNET</span><span class="sxs-lookup"><span data-stu-id="f1f0b-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="f1f0b-114">Questo comando ottiene un peering vnet.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="f1f0b-115">Esempio 3: ottenere un peering di VNET per oggetto</span><span class="sxs-lookup"><span data-stu-id="f1f0b-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="f1f0b-116">Questo comando ottiene un peering VNET per oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="f1f0b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1f0b-117">PARAMETERS</span></span>

### <span data-ttu-id="f1f0b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f0b-118">-DefaultProfile</span></span>
<span data-ttu-id="f1f0b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f0b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1f0b-120">-InputObject</span></span>
<span data-ttu-id="f1f0b-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f1f0b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1f0b-122">-Name</span></span>
<span data-ttu-id="f1f0b-123">Nome dell'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="f1f0b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1f0b-124">-PassThru</span></span>
<span data-ttu-id="f1f0b-125">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="f1f0b-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f1f0b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f0b-126">-ResourceGroupName</span></span>
<span data-ttu-id="f1f0b-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-127">The name of the resource group.</span></span>
<span data-ttu-id="f1f0b-128">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f1f0b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1f0b-129">-SubscriptionId</span></span>
<span data-ttu-id="f1f0b-130">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f1f0b-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1f0b-131">-WorkspaceName</span></span>
<span data-ttu-id="f1f0b-132">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="f1f0b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f0b-133">CommonParameters</span></span>
<span data-ttu-id="f1f0b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f0b-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1f0b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f0b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1f0b-136">INPUTS</span></span>

### <span data-ttu-id="f1f0b-137">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="f1f0b-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="f1f0b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1f0b-138">OUTPUTS</span></span>

### <span data-ttu-id="f1f0b-139">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f1f0b-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="f1f0b-140">Note</span><span class="sxs-lookup"><span data-stu-id="f1f0b-140">NOTES</span></span>

<span data-ttu-id="f1f0b-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f1f0b-141">ALIASES</span></span>

<span data-ttu-id="f1f0b-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1f0b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f1f0b-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1f0b-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f1f0b-145">INPUTOBJECT <IDatabricksIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f1f0b-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1f0b-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="f1f0b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1f0b-147">`[PeeringName <String>]`: Nome dell'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="f1f0b-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f1f0b-149">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="f1f0b-150">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f1f0b-151">`[WorkspaceName <String>]`: Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f1f0b-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="f1f0b-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1f0b-152">RELATED LINKS</span></span>

