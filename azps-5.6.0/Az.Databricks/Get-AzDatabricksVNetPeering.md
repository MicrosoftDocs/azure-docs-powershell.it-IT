---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: a5654fa0974accf4319df4cbbd08ef220fa7ad9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966477"
---
# <span data-ttu-id="0e202-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="0e202-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="0e202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e202-102">SYNOPSIS</span></span>
<span data-ttu-id="0e202-103">Ottiene il peering vNet dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0e202-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="0e202-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e202-104">SYNTAX</span></span>

### <span data-ttu-id="0e202-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0e202-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0e202-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="0e202-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0e202-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0e202-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="0e202-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0e202-108">DESCRIPTION</span></span>
<span data-ttu-id="0e202-109">Ottiene il peering vNet dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0e202-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="0e202-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e202-110">EXAMPLES</span></span>

### <span data-ttu-id="0e202-111">Esempio 1: Elencare tutti i peering vnet in un databrick</span><span class="sxs-lookup"><span data-stu-id="0e202-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="0e202-112">Questo comando elenca tutti i peering vnet sotto un databrick.</span><span class="sxs-lookup"><span data-stu-id="0e202-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="0e202-113">Esempio 2: Ottenere un peering vnet</span><span class="sxs-lookup"><span data-stu-id="0e202-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="0e202-114">Questo comando ottiene un peering vnet.</span><span class="sxs-lookup"><span data-stu-id="0e202-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="0e202-115">Esempio 3: Ottenere un peering vnet in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="0e202-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="0e202-116">Questo comando ottiene un peering vnet per oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e202-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="0e202-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e202-117">PARAMETERS</span></span>

### <span data-ttu-id="0e202-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e202-118">-DefaultProfile</span></span>
<span data-ttu-id="0e202-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e202-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e202-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e202-120">-InputObject</span></span>
<span data-ttu-id="0e202-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0e202-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0e202-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0e202-122">-Name</span></span>
<span data-ttu-id="0e202-123">Nome del peering vNet dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0e202-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="0e202-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e202-124">-PassThru</span></span>
<span data-ttu-id="0e202-125">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="0e202-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0e202-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e202-126">-ResourceGroupName</span></span>
<span data-ttu-id="0e202-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0e202-127">The name of the resource group.</span></span>
<span data-ttu-id="0e202-128">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0e202-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0e202-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e202-129">-SubscriptionId</span></span>
<span data-ttu-id="0e202-130">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e202-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0e202-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0e202-131">-WorkspaceName</span></span>
<span data-ttu-id="0e202-132">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0e202-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="0e202-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e202-133">CommonParameters</span></span>
<span data-ttu-id="0e202-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e202-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e202-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0e202-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e202-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="0e202-136">INPUTS</span></span>

### <span data-ttu-id="0e202-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="0e202-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="0e202-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e202-138">OUTPUTS</span></span>

### <span data-ttu-id="0e202-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkEndoing</span><span class="sxs-lookup"><span data-stu-id="0e202-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="0e202-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="0e202-140">NOTES</span></span>

<span data-ttu-id="0e202-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0e202-141">ALIASES</span></span>

<span data-ttu-id="0e202-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0e202-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0e202-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0e202-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0e202-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0e202-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0e202-145">INPUTOBJECT <IDatabricksIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="0e202-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0e202-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="0e202-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0e202-147">`[PeeringName <String>]`: nome del peering vNet dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0e202-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="0e202-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0e202-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0e202-149">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0e202-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="0e202-150">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e202-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0e202-151">`[WorkspaceName <String>]`: nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0e202-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="0e202-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e202-152">RELATED LINKS</span></span>

