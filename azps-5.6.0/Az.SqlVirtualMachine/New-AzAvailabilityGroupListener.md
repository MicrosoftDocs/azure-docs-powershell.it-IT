---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: f187a2704ed1f23d6cc5ac7dded1c8d9cd8ae954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008333"
---
# <span data-ttu-id="4d00d-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="4d00d-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="4d00d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d00d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d00d-103">Crea un nuovo ascoltatore del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="4d00d-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="4d00d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d00d-104">SYNTAX</span></span>

### <span data-ttu-id="4d00d-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d00d-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d00d-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="4d00d-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d00d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d00d-107">DESCRIPTION</span></span>
<span data-ttu-id="4d00d-108">Il New-AzAvailabilityGroupListener cmdlet crea un nuovo listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="4d00d-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="4d00d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d00d-109">EXAMPLES</span></span>

### <span data-ttu-id="4d00d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d00d-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="4d00d-111">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="4d00d-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="4d00d-112">AgSql01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="4d00d-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="4d00d-113">Crea un nuovo listener del gruppo di disponibilità Ag Listener01 per il gruppo di disponibilità AvailabilityGroup01 in SQL Gruppo di macchine virtuali SqlVmGroup01.</span><span class="sxs-lookup"><span data-stu-id="4d00d-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="4d00d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d00d-114">PARAMETERS</span></span>

### <span data-ttu-id="4d00d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d00d-115">-AsJob</span></span>
<span data-ttu-id="4d00d-116">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="4d00d-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4d00d-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="4d00d-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="4d00d-118">Nome del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="4d00d-118">Availability Group name.</span></span>

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

### <span data-ttu-id="4d00d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d00d-119">-DefaultProfile</span></span>
<span data-ttu-id="4d00d-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d00d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d00d-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="4d00d-121">-IpAddress</span></span>
<span data-ttu-id="4d00d-122">Indirizzo IP privato</span><span class="sxs-lookup"><span data-stu-id="4d00d-122">Private Ip Address</span></span>

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

### <span data-ttu-id="4d00d-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="4d00d-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="4d00d-124">ID servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="4d00d-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="4d00d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4d00d-125">-Name</span></span>
<span data-ttu-id="4d00d-126">Nome del listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="4d00d-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d00d-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="4d00d-127">-Port</span></span>
<span data-ttu-id="4d00d-128">Numero di porta di Listener di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="4d00d-128">Port number of AG Listener.</span></span> <span data-ttu-id="4d00d-129">Il valore predefinito è 1433.</span><span class="sxs-lookup"><span data-stu-id="4d00d-129">Default Value is 1433.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d00d-130">-Unaporta</span><span class="sxs-lookup"><span data-stu-id="4d00d-130">-ProbePort</span></span>
<span data-ttu-id="4d00d-131">Port di Port Disa loro</span><span class="sxs-lookup"><span data-stu-id="4d00d-131">Probe Port</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d00d-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="4d00d-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="4d00d-133">ID risorsa indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="4d00d-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="4d00d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d00d-134">-ResourceGroupName</span></span>
<span data-ttu-id="4d00d-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4d00d-135">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d00d-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="4d00d-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="4d00d-137">Elenco degli ID di risorsa di Sql VM</span><span class="sxs-lookup"><span data-stu-id="4d00d-137">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d00d-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="4d00d-138">-SqlVMGroupName</span></span>
<span data-ttu-id="4d00d-139">SQL del gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="4d00d-139">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d00d-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="4d00d-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="4d00d-141">SQL di gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="4d00d-141">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d00d-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4d00d-142">-SubnetId</span></span>
<span data-ttu-id="4d00d-143">ID risorsa subnet</span><span class="sxs-lookup"><span data-stu-id="4d00d-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="4d00d-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d00d-144">-Confirm</span></span>
<span data-ttu-id="4d00d-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d00d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d00d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d00d-146">-WhatIf</span></span>
<span data-ttu-id="4d00d-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d00d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d00d-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d00d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d00d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d00d-149">CommonParameters</span></span>
<span data-ttu-id="4d00d-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d00d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d00d-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d00d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d00d-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d00d-152">INPUTS</span></span>

### <span data-ttu-id="4d00d-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="4d00d-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="4d00d-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d00d-154">OUTPUTS</span></span>

### <span data-ttu-id="4d00d-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupFalse</span><span class="sxs-lookup"><span data-stu-id="4d00d-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="4d00d-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d00d-156">NOTES</span></span>

## <span data-ttu-id="4d00d-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d00d-157">RELATED LINKS</span></span>
