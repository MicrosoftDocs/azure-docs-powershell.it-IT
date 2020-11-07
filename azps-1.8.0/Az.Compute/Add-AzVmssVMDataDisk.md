---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 81f9e57bd2d815616cfc856246ff6950230f7112
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684830"
---
# <span data-ttu-id="de12e-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="de12e-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="de12e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de12e-102">SYNOPSIS</span></span>
<span data-ttu-id="de12e-103">Aggiunge un disco di dati a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="de12e-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="de12e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de12e-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de12e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de12e-105">DESCRIPTION</span></span>
<span data-ttu-id="de12e-106">Il cmdlet **Add-AzVmssVMDataDisk** aggiunge un disco di dati a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="de12e-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="de12e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de12e-107">EXAMPLES</span></span>

### <span data-ttu-id="de12e-108">Esempio 1: aggiungere un disco di dati gestito a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="de12e-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="de12e-109">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="de12e-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="de12e-110">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="de12e-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="de12e-111">Il comando successivo aggiunge il disco gestito alla VM vmss archiviata localmente in $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="de12e-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="de12e-112">Il comando finale aggiorna la VM vmss con il disco di dati aggiunto.</span><span class="sxs-lookup"><span data-stu-id="de12e-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="de12e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de12e-113">PARAMETERS</span></span>

### <span data-ttu-id="de12e-114">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="de12e-114">-Caching</span></span>
<span data-ttu-id="de12e-115">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="de12e-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="de12e-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="de12e-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="de12e-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="de12e-117">ReadOnly</span></span>
- <span data-ttu-id="de12e-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="de12e-118">ReadWrite</span></span>
- <span data-ttu-id="de12e-119">None il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="de12e-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="de12e-120">La modifica di questo valore fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="de12e-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="de12e-121">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="de12e-121">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de12e-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="de12e-122">-CreateOption</span></span>
<span data-ttu-id="de12e-123">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="de12e-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="de12e-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="de12e-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="de12e-125">Allegare.</span><span class="sxs-lookup"><span data-stu-id="de12e-125">Attach.</span></span>
<span data-ttu-id="de12e-126">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="de12e-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="de12e-127">Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="de12e-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="de12e-128">Il *VhdUri* è tutto ciò che serve per indicare alla piattaforma Azure la posizione del disco rigido virtuale (VHD) da allegare come disco di dati alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de12e-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="de12e-129">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="de12e-129">Empty.</span></span>
<span data-ttu-id="de12e-130">Specificalo per creare un disco dati vuoto.</span><span class="sxs-lookup"><span data-stu-id="de12e-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="de12e-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="de12e-131">FromImage.</span></span>
<span data-ttu-id="de12e-132">Specificare questa opzione per creare una macchina virtuale da un'immagine o un disco generalizzato.</span><span class="sxs-lookup"><span data-stu-id="de12e-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="de12e-133">Quando specifichi questa opzione, devi specificare il parametro *SourceImageUri* anche per indicare alla piattaforma Azure la posizione del VHD da allegare come disco di dati.</span><span class="sxs-lookup"><span data-stu-id="de12e-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="de12e-134">Il parametro *VhdUri* viene usato come posizione per identificare dove verrà archiviato il VHD del disco dati quando viene usato dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de12e-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de12e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de12e-135">-DefaultProfile</span></span>
<span data-ttu-id="de12e-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de12e-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de12e-137">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="de12e-137">-DiskSizeInGB</span></span>
<span data-ttu-id="de12e-138">Specifica le dimensioni, in gigabyte, di un disco vuoto da allegare a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de12e-138">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de12e-139">-Lun</span><span class="sxs-lookup"><span data-stu-id="de12e-139">-Lun</span></span>
<span data-ttu-id="de12e-140">Specifica il numero di unità logica (LUN) per un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="de12e-140">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de12e-141">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="de12e-141">-ManagedDiskId</span></span>
<span data-ttu-id="de12e-142">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="de12e-142">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de12e-143">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="de12e-143">-StorageAccountType</span></span>
<span data-ttu-id="de12e-144">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="de12e-144">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de12e-145">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="de12e-145">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="de12e-146">Specifica l'oggetto VM del set di scale della macchina virtuale locale a cui aggiungere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="de12e-146">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="de12e-147">Puoi usare il cmdlet **Get-AzVmssVM** per ottenere un oggetto VM set della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="de12e-147">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de12e-148">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="de12e-148">-WriteAccelerator</span></span>
<span data-ttu-id="de12e-149">Specifica se WriteAccelerator deve essere abilitato o disabilitato in un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="de12e-149">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="de12e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de12e-150">CommonParameters</span></span>
<span data-ttu-id="de12e-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de12e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de12e-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de12e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de12e-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de12e-153">INPUTS</span></span>

### <span data-ttu-id="de12e-154">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="de12e-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="de12e-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="de12e-155">System.Int32</span></span>

### <span data-ttu-id="de12e-156">System. String</span><span class="sxs-lookup"><span data-stu-id="de12e-156">System.String</span></span>

### <span data-ttu-id="de12e-157">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="de12e-157">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="de12e-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de12e-158">OUTPUTS</span></span>

### <span data-ttu-id="de12e-159">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="de12e-159">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="de12e-160">Note</span><span class="sxs-lookup"><span data-stu-id="de12e-160">NOTES</span></span>

## <span data-ttu-id="de12e-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de12e-161">RELATED LINKS</span></span>
