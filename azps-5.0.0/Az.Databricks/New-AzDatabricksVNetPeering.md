---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297324"
---
# <span data-ttu-id="cdcbc-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="cdcbc-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="cdcbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdcbc-102">SYNOPSIS</span></span>
<span data-ttu-id="cdcbc-103">Crea un peering vNet per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="cdcbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdcbc-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cdcbc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdcbc-105">DESCRIPTION</span></span>
<span data-ttu-id="cdcbc-106">Crea un peering vNet per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="cdcbc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdcbc-107">EXAMPLES</span></span>

### <span data-ttu-id="cdcbc-108">Esempio 1: creare un peering VNET per databricks</span><span class="sxs-lookup"><span data-stu-id="cdcbc-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="cdcbc-109">Questo comando crea un peering VNET per databricks.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="cdcbc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdcbc-110">PARAMETERS</span></span>

### <span data-ttu-id="cdcbc-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="cdcbc-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="cdcbc-112">Se il traffico inoltrato dalle VM nella rete virtuale locale sarà consentito/non consentito in una rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="cdcbc-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="cdcbc-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="cdcbc-114">Se i collegamenti del gateway possono essere usati in una rete virtuale remota per creare un collegamento a questo network virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="cdcbc-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="cdcbc-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="cdcbc-116">Se le VM nello spazio di rete virtuale locale sarebbero in grado di accedere alle VM nello spazio di rete virtuale remoto.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="cdcbc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdcbc-117">-AsJob</span></span>
<span data-ttu-id="cdcbc-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="cdcbc-118">Run the command as a job</span></span>

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

### <span data-ttu-id="cdcbc-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="cdcbc-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="cdcbc-120">Elenco di blocchi di indirizzi riservati per questa rete virtuale nella notazione CIDR.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="cdcbc-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="cdcbc-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="cdcbc-122">ID della rete virtuale databricks.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="cdcbc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdcbc-123">-DefaultProfile</span></span>
<span data-ttu-id="cdcbc-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdcbc-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdcbc-125">-Name</span></span>
<span data-ttu-id="cdcbc-126">Nome dell'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="cdcbc-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="cdcbc-127">-NoWait</span></span>
<span data-ttu-id="cdcbc-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="cdcbc-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cdcbc-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="cdcbc-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="cdcbc-130">Elenco di blocchi di indirizzi riservati per questa rete virtuale nella notazione CIDR.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="cdcbc-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="cdcbc-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="cdcbc-132">ID della rete virtuale remota.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="cdcbc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdcbc-133">-ResourceGroupName</span></span>
<span data-ttu-id="cdcbc-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-134">The name of the resource group.</span></span>
<span data-ttu-id="cdcbc-135">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cdcbc-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cdcbc-136">-SubscriptionId</span></span>
<span data-ttu-id="cdcbc-137">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cdcbc-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="cdcbc-138">-UseRemoteGateway</span></span>
<span data-ttu-id="cdcbc-139">Se i gateway remoti possono essere usati in questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="cdcbc-140">Se il contrassegno è impostato su true e anche allowGatewayTransit su peering remoto è vero, la rete virtuale utilizzerà i gateway della rete virtuale remota per il transito.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="cdcbc-141">Questo flag può essere impostato su true solo per un peering.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="cdcbc-142">Questo contrassegno non può essere impostato se Virtual Network ha già un gateway.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="cdcbc-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cdcbc-143">-WorkspaceName</span></span>
<span data-ttu-id="cdcbc-144">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="cdcbc-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cdcbc-145">-Confirm</span></span>
<span data-ttu-id="cdcbc-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdcbc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdcbc-147">-WhatIf</span></span>
<span data-ttu-id="cdcbc-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdcbc-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdcbc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdcbc-150">CommonParameters</span></span>
<span data-ttu-id="cdcbc-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdcbc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdcbc-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdcbc-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdcbc-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdcbc-153">INPUTS</span></span>

## <span data-ttu-id="cdcbc-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdcbc-154">OUTPUTS</span></span>

### <span data-ttu-id="cdcbc-155">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cdcbc-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="cdcbc-156">Note</span><span class="sxs-lookup"><span data-stu-id="cdcbc-156">NOTES</span></span>

<span data-ttu-id="cdcbc-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cdcbc-157">ALIASES</span></span>

## <span data-ttu-id="cdcbc-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdcbc-158">RELATED LINKS</span></span>

