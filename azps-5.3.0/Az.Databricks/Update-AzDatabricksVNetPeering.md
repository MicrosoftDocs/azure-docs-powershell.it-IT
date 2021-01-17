---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479307"
---
# <span data-ttu-id="efc2f-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="efc2f-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="efc2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="efc2f-102">SYNOPSIS</span></span>
<span data-ttu-id="efc2f-103">Aggiornare il peering di vNet per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="efc2f-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="efc2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efc2f-104">SYNTAX</span></span>

### <span data-ttu-id="efc2f-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="efc2f-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="efc2f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="efc2f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="efc2f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efc2f-107">DESCRIPTION</span></span>
<span data-ttu-id="efc2f-108">Aggiornare il peering di vNet per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="efc2f-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="efc2f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efc2f-109">EXAMPLES</span></span>

### <span data-ttu-id="efc2f-110">Esempio 1: aggiornare AllowForwardedTraffic di VNET peering</span><span class="sxs-lookup"><span data-stu-id="efc2f-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="efc2f-111">Questo comando Aggiorna AllowForwardedTraffic di VNET peering.</span><span class="sxs-lookup"><span data-stu-id="efc2f-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="efc2f-112">Esempio 2: aggiornare AllowForwardedTraffic di VNET peering per oggetto</span><span class="sxs-lookup"><span data-stu-id="efc2f-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="efc2f-113">Questo comando Aggiorna AllowForwardedTraffic di VNET peering per oggetto.</span><span class="sxs-lookup"><span data-stu-id="efc2f-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="efc2f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efc2f-114">PARAMETERS</span></span>

### <span data-ttu-id="efc2f-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="efc2f-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="efc2f-116">[System. Management. Automation. SwitchParameter] se il traffico inoltrato dalle VM nella rete virtuale locale sarà consentito/non consentito in una rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="efc2f-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="efc2f-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="efc2f-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="efc2f-118">[System. Management. Automation. SwitchParameter] se i collegamenti del gateway possono essere usati in una rete virtuale remota per collegarsi a questo network virtuale.</span><span class="sxs-lookup"><span data-stu-id="efc2f-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="efc2f-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="efc2f-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="efc2f-120">[System. Management. Automation. SwitchParameter] se le VM nello spazio di rete virtuale locale sarebbero in grado di accedere alle VM nello spazio di rete virtuale remoto.</span><span class="sxs-lookup"><span data-stu-id="efc2f-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="efc2f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efc2f-121">-AsJob</span></span>
<span data-ttu-id="efc2f-122">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="efc2f-122">Run the command as a job</span></span>

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

### <span data-ttu-id="efc2f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc2f-123">-DefaultProfile</span></span>
<span data-ttu-id="efc2f-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efc2f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc2f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efc2f-125">-InputObject</span></span>
<span data-ttu-id="efc2f-126">Parametro Identity.</span><span class="sxs-lookup"><span data-stu-id="efc2f-126">Identity parameter.</span></span>
<span data-ttu-id="efc2f-127">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="efc2f-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="efc2f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="efc2f-128">-Name</span></span>
<span data-ttu-id="efc2f-129">Il nome del VNetPeering.</span><span class="sxs-lookup"><span data-stu-id="efc2f-129">The name of the VNetPeering.</span></span>

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

### <span data-ttu-id="efc2f-130">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="efc2f-130">-NoWait</span></span>
<span data-ttu-id="efc2f-131">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="efc2f-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="efc2f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc2f-132">-ResourceGroupName</span></span>
<span data-ttu-id="efc2f-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="efc2f-133">The name of the resource group.</span></span>
<span data-ttu-id="efc2f-134">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="efc2f-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="efc2f-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="efc2f-135">-SubscriptionId</span></span>
<span data-ttu-id="efc2f-136">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="efc2f-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="efc2f-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="efc2f-137">-UseRemoteGateway</span></span>
<span data-ttu-id="efc2f-138">[System. Management. Automation. SwitchParameter] se i gateway remoti possono essere usati in questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="efc2f-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="efc2f-139">Se il contrassegno è impostato su true e anche allowGatewayTransit su peering remoto è vero, la rete virtuale utilizzerà i gateway della rete virtuale remota per il transito.</span><span class="sxs-lookup"><span data-stu-id="efc2f-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="efc2f-140">Questo flag può essere impostato su true solo per un peering.</span><span class="sxs-lookup"><span data-stu-id="efc2f-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="efc2f-141">Questo contrassegno non può essere impostato se Virtual Network ha già un gateway.</span><span class="sxs-lookup"><span data-stu-id="efc2f-141">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="efc2f-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="efc2f-142">-WorkspaceName</span></span>
<span data-ttu-id="efc2f-143">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="efc2f-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="efc2f-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="efc2f-144">-Confirm</span></span>
<span data-ttu-id="efc2f-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efc2f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc2f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc2f-146">-WhatIf</span></span>
<span data-ttu-id="efc2f-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efc2f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efc2f-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efc2f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc2f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc2f-149">CommonParameters</span></span>
<span data-ttu-id="efc2f-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc2f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc2f-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efc2f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc2f-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="efc2f-152">INPUTS</span></span>

### <span data-ttu-id="efc2f-153">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="efc2f-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="efc2f-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efc2f-154">OUTPUTS</span></span>

### <span data-ttu-id="efc2f-155">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="efc2f-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="efc2f-156">Note</span><span class="sxs-lookup"><span data-stu-id="efc2f-156">NOTES</span></span>

<span data-ttu-id="efc2f-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="efc2f-157">ALIASES</span></span>

<span data-ttu-id="efc2f-158">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efc2f-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="efc2f-159">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="efc2f-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="efc2f-160">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="efc2f-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="efc2f-161">INPUTOBJECT <IDatabricksIdentity> : parametro Identity.</span><span class="sxs-lookup"><span data-stu-id="efc2f-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="efc2f-162">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="efc2f-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="efc2f-163">`[PeeringName <String>]`: Nome dell'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="efc2f-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="efc2f-164">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="efc2f-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="efc2f-165">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="efc2f-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="efc2f-166">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="efc2f-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="efc2f-167">`[WorkspaceName <String>]`: Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="efc2f-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="efc2f-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efc2f-168">RELATED LINKS</span></span>

