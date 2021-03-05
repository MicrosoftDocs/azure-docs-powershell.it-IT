---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: a569f605c139d5cd34c42ee1567989acebabbe61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962253"
---
# <span data-ttu-id="47b0d-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="47b0d-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="47b0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="47b0d-103">Crea peering vNet per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="47b0d-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="47b0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47b0d-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47b0d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="47b0d-105">DESCRIPTION</span></span>
<span data-ttu-id="47b0d-106">Crea peering vNet per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="47b0d-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="47b0d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47b0d-107">EXAMPLES</span></span>

### <span data-ttu-id="47b0d-108">Esempio 1: Creare un peering vnet per databricks</span><span class="sxs-lookup"><span data-stu-id="47b0d-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="47b0d-109">Questo comando crea un peering vnet per i databrick.</span><span class="sxs-lookup"><span data-stu-id="47b0d-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="47b0d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47b0d-110">PARAMETERS</span></span>

### <span data-ttu-id="47b0d-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="47b0d-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="47b0d-112">Se il traffico inoltrato dalle macchine virtuali nella rete virtuale locale sarà consentito/non consentito nella rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="47b0d-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="47b0d-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="47b0d-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="47b0d-114">Se i collegamenti del gateway possono essere usati nella rete virtuale remota per collegarsi a questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="47b0d-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="47b0d-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="47b0d-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="47b0d-116">Se le macchine virtuali nello spazio di rete virtuale locale sarebbero in grado di accedere alle macchine virtuali nello spazio di rete virtuale remoto.</span><span class="sxs-lookup"><span data-stu-id="47b0d-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="47b0d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47b0d-117">-AsJob</span></span>
<span data-ttu-id="47b0d-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="47b0d-118">Run the command as a job</span></span>

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

### <span data-ttu-id="47b0d-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="47b0d-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="47b0d-120">Elenco di blocchi di indirizzi riservati per questa rete virtuale nella notazione CIDR.</span><span class="sxs-lookup"><span data-stu-id="47b0d-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b0d-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="47b0d-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="47b0d-122">ID della rete virtuale databricks.</span><span class="sxs-lookup"><span data-stu-id="47b0d-122">The Id of the databricks virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b0d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b0d-123">-DefaultProfile</span></span>
<span data-ttu-id="47b0d-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47b0d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b0d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="47b0d-125">-Name</span></span>
<span data-ttu-id="47b0d-126">Nome del peering vNet dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="47b0d-126">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b0d-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="47b0d-127">-NoWait</span></span>
<span data-ttu-id="47b0d-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="47b0d-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="47b0d-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="47b0d-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="47b0d-130">Elenco di blocchi di indirizzi riservati per questa rete virtuale nella notazione CIDR.</span><span class="sxs-lookup"><span data-stu-id="47b0d-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b0d-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="47b0d-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="47b0d-132">ID della rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="47b0d-132">The Id of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b0d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b0d-133">-ResourceGroupName</span></span>
<span data-ttu-id="47b0d-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="47b0d-134">The name of the resource group.</span></span>
<span data-ttu-id="47b0d-135">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="47b0d-135">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b0d-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47b0d-136">-SubscriptionId</span></span>
<span data-ttu-id="47b0d-137">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="47b0d-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b0d-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="47b0d-138">-UseRemoteGateway</span></span>
<span data-ttu-id="47b0d-139">Se è possibile usare gateway remoti in questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="47b0d-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="47b0d-140">Se il flag è impostato su true e allowGatewayTransit anche nel peering remoto è true, la rete virtuale userà i gateway della rete virtuale remota per il transito.</span><span class="sxs-lookup"><span data-stu-id="47b0d-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="47b0d-141">Solo un peering può avere questo flag impostato su true.</span><span class="sxs-lookup"><span data-stu-id="47b0d-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="47b0d-142">Questo flag non può essere impostato se la rete virtuale ha già un gateway.</span><span class="sxs-lookup"><span data-stu-id="47b0d-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="47b0d-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="47b0d-143">-WorkspaceName</span></span>
<span data-ttu-id="47b0d-144">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="47b0d-144">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b0d-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47b0d-145">-Confirm</span></span>
<span data-ttu-id="47b0d-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47b0d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47b0d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b0d-147">-WhatIf</span></span>
<span data-ttu-id="47b0d-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47b0d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b0d-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47b0d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47b0d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b0d-150">CommonParameters</span></span>
<span data-ttu-id="47b0d-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b0d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b0d-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47b0d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b0d-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="47b0d-153">INPUTS</span></span>

## <span data-ttu-id="47b0d-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47b0d-154">OUTPUTS</span></span>

### <span data-ttu-id="47b0d-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkApplicationing</span><span class="sxs-lookup"><span data-stu-id="47b0d-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="47b0d-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="47b0d-156">NOTES</span></span>

<span data-ttu-id="47b0d-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="47b0d-157">ALIASES</span></span>

## <span data-ttu-id="47b0d-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47b0d-158">RELATED LINKS</span></span>

