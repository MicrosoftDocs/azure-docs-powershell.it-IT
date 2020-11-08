---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199981"
---
# <span data-ttu-id="0bbd6-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="0bbd6-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="0bbd6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bbd6-102">SYNOPSIS</span></span>
<span data-ttu-id="0bbd6-103">Aggiorna il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="0bbd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bbd6-104">SYNTAX</span></span>

### <span data-ttu-id="0bbd6-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0bbd6-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bbd6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0bbd6-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bbd6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bbd6-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bbd6-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="0bbd6-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bbd6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bbd6-109">DESCRIPTION</span></span>
<span data-ttu-id="0bbd6-110">Il cmdlet Update-AzAvailabilityGroupListener aggiorna un listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="0bbd6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bbd6-111">EXAMPLES</span></span>

### <span data-ttu-id="0bbd6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0bbd6-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="0bbd6-113">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="0bbd6-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="0bbd6-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="0bbd6-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="0bbd6-115">Aggiorna l'elenco macchine virtuali SQL per il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="0bbd6-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bbd6-116">PARAMETERS</span></span>

### <span data-ttu-id="0bbd6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bbd6-117">-AsJob</span></span>
<span data-ttu-id="0bbd6-118">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="0bbd6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bbd6-119">-DefaultProfile</span></span>
<span data-ttu-id="0bbd6-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bbd6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bbd6-121">-InputObject</span></span>
<span data-ttu-id="0bbd6-122">Oggetto listener gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="0bbd6-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bbd6-123">-Name</span></span>
<span data-ttu-id="0bbd6-124">Nome del listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="0bbd6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bbd6-125">-ResourceGroupName</span></span>
<span data-ttu-id="0bbd6-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="0bbd6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bbd6-127">-ResourceId</span></span>
<span data-ttu-id="0bbd6-128">ID risorsa listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="0bbd6-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="0bbd6-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0bbd6-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="0bbd6-130">Elenco degli ID delle risorse di SQL VM</span><span class="sxs-lookup"><span data-stu-id="0bbd6-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="0bbd6-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="0bbd6-131">-SqlVMGroupName</span></span>
<span data-ttu-id="0bbd6-132">Nome del gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="0bbd6-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="0bbd6-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="0bbd6-134">Oggetto gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="0bbd6-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0bbd6-135">-Confirm</span></span>
<span data-ttu-id="0bbd6-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bbd6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bbd6-137">-WhatIf</span></span>
<span data-ttu-id="0bbd6-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bbd6-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bbd6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bbd6-140">CommonParameters</span></span>
<span data-ttu-id="0bbd6-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bbd6-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bbd6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bbd6-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bbd6-143">INPUTS</span></span>

### <span data-ttu-id="0bbd6-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="0bbd6-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="0bbd6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0bbd6-145">System.String</span></span>

### <span data-ttu-id="0bbd6-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="0bbd6-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="0bbd6-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bbd6-147">OUTPUTS</span></span>

### <span data-ttu-id="0bbd6-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="0bbd6-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="0bbd6-149">Note</span><span class="sxs-lookup"><span data-stu-id="0bbd6-149">NOTES</span></span>

## <span data-ttu-id="0bbd6-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bbd6-150">RELATED LINKS</span></span>