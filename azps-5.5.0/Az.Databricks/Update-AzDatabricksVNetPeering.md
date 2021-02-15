---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209762"
---
# <span data-ttu-id="eefda-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="eefda-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="eefda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eefda-102">SYNOPSIS</span></span>
<span data-ttu-id="eefda-103">Aggiornare il peering vNet per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eefda-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="eefda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eefda-104">SYNTAX</span></span>

### <span data-ttu-id="eefda-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eefda-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eefda-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="eefda-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eefda-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eefda-107">DESCRIPTION</span></span>
<span data-ttu-id="eefda-108">Aggiornare il peering vNet per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eefda-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="eefda-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eefda-109">EXAMPLES</span></span>

### <span data-ttu-id="eefda-110">Esempio 1: Aggiornare AllowForwardedTraffic del peering vnet</span><span class="sxs-lookup"><span data-stu-id="eefda-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="eefda-111">Questo comando aggiorna AllowForwardedTraffic del peering vnet.</span><span class="sxs-lookup"><span data-stu-id="eefda-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="eefda-112">Esempio 2: Aggiornare AllowForwardedTraffic del peering vnet in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="eefda-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="eefda-113">Questo comando aggiorna AllowForwardedTraffic del peering vnet in base all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="eefda-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="eefda-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eefda-114">PARAMETERS</span></span>

### <span data-ttu-id="eefda-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="eefda-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="eefda-116">[System.Management.Automation.SwitchParameter] Indica se il traffico inoltrato dalle macchine virtuali nella rete virtuale locale sarà consentito/non consentito nella rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="eefda-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefda-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="eefda-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="eefda-118">[System.Management.Automation.SwitchParameter] Se i collegamenti del gateway possono essere usati nella rete virtuale remota per collegarsi a questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="eefda-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefda-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="eefda-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="eefda-120">[System.Management.Automation.SwitchParameter] Se le macchine virtuali nello spazio di rete virtuale locale sarebbero in grado di accedere alle macchine virtuali nello spazio di rete virtuale remoto.</span><span class="sxs-lookup"><span data-stu-id="eefda-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefda-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eefda-121">-AsJob</span></span>
<span data-ttu-id="eefda-122">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="eefda-122">Run the command as a job</span></span>

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

### <span data-ttu-id="eefda-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eefda-123">-DefaultProfile</span></span>
<span data-ttu-id="eefda-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eefda-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eefda-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eefda-125">-InputObject</span></span>
<span data-ttu-id="eefda-126">Parametro di identità.</span><span class="sxs-lookup"><span data-stu-id="eefda-126">Identity parameter.</span></span>
<span data-ttu-id="eefda-127">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="eefda-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eefda-128">-Name</span><span class="sxs-lookup"><span data-stu-id="eefda-128">-Name</span></span>
<span data-ttu-id="eefda-129">Nome di VNetCollectioning.</span><span class="sxs-lookup"><span data-stu-id="eefda-129">The name of the VNetPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PeeringName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefda-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eefda-130">-NoWait</span></span>
<span data-ttu-id="eefda-131">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="eefda-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eefda-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eefda-132">-ResourceGroupName</span></span>
<span data-ttu-id="eefda-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eefda-133">The name of the resource group.</span></span>
<span data-ttu-id="eefda-134">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="eefda-134">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefda-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eefda-135">-SubscriptionId</span></span>
<span data-ttu-id="eefda-136">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eefda-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefda-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="eefda-137">-UseRemoteGateway</span></span>
<span data-ttu-id="eefda-138">[System.Management.Automation.SwitchParameter] Se è possibile usare gateway remoti in questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="eefda-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="eefda-139">Se il flag è impostato su true e allowGatewayTransit anche nel peering remoto è true, la rete virtuale userà gateway di rete virtuale remota per il transito.</span><span class="sxs-lookup"><span data-stu-id="eefda-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="eefda-140">Solo un peering può avere questo flag impostato su true.</span><span class="sxs-lookup"><span data-stu-id="eefda-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="eefda-141">Questo flag non può essere impostato se la rete virtuale ha già un gateway.</span><span class="sxs-lookup"><span data-stu-id="eefda-141">This flag cannot be set if virtual network already has a gateway.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefda-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eefda-142">-WorkspaceName</span></span>
<span data-ttu-id="eefda-143">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eefda-143">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefda-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eefda-144">-Confirm</span></span>
<span data-ttu-id="eefda-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eefda-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eefda-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eefda-146">-WhatIf</span></span>
<span data-ttu-id="eefda-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eefda-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eefda-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eefda-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eefda-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefda-149">CommonParameters</span></span>
<span data-ttu-id="eefda-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eefda-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefda-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eefda-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefda-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="eefda-152">INPUTS</span></span>

### <span data-ttu-id="eefda-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="eefda-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="eefda-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eefda-154">OUTPUTS</span></span>

### <span data-ttu-id="eefda-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkEndoing</span><span class="sxs-lookup"><span data-stu-id="eefda-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="eefda-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="eefda-156">NOTES</span></span>

<span data-ttu-id="eefda-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="eefda-157">ALIASES</span></span>

<span data-ttu-id="eefda-158">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="eefda-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eefda-159">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="eefda-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eefda-160">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eefda-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eefda-161"><IDatabricksIdentity>INPUTOBJECT: parametro Identity.</span><span class="sxs-lookup"><span data-stu-id="eefda-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="eefda-162">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="eefda-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eefda-163">`[PeeringName <String>]`: nome del peering vNet dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eefda-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="eefda-164">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eefda-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="eefda-165">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="eefda-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="eefda-166">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eefda-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="eefda-167">`[WorkspaceName <String>]`: nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eefda-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="eefda-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eefda-168">RELATED LINKS</span></span>

