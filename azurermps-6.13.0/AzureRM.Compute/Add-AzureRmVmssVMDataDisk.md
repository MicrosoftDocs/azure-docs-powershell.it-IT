---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssVMDataDisk.md
ms.openlocfilehash: c4a4aa530f29de93458f618dbf45f639fe873f1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517492"
---
# <span data-ttu-id="06276-101">Add-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="06276-101">Add-AzureRmVmssVMDataDisk</span></span>

## <span data-ttu-id="06276-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06276-102">SYNOPSIS</span></span>
<span data-ttu-id="06276-103">Aggiunge un disco di dati a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="06276-103">Adds a data disk to a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06276-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06276-104">SYNTAX</span></span>

```
Add-AzureRmVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06276-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06276-105">DESCRIPTION</span></span>
<span data-ttu-id="06276-106">Il cmdlet **Add-AzureRmVmssVMDataDisk** aggiunge un disco di dati a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="06276-106">The **Add-AzureRmVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="06276-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06276-107">EXAMPLES</span></span>

### <span data-ttu-id="06276-108">Esempio 1: aggiungere un disco di dati gestito a una VM vmss.</span><span class="sxs-lookup"><span data-stu-id="06276-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="06276-109">Il primo comando ottiene un disco gestito esistente.</span><span class="sxs-lookup"><span data-stu-id="06276-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="06276-110">Il comando successivo consente di ottenere una VM vmss esistente specificata dal nome del gruppo di risorse, dal nome vmss e dall'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="06276-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="06276-111">Il comando successivo aggiunge il disco gestito alla VM vmss archiviata localmente in $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="06276-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="06276-112">Il comando finale aggiorna la VM vmss con il disco di dati aggiunto.</span><span class="sxs-lookup"><span data-stu-id="06276-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="06276-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06276-113">PARAMETERS</span></span>

### <span data-ttu-id="06276-114">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="06276-114">-Caching</span></span>
<span data-ttu-id="06276-115">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="06276-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="06276-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="06276-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06276-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="06276-117">ReadOnly</span></span>
- <span data-ttu-id="06276-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="06276-118">ReadWrite</span></span>
- <span data-ttu-id="06276-119">None il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="06276-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="06276-120">La modifica di questo valore fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="06276-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="06276-121">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="06276-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="06276-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="06276-122">-CreateOption</span></span>
<span data-ttu-id="06276-123">Specifica se questo cmdlet crea un disco nella macchina virtuale da una piattaforma o da un'immagine utente, crea un disco vuoto o allega un disco esistente.</span><span class="sxs-lookup"><span data-stu-id="06276-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="06276-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="06276-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06276-125">Allegare.</span><span class="sxs-lookup"><span data-stu-id="06276-125">Attach.</span></span>
<span data-ttu-id="06276-126">Specificare questa opzione per creare una macchina virtuale da un disco specializzato.</span><span class="sxs-lookup"><span data-stu-id="06276-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="06276-127">Quando specifichi questa opzione, non specificare il parametro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="06276-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="06276-128">Il *VhdUri* è tutto ciò che serve per indicare alla piattaforma Azure la posizione del disco rigido virtuale (VHD) da allegare come disco di dati alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06276-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="06276-129">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="06276-129">Empty.</span></span>
<span data-ttu-id="06276-130">Specificalo per creare un disco dati vuoto.</span><span class="sxs-lookup"><span data-stu-id="06276-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="06276-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="06276-131">FromImage.</span></span>
<span data-ttu-id="06276-132">Specificare questa opzione per creare una macchina virtuale da un'immagine o un disco generalizzato.</span><span class="sxs-lookup"><span data-stu-id="06276-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="06276-133">Quando specifichi questa opzione, devi specificare il parametro *SourceImageUri* anche per indicare alla piattaforma Azure la posizione del VHD da allegare come disco di dati.</span><span class="sxs-lookup"><span data-stu-id="06276-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="06276-134">Il parametro *VhdUri* viene usato come posizione per identificare dove verrà archiviato il VHD del disco dati quando viene usato dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06276-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="06276-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06276-135">-DefaultProfile</span></span>
<span data-ttu-id="06276-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06276-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06276-137">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="06276-137">-DiskSizeInGB</span></span>
<span data-ttu-id="06276-138">Specifica le dimensioni, in gigabyte, di un disco vuoto da allegare a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06276-138">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="06276-139">-Lun</span><span class="sxs-lookup"><span data-stu-id="06276-139">-Lun</span></span>
<span data-ttu-id="06276-140">Specifica il numero di unità logica (LUN) per un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="06276-140">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="06276-141">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="06276-141">-ManagedDiskId</span></span>
<span data-ttu-id="06276-142">Specifica l'ID di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="06276-142">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="06276-143">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="06276-143">-StorageAccountType</span></span>
<span data-ttu-id="06276-144">Specifica il tipo di account di archiviazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="06276-144">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="06276-145">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="06276-145">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="06276-146">Specifica l'oggetto VM del set di scale della macchina virtuale locale a cui aggiungere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="06276-146">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="06276-147">Puoi usare il cmdlet **Get-AzureRmVmssVM** per ottenere un oggetto VM set della scala della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="06276-147">You can use the **Get-AzureRmVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06276-148">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="06276-148">-WriteAccelerator</span></span>
<span data-ttu-id="06276-149">Specifica se WriteAccelerator deve essere abilitato o disabilitato in un disco dati gestito.</span><span class="sxs-lookup"><span data-stu-id="06276-149">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="06276-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06276-150">CommonParameters</span></span>
<span data-ttu-id="06276-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06276-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06276-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06276-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06276-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06276-153">INPUTS</span></span>

### <span data-ttu-id="06276-154">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="06276-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="06276-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="06276-155">System.Int32</span></span>

### <span data-ttu-id="06276-156">System. String</span><span class="sxs-lookup"><span data-stu-id="06276-156">System.String</span></span>

### <span data-ttu-id="06276-157">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="06276-157">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="06276-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06276-158">OUTPUTS</span></span>

### <span data-ttu-id="06276-159">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="06276-159">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="06276-160">Note</span><span class="sxs-lookup"><span data-stu-id="06276-160">NOTES</span></span>

## <span data-ttu-id="06276-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06276-161">RELATED LINKS</span></span>
