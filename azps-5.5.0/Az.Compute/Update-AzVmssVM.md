---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194958"
---
# <span data-ttu-id="f5e2b-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="f5e2b-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="f5e2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e2b-103">Aggiorna lo stato di una VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="f5e2b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5e2b-104">SYNTAX</span></span>

### <span data-ttu-id="f5e2b-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="f5e2b-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5e2b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f5e2b-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5e2b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f5e2b-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5e2b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f5e2b-108">DESCRIPTION</span></span>
<span data-ttu-id="f5e2b-109">Aggiorna lo stato di una VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="f5e2b-110">Per il momento, l'unico aggiornamento consentito è l'aggiunta di un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="f5e2b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5e2b-111">EXAMPLES</span></span>

### <span data-ttu-id="f5e2b-112">Esempio 1: Aggiungere un disco dati gestito a una VM Vmss usando New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f5e2b-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="f5e2b-113">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="f5e2b-114">Il comando successivo crea un oggetto disco dati con il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="f5e2b-115">Il comando successivo ottiene una VM Vmss esistente specificata dal nome del gruppo di risorse, dal nome della macchina virtuale e dall'ID dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="f5e2b-116">Il comando finale aggiorna Vmss VM aggiungendo un nuovo disco dati.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="f5e2b-117">Esempio 2: Aggiungere un disco dati gestito a una VM Vmss usando Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f5e2b-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="f5e2b-118">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="f5e2b-119">Il comando successivo ottiene una VM Vmss esistente specificata dal nome del gruppo di risorse, dal nome della macchina virtuale e dall'ID dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="f5e2b-120">Il comando successivo aggiunge il disco gestito alla macchina virtuale Vmss archiviata localmente in $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="f5e2b-121">Il comando finale aggiorna vmss con il disco dati aggiunto.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="f5e2b-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f5e2b-122">Example 3</span></span>

<span data-ttu-id="f5e2b-123">Aggiorna lo stato di una VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="f5e2b-124">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="f5e2b-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="f5e2b-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5e2b-125">PARAMETERS</span></span>

### <span data-ttu-id="f5e2b-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5e2b-126">-AsJob</span></span>
<span data-ttu-id="f5e2b-127">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f5e2b-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5e2b-128">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="f5e2b-128">-DataDisk</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e2b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e2b-129">-DefaultProfile</span></span>
<span data-ttu-id="f5e2b-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5e2b-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f5e2b-131">-InstanceId</span></span>
<span data-ttu-id="f5e2b-132">Specifica l'ID istanza di una macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-132">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e2b-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="f5e2b-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="f5e2b-134">Indica che la MACCHINA virtuale per il set di scalabilità della macchina virtuale non deve essere considerata per l'eliminazione durante un'operazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="f5e2b-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="f5e2b-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="f5e2b-136">Indica che gli aggiornamenti o le azioni del modello (incluso il scale-in) avviati nel sistema VMSS non devono essere applicati alla macchina virtuale VMSS.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="f5e2b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e2b-137">-ResourceGroupName</span></span>
<span data-ttu-id="f5e2b-138">Specifica il nome del gruppo di risorse del sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-138">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e2b-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5e2b-139">-ResourceId</span></span>
<span data-ttu-id="f5e2b-140">ID risorsa per la macchina virtuale impostata per il set di scalabilità della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f5e2b-140">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e2b-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f5e2b-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="f5e2b-142">Oggetto VM impostato per il set di scalabilità della macchina virtuale locale</span><span class="sxs-lookup"><span data-stu-id="f5e2b-142">Local virtual machine scale set VM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e2b-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f5e2b-143">-VMScaleSetName</span></span>
<span data-ttu-id="f5e2b-144">Nome del set di scalabilità della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f5e2b-144">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e2b-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5e2b-145">-Confirm</span></span>
<span data-ttu-id="f5e2b-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5e2b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5e2b-147">-WhatIf</span></span>
<span data-ttu-id="f5e2b-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5e2b-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5e2b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e2b-150">CommonParameters</span></span>
<span data-ttu-id="f5e2b-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e2b-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f5e2b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e2b-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="f5e2b-153">INPUTS</span></span>

### <span data-ttu-id="f5e2b-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f5e2b-154">System.String</span></span>

### <span data-ttu-id="f5e2b-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="f5e2b-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="f5e2b-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f5e2b-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="f5e2b-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5e2b-157">OUTPUTS</span></span>

### <span data-ttu-id="f5e2b-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f5e2b-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="f5e2b-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="f5e2b-159">NOTES</span></span>

## <span data-ttu-id="f5e2b-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5e2b-160">RELATED LINKS</span></span>
