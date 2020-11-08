---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031918"
---
# <span data-ttu-id="e425c-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e425c-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="e425c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e425c-102">SYNOPSIS</span></span>
<span data-ttu-id="e425c-103">Aggiunge un disco di dati a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="e425c-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="e425c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e425c-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e425c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e425c-105">DESCRIPTION</span></span>
<span data-ttu-id="e425c-106">Il cmdlet **Add-AzVmssVMDataDisk** aggiunge un disco di dati a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="e425c-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="e425c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e425c-107">EXAMPLES</span></span>

### <span data-ttu-id="e425c-108">Esempio 1: aggiungere un disco di dati gestito a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="e425c-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="e425c-109">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="e425c-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="e425c-110">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="e425c-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="e425c-111">Il comando successivo aggiunge il disco gestito alla VM vmss archiviata localmente in $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="e425c-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="e425c-112">Il comando finale aggiorna la VM vmss con il disco di dati aggiunto.</span><span class="sxs-lookup"><span data-stu-id="e425c-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="e425c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e425c-113">PARAMETERS</span></span>

### <span data-ttu-id="e425c-114">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="e425c-114">-Caching</span></span>
<span data-ttu-id="e425c-115">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="e425c-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="e425c-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e425c-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e425c-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e425c-117">ReadOnly</span></span>
- <span data-ttu-id="e425c-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e425c-118">ReadWrite</span></span>
- <span data-ttu-id="e425c-119">None il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="e425c-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="e425c-120">La modifica di questo valore fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="e425c-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="e425c-121">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="e425c-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="e425c-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e425c-122">-CreateOption</span></span>
<span data-ttu-id="e425c-123">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="e425c-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="e425c-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e425c-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e425c-125">Allegare.</span><span class="sxs-lookup"><span data-stu-id="e425c-125">Attach.</span></span>
<span data-ttu-id="e425c-126">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="e425c-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="e425c-127">Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="e425c-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="e425c-128">Il *VhdUri* è tutto ciò che serve per indicare alla piattaforma Azure la posizione del disco rigido virtuale (VHD) da allegare come disco di dati alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e425c-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="e425c-129">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="e425c-129">Empty.</span></span>
<span data-ttu-id="e425c-130">Specificalo per creare un disco dati vuoto.</span><span class="sxs-lookup"><span data-stu-id="e425c-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="e425c-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="e425c-131">FromImage.</span></span>
<span data-ttu-id="e425c-132">Specificare questa opzione per creare una macchina virtuale da un'immagine o un disco generalizzato.</span><span class="sxs-lookup"><span data-stu-id="e425c-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="e425c-133">Quando specifichi questa opzione, devi specificare il parametro *SourceImageUri* anche per indicare alla piattaforma Azure la posizione del VHD da allegare come disco di dati.</span><span class="sxs-lookup"><span data-stu-id="e425c-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="e425c-134">Il parametro *VhdUri* viene usato come posizione per identificare dove verrà archiviato il VHD del disco dati quando viene usato dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e425c-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="e425c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e425c-135">-DefaultProfile</span></span>
<span data-ttu-id="e425c-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e425c-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e425c-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e425c-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e425c-138">Specifica l'ID risorsa del set di crittografia disco gestito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="e425c-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="e425c-139">Questa operazione può essere specificata solo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="e425c-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="e425c-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e425c-140">-DiskSizeInGB</span></span>
<span data-ttu-id="e425c-141">Specifica le dimensioni, in gigabyte, di un disco vuoto da allegare a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e425c-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="e425c-142">-Lun</span><span class="sxs-lookup"><span data-stu-id="e425c-142">-Lun</span></span>
<span data-ttu-id="e425c-143">Specifica il numero di unità logica (LUN) per un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="e425c-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="e425c-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="e425c-144">-ManagedDiskId</span></span>
<span data-ttu-id="e425c-145">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="e425c-145">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="e425c-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e425c-146">-StorageAccountType</span></span>
<span data-ttu-id="e425c-147">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="e425c-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="e425c-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e425c-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="e425c-149">Specifica l'oggetto VM del set di scale della macchina virtuale locale a cui aggiungere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="e425c-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="e425c-150">Puoi usare il cmdlet **Get-AzVmssVM** per ottenere un oggetto VM set della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e425c-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="e425c-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e425c-151">-WriteAccelerator</span></span>
<span data-ttu-id="e425c-152">Specifica se WriteAccelerator deve essere abilitato o disabilitato in un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="e425c-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="e425c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e425c-153">CommonParameters</span></span>
<span data-ttu-id="e425c-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e425c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e425c-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e425c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e425c-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e425c-156">INPUTS</span></span>

### <span data-ttu-id="e425c-157">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e425c-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="e425c-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e425c-158">System.Int32</span></span>

### <span data-ttu-id="e425c-159">System. String</span><span class="sxs-lookup"><span data-stu-id="e425c-159">System.String</span></span>

### <span data-ttu-id="e425c-160">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="e425c-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="e425c-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e425c-161">OUTPUTS</span></span>

### <span data-ttu-id="e425c-162">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e425c-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="e425c-163">Note</span><span class="sxs-lookup"><span data-stu-id="e425c-163">NOTES</span></span>

## <span data-ttu-id="e425c-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e425c-164">RELATED LINKS</span></span>
