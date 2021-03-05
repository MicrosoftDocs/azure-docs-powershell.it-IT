---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: c94f1e842697a64dd95f7d5ccb90e389484a61e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967246"
---
# <span data-ttu-id="ddc4d-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="ddc4d-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="ddc4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddc4d-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc4d-103">Aggiorna l'ascoltatore del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="ddc4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddc4d-104">SYNTAX</span></span>

### <span data-ttu-id="ddc4d-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ddc4d-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddc4d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ddc4d-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddc4d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddc4d-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc4d-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="ddc4d-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc4d-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ddc4d-109">DESCRIPTION</span></span>
<span data-ttu-id="ddc4d-110">Il Update-AzAvailabilityGroupListener cmdlet aggiorna un listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="ddc4d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddc4d-111">EXAMPLES</span></span>

### <span data-ttu-id="ddc4d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ddc4d-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="ddc4d-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc4d-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="ddc4d-114">AgSql01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="ddc4d-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="ddc4d-115">Aggiorna l'elenco SQL macchine virtuali per Il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="ddc4d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddc4d-116">PARAMETERS</span></span>

### <span data-ttu-id="ddc4d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddc4d-117">-AsJob</span></span>
<span data-ttu-id="ddc4d-118">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ddc4d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc4d-119">-DefaultProfile</span></span>
<span data-ttu-id="ddc4d-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddc4d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddc4d-121">-InputObject</span></span>
<span data-ttu-id="ddc4d-122">Oggetto Listener gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc4d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ddc4d-123">-Name</span></span>
<span data-ttu-id="ddc4d-124">Nome del listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc4d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc4d-125">-ResourceGroupName</span></span>
<span data-ttu-id="ddc4d-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ddc4d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddc4d-127">-ResourceId</span></span>
<span data-ttu-id="ddc4d-128">ID risorsa listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="ddc4d-128">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: AvailabilityGroupListenerId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc4d-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="ddc4d-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="ddc4d-130">Elenco degli ID di risorsa di Sql VM</span><span class="sxs-lookup"><span data-stu-id="ddc4d-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="ddc4d-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc4d-131">-SqlVMGroupName</span></span>
<span data-ttu-id="ddc4d-132">SQL del gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="ddc4d-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="ddc4d-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="ddc4d-134">SQL di gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="ddc4d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddc4d-135">-Confirm</span></span>
<span data-ttu-id="ddc4d-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc4d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc4d-137">-WhatIf</span></span>
<span data-ttu-id="ddc4d-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc4d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc4d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc4d-140">CommonParameters</span></span>
<span data-ttu-id="ddc4d-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc4d-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ddc4d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc4d-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="ddc4d-143">INPUTS</span></span>

### <span data-ttu-id="ddc4d-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupAmaModel</span><span class="sxs-lookup"><span data-stu-id="ddc4d-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="ddc4d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ddc4d-145">System.String</span></span>

### <span data-ttu-id="ddc4d-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ddc4d-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ddc4d-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddc4d-147">OUTPUTS</span></span>

### <span data-ttu-id="ddc4d-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupAmaModel</span><span class="sxs-lookup"><span data-stu-id="ddc4d-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="ddc4d-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="ddc4d-149">NOTES</span></span>

## <span data-ttu-id="ddc4d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddc4d-150">RELATED LINKS</span></span>
