---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334360"
---
# <span data-ttu-id="d30c7-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="d30c7-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="d30c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d30c7-102">SYNOPSIS</span></span>
<span data-ttu-id="d30c7-103">Aggiorna il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="d30c7-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="d30c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d30c7-104">SYNTAX</span></span>

### <span data-ttu-id="d30c7-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d30c7-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d30c7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d30c7-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d30c7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d30c7-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d30c7-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="d30c7-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d30c7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d30c7-109">DESCRIPTION</span></span>
<span data-ttu-id="d30c7-110">Il cmdlet Update-AzAvailabilityGroupListener aggiorna un listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="d30c7-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="d30c7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d30c7-111">EXAMPLES</span></span>

### <span data-ttu-id="d30c7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d30c7-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="d30c7-113">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="d30c7-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="d30c7-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="d30c7-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="d30c7-115">Aggiorna l'elenco macchine virtuali SQL per il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="d30c7-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="d30c7-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d30c7-116">PARAMETERS</span></span>

### <span data-ttu-id="d30c7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d30c7-117">-AsJob</span></span>
<span data-ttu-id="d30c7-118">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="d30c7-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d30c7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d30c7-119">-DefaultProfile</span></span>
<span data-ttu-id="d30c7-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d30c7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d30c7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d30c7-121">-InputObject</span></span>
<span data-ttu-id="d30c7-122">Oggetto listener gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="d30c7-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="d30c7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d30c7-123">-Name</span></span>
<span data-ttu-id="d30c7-124">Nome del listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="d30c7-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="d30c7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d30c7-125">-ResourceGroupName</span></span>
<span data-ttu-id="d30c7-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d30c7-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="d30c7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d30c7-127">-ResourceId</span></span>
<span data-ttu-id="d30c7-128">ID risorsa listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="d30c7-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="d30c7-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d30c7-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="d30c7-130">Elenco degli ID delle risorse di SQL VM</span><span class="sxs-lookup"><span data-stu-id="d30c7-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="d30c7-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="d30c7-131">-SqlVMGroupName</span></span>
<span data-ttu-id="d30c7-132">Nome del gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="d30c7-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="d30c7-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="d30c7-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="d30c7-134">Oggetto gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="d30c7-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="d30c7-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d30c7-135">-Confirm</span></span>
<span data-ttu-id="d30c7-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d30c7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d30c7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d30c7-137">-WhatIf</span></span>
<span data-ttu-id="d30c7-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d30c7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d30c7-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d30c7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d30c7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d30c7-140">CommonParameters</span></span>
<span data-ttu-id="d30c7-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d30c7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d30c7-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d30c7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d30c7-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d30c7-143">INPUTS</span></span>

### <span data-ttu-id="d30c7-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="d30c7-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="d30c7-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d30c7-145">System.String</span></span>

### <span data-ttu-id="d30c7-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="d30c7-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="d30c7-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d30c7-147">OUTPUTS</span></span>

### <span data-ttu-id="d30c7-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="d30c7-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="d30c7-149">Note</span><span class="sxs-lookup"><span data-stu-id="d30c7-149">NOTES</span></span>

## <span data-ttu-id="d30c7-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d30c7-150">RELATED LINKS</span></span>
