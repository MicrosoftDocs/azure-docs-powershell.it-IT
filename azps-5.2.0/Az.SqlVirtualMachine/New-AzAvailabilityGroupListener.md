---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364640"
---
# <span data-ttu-id="aa806-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="aa806-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="aa806-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa806-102">SYNOPSIS</span></span>
<span data-ttu-id="aa806-103">Crea un nuovo listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="aa806-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="aa806-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa806-104">SYNTAX</span></span>

### <span data-ttu-id="aa806-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa806-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa806-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="aa806-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa806-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa806-107">DESCRIPTION</span></span>
<span data-ttu-id="aa806-108">Il cmdlet New-AzAvailabilityGroupListener crea un nuovo listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="aa806-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="aa806-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa806-109">EXAMPLES</span></span>

### <span data-ttu-id="aa806-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aa806-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="aa806-111">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="aa806-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="aa806-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="aa806-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="aa806-113">Crea un nuovo listener del gruppo di disponibilità AgListener01 per il gruppo di disponibilità AvailabilityGroup01 nel gruppo SQL Virtual Machine SqlVmGroup01.</span><span class="sxs-lookup"><span data-stu-id="aa806-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="aa806-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa806-114">PARAMETERS</span></span>

### <span data-ttu-id="aa806-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa806-115">-AsJob</span></span>
<span data-ttu-id="aa806-116">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="aa806-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="aa806-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="aa806-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="aa806-118">Nome del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="aa806-118">Availability Group name.</span></span>

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

### <span data-ttu-id="aa806-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa806-119">-DefaultProfile</span></span>
<span data-ttu-id="aa806-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa806-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa806-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="aa806-121">-IpAddress</span></span>
<span data-ttu-id="aa806-122">Indirizzo IP privato</span><span class="sxs-lookup"><span data-stu-id="aa806-122">Private Ip Address</span></span>

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

### <span data-ttu-id="aa806-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="aa806-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="aa806-124">ID di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="aa806-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="aa806-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa806-125">-Name</span></span>
<span data-ttu-id="aa806-126">Nome del listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="aa806-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="aa806-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="aa806-127">-Port</span></span>
<span data-ttu-id="aa806-128">Numero di porta del listener di AG.</span><span class="sxs-lookup"><span data-stu-id="aa806-128">Port number of AG Listener.</span></span> <span data-ttu-id="aa806-129">Il valore predefinito è 1433.</span><span class="sxs-lookup"><span data-stu-id="aa806-129">Default Value is 1433.</span></span>

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

### <span data-ttu-id="aa806-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="aa806-130">-ProbePort</span></span>
<span data-ttu-id="aa806-131">Porta sonda</span><span class="sxs-lookup"><span data-stu-id="aa806-131">Probe Port</span></span>

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

### <span data-ttu-id="aa806-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="aa806-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="aa806-133">ID risorsa indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="aa806-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="aa806-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa806-134">-ResourceGroupName</span></span>
<span data-ttu-id="aa806-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aa806-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="aa806-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="aa806-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="aa806-137">Elenco degli ID delle risorse di SQL VM</span><span class="sxs-lookup"><span data-stu-id="aa806-137">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="aa806-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="aa806-138">-SqlVMGroupName</span></span>
<span data-ttu-id="aa806-139">Nome del gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="aa806-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="aa806-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="aa806-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="aa806-141">Oggetto gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="aa806-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="aa806-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="aa806-142">-SubnetId</span></span>
<span data-ttu-id="aa806-143">ID risorsa subnet</span><span class="sxs-lookup"><span data-stu-id="aa806-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="aa806-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa806-144">-Confirm</span></span>
<span data-ttu-id="aa806-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa806-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa806-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa806-146">-WhatIf</span></span>
<span data-ttu-id="aa806-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa806-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa806-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa806-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa806-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa806-149">CommonParameters</span></span>
<span data-ttu-id="aa806-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa806-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa806-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa806-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa806-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa806-152">INPUTS</span></span>

### <span data-ttu-id="aa806-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="aa806-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="aa806-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa806-154">OUTPUTS</span></span>

### <span data-ttu-id="aa806-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="aa806-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="aa806-156">Note</span><span class="sxs-lookup"><span data-stu-id="aa806-156">NOTES</span></span>

## <span data-ttu-id="aa806-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa806-157">RELATED LINKS</span></span>
