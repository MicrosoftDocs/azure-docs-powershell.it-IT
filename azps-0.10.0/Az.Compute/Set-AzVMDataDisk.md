---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: b927e9b61e4d76795e35f2356b900b959a94e082
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863374"
---
# <span data-ttu-id="9e232-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9e232-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="9e232-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e232-102">SYNOPSIS</span></span>
<span data-ttu-id="9e232-103">Modifica le proprietà di un disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e232-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="9e232-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e232-104">SYNTAX</span></span>

### <span data-ttu-id="9e232-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="9e232-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e232-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="9e232-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e232-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e232-107">DESCRIPTION</span></span>
<span data-ttu-id="9e232-108">Il cmdlet **set-AzVMDataDisk** modifica le proprietà di un disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e232-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="9e232-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e232-109">EXAMPLES</span></span>

### <span data-ttu-id="9e232-110">Esempio 1: modificare la modalità di memorizzazione nella cache di un disco di dati</span><span class="sxs-lookup"><span data-stu-id="9e232-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="9e232-111">Il primo comando ottiene la macchina virtuale denominata ContosoVM07 tramite **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="9e232-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="9e232-112">Il comando lo archivia nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="9e232-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="9e232-113">Il secondo comando consente di modificare la modalità di memorizzazione nella cache per il disco di dati denominato DataDisk01 nella macchina virtuale in $VM.</span><span class="sxs-lookup"><span data-stu-id="9e232-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="9e232-114">Il comando passa il risultato al cmdlet Update-AzVM, che implementa le modifiche.</span><span class="sxs-lookup"><span data-stu-id="9e232-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="9e232-115">Una modifica alla modalità di incasso causa il riavvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e232-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="9e232-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e232-116">PARAMETERS</span></span>

### <span data-ttu-id="9e232-117">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="9e232-117">-Caching</span></span>
<span data-ttu-id="9e232-118">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="9e232-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="9e232-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e232-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e232-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9e232-120">ReadOnly</span></span>
- <span data-ttu-id="9e232-121">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9e232-121">ReadWrite</span></span>

<span data-ttu-id="9e232-122">Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="9e232-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="9e232-123">La modifica di questo valore fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="9e232-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="9e232-124">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="9e232-124">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e232-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e232-125">-DefaultProfile</span></span>
<span data-ttu-id="9e232-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e232-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e232-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="9e232-127">-DiskSizeInGB</span></span>
<span data-ttu-id="9e232-128">Specifica le dimensioni, in gigabyte, per il disco dati.</span><span class="sxs-lookup"><span data-stu-id="9e232-128">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e232-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="9e232-129">-Lun</span></span>
<span data-ttu-id="9e232-130">Specifica il numero di unità logica (LUN) del disco di dati modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e232-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e232-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e232-131">-Name</span></span>
<span data-ttu-id="9e232-132">Specifica il nome del disco di dati modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e232-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e232-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9e232-133">-StorageAccountType</span></span>
<span data-ttu-id="9e232-134">Tipo di account del disco gestito della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e232-134">The virtual machine managed disk's account type.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e232-135">-VM</span><span class="sxs-lookup"><span data-stu-id="9e232-135">-VM</span></span>
<span data-ttu-id="9e232-136">Specifica la macchina virtuale per cui questo cmdlet modifica un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="9e232-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="9e232-137">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="9e232-137">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e232-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9e232-138">-WriteAccelerator</span></span>
<span data-ttu-id="9e232-139">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco dati.</span><span class="sxs-lookup"><span data-stu-id="9e232-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e232-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e232-140">CommonParameters</span></span>
<span data-ttu-id="9e232-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e232-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e232-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e232-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e232-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e232-143">INPUTS</span></span>

### <span data-ttu-id="9e232-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9e232-144">PSVirtualMachine</span></span>
<span data-ttu-id="9e232-145">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9e232-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="9e232-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e232-146">OUTPUTS</span></span>

### <span data-ttu-id="9e232-147">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9e232-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9e232-148">Note</span><span class="sxs-lookup"><span data-stu-id="9e232-148">NOTES</span></span>

## <span data-ttu-id="9e232-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e232-149">RELATED LINKS</span></span>

[<span data-ttu-id="9e232-150">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e232-150">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9e232-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e232-151">Update-AzVM</span></span>](./Update-AzVM.md)


