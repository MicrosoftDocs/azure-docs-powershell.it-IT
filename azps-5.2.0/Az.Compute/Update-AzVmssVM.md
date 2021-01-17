---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360846"
---
# <span data-ttu-id="e588a-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="e588a-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="e588a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e588a-102">SYNOPSIS</span></span>
<span data-ttu-id="e588a-103">Aggiorna lo stato di una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="e588a-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="e588a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e588a-104">SYNTAX</span></span>

### <span data-ttu-id="e588a-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e588a-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e588a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e588a-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e588a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e588a-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e588a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e588a-108">DESCRIPTION</span></span>
<span data-ttu-id="e588a-109">Aggiorna lo stato di una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="e588a-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="e588a-110">Per il momento, l'unico aggiornamento consentito è l'aggiunta di un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="e588a-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="e588a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e588a-111">EXAMPLES</span></span>

### <span data-ttu-id="e588a-112">Esempio 1: aggiungere un disco di dati gestito a una VM vmss con New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e588a-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="e588a-113">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="e588a-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="e588a-114">Il comando successivo crea un oggetto disco dati con il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="e588a-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="e588a-115">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="e588a-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="e588a-116">Il comando finale aggiorna la VM vmss aggiungendo un nuovo disco di dati.</span><span class="sxs-lookup"><span data-stu-id="e588a-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="e588a-117">Esempio 2: aggiungere un disco di dati gestito a una VM vmss con Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e588a-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="e588a-118">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="e588a-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="e588a-119">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="e588a-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="e588a-120">Il comando successivo aggiunge il disco gestito alla VM vmss archiviata localmente in $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="e588a-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="e588a-121">Il comando finale aggiorna la VM vmss con il disco di dati aggiunto.</span><span class="sxs-lookup"><span data-stu-id="e588a-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="e588a-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e588a-122">Example 3</span></span>

<span data-ttu-id="e588a-123">Aggiorna lo stato di una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="e588a-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="e588a-124">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="e588a-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="e588a-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e588a-125">PARAMETERS</span></span>

### <span data-ttu-id="e588a-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e588a-126">-AsJob</span></span>
<span data-ttu-id="e588a-127">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e588a-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e588a-128">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="e588a-128">-DataDisk</span></span>

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

### <span data-ttu-id="e588a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e588a-129">-DefaultProfile</span></span>
<span data-ttu-id="e588a-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e588a-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e588a-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e588a-131">-InstanceId</span></span>
<span data-ttu-id="e588a-132">Specifica l'ID istanza di una VM VMSS.</span><span class="sxs-lookup"><span data-stu-id="e588a-132">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="e588a-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="e588a-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="e588a-134">Indica che la scala della macchina virtuale set VM non deve essere considerata per l'eliminazione durante un'operazione di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="e588a-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="e588a-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="e588a-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="e588a-136">Indica che gli aggiornamenti o le azioni del modello (incluso il ridimensionamento) avviati in VMSS non devono essere applicati alla VM VMSS.</span><span class="sxs-lookup"><span data-stu-id="e588a-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="e588a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e588a-137">-ResourceGroupName</span></span>
<span data-ttu-id="e588a-138">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="e588a-138">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="e588a-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e588a-139">-ResourceId</span></span>
<span data-ttu-id="e588a-140">ID risorsa per la scala macchina virtuale set VM</span><span class="sxs-lookup"><span data-stu-id="e588a-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="e588a-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e588a-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="e588a-142">Oggetto VM set della scala della macchina virtuale locale</span><span class="sxs-lookup"><span data-stu-id="e588a-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="e588a-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e588a-143">-VMScaleSetName</span></span>
<span data-ttu-id="e588a-144">Nome del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e588a-144">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="e588a-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e588a-145">-Confirm</span></span>
<span data-ttu-id="e588a-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e588a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e588a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e588a-147">-WhatIf</span></span>
<span data-ttu-id="e588a-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e588a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e588a-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e588a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e588a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e588a-150">CommonParameters</span></span>
<span data-ttu-id="e588a-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e588a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e588a-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e588a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e588a-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e588a-153">INPUTS</span></span>

### <span data-ttu-id="e588a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e588a-154">System.String</span></span>

### <span data-ttu-id="e588a-155">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="e588a-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="e588a-156">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e588a-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="e588a-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e588a-157">OUTPUTS</span></span>

### <span data-ttu-id="e588a-158">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e588a-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="e588a-159">Note</span><span class="sxs-lookup"><span data-stu-id="e588a-159">NOTES</span></span>

## <span data-ttu-id="e588a-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e588a-160">RELATED LINKS</span></span>
