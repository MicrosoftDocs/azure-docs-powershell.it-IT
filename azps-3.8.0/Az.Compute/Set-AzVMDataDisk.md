---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: 2361fc663efc3ec4a967c718abd778599ca5340b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022597"
---
# <span data-ttu-id="fd441-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fd441-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="fd441-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd441-102">SYNOPSIS</span></span>
<span data-ttu-id="fd441-103">Modifica le proprietà di un disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd441-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="fd441-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd441-104">SYNTAX</span></span>

### <span data-ttu-id="fd441-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="fd441-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd441-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="fd441-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd441-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd441-107">DESCRIPTION</span></span>
<span data-ttu-id="fd441-108">Il cmdlet **set-AzVMDataDisk** modifica le proprietà di un disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd441-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="fd441-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd441-109">EXAMPLES</span></span>

### <span data-ttu-id="fd441-110">Esempio 1: modificare la modalità di memorizzazione nella cache di un disco di dati</span><span class="sxs-lookup"><span data-stu-id="fd441-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="fd441-111">Il primo comando ottiene la macchina virtuale denominata ContosoVM07 tramite **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="fd441-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="fd441-112">Il comando lo archivia nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="fd441-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="fd441-113">Il secondo comando consente di modificare la modalità di memorizzazione nella cache per il disco di dati denominato DataDisk01 nella macchina virtuale in $VM.</span><span class="sxs-lookup"><span data-stu-id="fd441-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="fd441-114">Il comando passa il risultato al cmdlet Update-AzVM, che implementa le modifiche.</span><span class="sxs-lookup"><span data-stu-id="fd441-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="fd441-115">Una modifica alla modalità di incasso causa il riavvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd441-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="fd441-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd441-116">PARAMETERS</span></span>

### <span data-ttu-id="fd441-117">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="fd441-117">-Caching</span></span>
<span data-ttu-id="fd441-118">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="fd441-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="fd441-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd441-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fd441-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fd441-120">ReadOnly</span></span>
- <span data-ttu-id="fd441-121">ReadWrite il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="fd441-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="fd441-122">La modifica di questo valore fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="fd441-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="fd441-123">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="fd441-123">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd441-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd441-124">-DefaultProfile</span></span>
<span data-ttu-id="fd441-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd441-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd441-126">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="fd441-126">-DiskEncryptionSetId</span></span>
<span data-ttu-id="fd441-127">Specifica l'ID risorsa del set di crittografia disco gestito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="fd441-127">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="fd441-128">Questa operazione può essere specificata solo per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="fd441-128">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="fd441-129">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="fd441-129">-DiskSizeInGB</span></span>
<span data-ttu-id="fd441-130">Specifica le dimensioni, in gigabyte, per il disco dati.</span><span class="sxs-lookup"><span data-stu-id="fd441-130">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd441-131">-Lun</span><span class="sxs-lookup"><span data-stu-id="fd441-131">-Lun</span></span>
<span data-ttu-id="fd441-132">Specifica il numero di unità logica (LUN) del disco di dati modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd441-132">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd441-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd441-133">-Name</span></span>
<span data-ttu-id="fd441-134">Specifica il nome del disco di dati modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd441-134">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd441-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="fd441-135">-StorageAccountType</span></span>
<span data-ttu-id="fd441-136">Tipo di account del disco gestito della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd441-136">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="fd441-137">-VM</span><span class="sxs-lookup"><span data-stu-id="fd441-137">-VM</span></span>
<span data-ttu-id="fd441-138">Specifica la macchina virtuale per cui questo cmdlet modifica un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="fd441-138">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="fd441-139">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="fd441-139">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd441-140">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="fd441-140">-WriteAccelerator</span></span>
<span data-ttu-id="fd441-141">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco dati.</span><span class="sxs-lookup"><span data-stu-id="fd441-141">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="fd441-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd441-142">CommonParameters</span></span>
<span data-ttu-id="fd441-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd441-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd441-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd441-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd441-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd441-145">INPUTS</span></span>

### <span data-ttu-id="fd441-146">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fd441-146">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="fd441-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fd441-147">System.String</span></span>

### <span data-ttu-id="fd441-148">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fd441-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fd441-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fd441-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="fd441-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd441-150">OUTPUTS</span></span>

### <span data-ttu-id="fd441-151">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fd441-151">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fd441-152">Note</span><span class="sxs-lookup"><span data-stu-id="fd441-152">NOTES</span></span>

## <span data-ttu-id="fd441-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd441-153">RELATED LINKS</span></span>

[<span data-ttu-id="fd441-154">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="fd441-154">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="fd441-155">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="fd441-155">Update-AzVM</span></span>](./Update-AzVM.md)


