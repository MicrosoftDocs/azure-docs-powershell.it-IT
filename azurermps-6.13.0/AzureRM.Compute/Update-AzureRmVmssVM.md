---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmssVM.md
ms.openlocfilehash: 3003387b0d989d01231e7be549727ebc88158723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687618"
---
# <span data-ttu-id="a76ff-101">Update-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="a76ff-101">Update-AzureRmVmssVM</span></span>

## <span data-ttu-id="a76ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a76ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a76ff-103">Aggiorna lo stato di una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="a76ff-103">Updates the state of a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a76ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a76ff-104">SYNTAX</span></span>

### <span data-ttu-id="a76ff-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a76ff-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a76ff-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a76ff-106">ResourceIdParameter</span></span>
```
Update-AzureRmVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a76ff-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a76ff-107">ObjectParameter</span></span>
```
Update-AzureRmVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a76ff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a76ff-108">DESCRIPTION</span></span>
<span data-ttu-id="a76ff-109">Aggiorna lo stato di una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="a76ff-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="a76ff-110">Per il momento, l'unico aggiornamento consentito è l'aggiunta di un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="a76ff-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="a76ff-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a76ff-111">EXAMPLES</span></span>

### <span data-ttu-id="a76ff-112">Esempio 1: aggiungere un disco di dati gestito a una VM vmss con New-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a76ff-112">Example 1: Add a managed data disk to a Vmss VM using New-AzureRmVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzureRmVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="a76ff-113">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="a76ff-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="a76ff-114">Il comando successivo crea un oggetto disco dati con il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="a76ff-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="a76ff-115">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="a76ff-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="a76ff-116">Il comando finale aggiorna la VM vmss aggiungendo un nuovo disco di dati.</span><span class="sxs-lookup"><span data-stu-id="a76ff-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="a76ff-117">Esempio 2: aggiungere un disco di dati gestito a una VM vmss con Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a76ff-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzureRmVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="a76ff-118">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="a76ff-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="a76ff-119">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="a76ff-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="a76ff-120">Il comando successivo aggiunge il disco gestito alla VM vmss archiviata localmente in $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="a76ff-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="a76ff-121">Il comando finale aggiorna la VM vmss con il disco di dati aggiunto.</span><span class="sxs-lookup"><span data-stu-id="a76ff-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="a76ff-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a76ff-122">PARAMETERS</span></span>

### <span data-ttu-id="a76ff-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a76ff-123">-AsJob</span></span>
<span data-ttu-id="a76ff-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a76ff-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a76ff-125">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="a76ff-125">-DataDisk</span></span>

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

### <span data-ttu-id="a76ff-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76ff-126">-DefaultProfile</span></span>
<span data-ttu-id="a76ff-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a76ff-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76ff-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a76ff-128">-InstanceId</span></span>
<span data-ttu-id="a76ff-129">Specifica l'ID istanza di una VM VMSS.</span><span class="sxs-lookup"><span data-stu-id="a76ff-129">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a76ff-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a76ff-130">-ResourceGroupName</span></span>
<span data-ttu-id="a76ff-131">Specifica il nome del gruppo di risorse di VMSS.</span><span class="sxs-lookup"><span data-stu-id="a76ff-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a76ff-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a76ff-132">-ResourceId</span></span>
<span data-ttu-id="a76ff-133">ID risorsa per la scala macchina virtuale set VM</span><span class="sxs-lookup"><span data-stu-id="a76ff-133">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="a76ff-134">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a76ff-134">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="a76ff-135">Oggetto VM set della scala della macchina virtuale locale</span><span class="sxs-lookup"><span data-stu-id="a76ff-135">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="a76ff-136">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a76ff-136">-VMScaleSetName</span></span>
<span data-ttu-id="a76ff-137">Nome del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="a76ff-137">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a76ff-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a76ff-138">-Confirm</span></span>
<span data-ttu-id="a76ff-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a76ff-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a76ff-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76ff-140">-WhatIf</span></span>
<span data-ttu-id="a76ff-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a76ff-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a76ff-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a76ff-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a76ff-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76ff-143">CommonParameters</span></span>
<span data-ttu-id="a76ff-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a76ff-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76ff-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a76ff-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76ff-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a76ff-146">INPUTS</span></span>

### <span data-ttu-id="a76ff-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a76ff-147">System.String</span></span>

### <span data-ttu-id="a76ff-148">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="a76ff-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>
<span data-ttu-id="a76ff-149">Parametri: DataDisk (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a76ff-149">Parameters: DataDisk (ByValue)</span></span>

### <span data-ttu-id="a76ff-150">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a76ff-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>
<span data-ttu-id="a76ff-151">Parametri: VirtualMachineScaleSetVM (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a76ff-151">Parameters: VirtualMachineScaleSetVM (ByValue)</span></span>

## <span data-ttu-id="a76ff-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a76ff-152">OUTPUTS</span></span>

### <span data-ttu-id="a76ff-153">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a76ff-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="a76ff-154">Note</span><span class="sxs-lookup"><span data-stu-id="a76ff-154">NOTES</span></span>

## <span data-ttu-id="a76ff-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a76ff-155">RELATED LINKS</span></span>
