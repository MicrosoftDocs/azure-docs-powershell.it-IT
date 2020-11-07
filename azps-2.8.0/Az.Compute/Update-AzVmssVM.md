---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: bc24cab117a3ada64c4e64118b4b9b86ebffef55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675104"
---
# <span data-ttu-id="2b62b-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="2b62b-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="2b62b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b62b-102">SYNOPSIS</span></span>
<span data-ttu-id="2b62b-103">Aggiorna lo stato di una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="2b62b-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="2b62b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b62b-104">SYNTAX</span></span>

### <span data-ttu-id="2b62b-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b62b-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b62b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2b62b-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b62b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2b62b-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b62b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b62b-108">DESCRIPTION</span></span>
<span data-ttu-id="2b62b-109">Aggiorna lo stato di una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="2b62b-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="2b62b-110">Per il momento, l'unico aggiornamento consentito è l'aggiunta di un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="2b62b-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="2b62b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b62b-111">EXAMPLES</span></span>

### <span data-ttu-id="2b62b-112">Esempio 1: aggiungere un disco di dati gestito a una VM vmss con New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2b62b-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="2b62b-113">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="2b62b-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="2b62b-114">Il comando successivo crea un oggetto disco dati con il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="2b62b-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="2b62b-115">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="2b62b-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="2b62b-116">Il comando finale aggiorna la VM vmss aggiungendo un nuovo disco di dati.</span><span class="sxs-lookup"><span data-stu-id="2b62b-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="2b62b-117">Esempio 2: aggiungere un disco di dati gestito a una VM vmss con Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2b62b-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="2b62b-118">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="2b62b-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="2b62b-119">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="2b62b-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="2b62b-120">Il comando successivo aggiunge il disco gestito alla VM vmss archiviata localmente in $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="2b62b-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="2b62b-121">Il comando finale aggiorna la VM vmss con il disco di dati aggiunto.</span><span class="sxs-lookup"><span data-stu-id="2b62b-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="2b62b-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b62b-122">PARAMETERS</span></span>

### <span data-ttu-id="2b62b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b62b-123">-AsJob</span></span>
<span data-ttu-id="2b62b-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2b62b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b62b-125">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="2b62b-125">-DataDisk</span></span>

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

### <span data-ttu-id="2b62b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b62b-126">-DefaultProfile</span></span>
<span data-ttu-id="2b62b-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b62b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b62b-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2b62b-128">-InstanceId</span></span>
<span data-ttu-id="2b62b-129">Specifica l'ID istanza di una VM VMSS.</span><span class="sxs-lookup"><span data-stu-id="2b62b-129">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="2b62b-130">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="2b62b-130">-ProtectFromScaleIn</span></span>
<span data-ttu-id="2b62b-131">Indica che la scala della macchina virtuale set VM non deve essere considerata per l'eliminazione durante un'operazione di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="2b62b-131">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="2b62b-132">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="2b62b-132">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="2b62b-133">Indica che gli aggiornamenti o le azioni del modello (incluso il ridimensionamento) avviati in VMSS non devono essere applicati alla VM VMSS.</span><span class="sxs-lookup"><span data-stu-id="2b62b-133">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="2b62b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b62b-134">-ResourceGroupName</span></span>
<span data-ttu-id="2b62b-135">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="2b62b-135">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="2b62b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b62b-136">-ResourceId</span></span>
<span data-ttu-id="2b62b-137">ID risorsa per la scala macchina virtuale set VM</span><span class="sxs-lookup"><span data-stu-id="2b62b-137">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="2b62b-138">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2b62b-138">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="2b62b-139">Oggetto VM set della scala della macchina virtuale locale</span><span class="sxs-lookup"><span data-stu-id="2b62b-139">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="2b62b-140">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2b62b-140">-VMScaleSetName</span></span>
<span data-ttu-id="2b62b-141">Nome del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="2b62b-141">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="2b62b-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b62b-142">-Confirm</span></span>
<span data-ttu-id="2b62b-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b62b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b62b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b62b-144">-WhatIf</span></span>
<span data-ttu-id="2b62b-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b62b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b62b-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b62b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b62b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b62b-147">CommonParameters</span></span>
<span data-ttu-id="2b62b-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b62b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b62b-149">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b62b-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b62b-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b62b-150">INPUTS</span></span>

### <span data-ttu-id="2b62b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="2b62b-151">System.String</span></span>

### <span data-ttu-id="2b62b-152">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="2b62b-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="2b62b-153">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2b62b-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2b62b-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b62b-154">OUTPUTS</span></span>

### <span data-ttu-id="2b62b-155">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2b62b-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2b62b-156">Note</span><span class="sxs-lookup"><span data-stu-id="2b62b-156">NOTES</span></span>

## <span data-ttu-id="2b62b-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b62b-157">RELATED LINKS</span></span>
