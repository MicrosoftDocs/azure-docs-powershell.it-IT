---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: 53ad88f6e3df11eb3a8f2f9c4b21af40b9ea614b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867135"
---
# <span data-ttu-id="3a9cf-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3a9cf-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="3a9cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9cf-103">Modifica le proprietà di un disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a9cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a9cf-104">SYNTAX</span></span>

### <span data-ttu-id="3a9cf-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="3a9cf-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a9cf-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="3a9cf-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a9cf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a9cf-107">DESCRIPTION</span></span>
<span data-ttu-id="3a9cf-108">Il cmdlet **set-AzureRmVMDataDisk** modifica le proprietà di un disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="3a9cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a9cf-109">EXAMPLES</span></span>

### <span data-ttu-id="3a9cf-110">Esempio 1: modificare la modalità di memorizzazione nella cache di un disco di dati</span><span class="sxs-lookup"><span data-stu-id="3a9cf-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="3a9cf-111">Il primo comando ottiene la macchina virtuale denominata ContosoVM07 tramite **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="3a9cf-112">Il comando lo archivia nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="3a9cf-113">Il secondo comando consente di modificare la modalità di memorizzazione nella cache per il disco di dati denominato DataDisk01 nella macchina virtuale in $VM.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="3a9cf-114">Il comando passa il risultato al cmdlet Update-AzureRmVM, che implementa le modifiche.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="3a9cf-115">Una modifica alla modalità di incasso causa il riavvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="3a9cf-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a9cf-116">PARAMETERS</span></span>

### <span data-ttu-id="3a9cf-117">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="3a9cf-117">-Caching</span></span>
<span data-ttu-id="3a9cf-118">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="3a9cf-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a9cf-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a9cf-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3a9cf-120">ReadOnly</span></span>
- <span data-ttu-id="3a9cf-121">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3a9cf-121">ReadWrite</span></span>

<span data-ttu-id="3a9cf-122">Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="3a9cf-123">La modifica di questo valore fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="3a9cf-124">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="3a9cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9cf-125">-DefaultProfile</span></span>
<span data-ttu-id="3a9cf-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a9cf-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="3a9cf-127">-DiskSizeInGB</span></span>
<span data-ttu-id="3a9cf-128">Specifica le dimensioni, in gigabyte, per il disco dati.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="3a9cf-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="3a9cf-129">-Lun</span></span>
<span data-ttu-id="3a9cf-130">Specifica il numero di unità logica (LUN) del disco di dati modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3a9cf-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a9cf-131">-Name</span></span>
<span data-ttu-id="3a9cf-132">Specifica il nome del disco di dati modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3a9cf-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3a9cf-133">-StorageAccountType</span></span>
<span data-ttu-id="3a9cf-134">Tipo di account del disco gestito della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-134">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="3a9cf-135">-VM</span><span class="sxs-lookup"><span data-stu-id="3a9cf-135">-VM</span></span>
<span data-ttu-id="3a9cf-136">Specifica la macchina virtuale per cui questo cmdlet modifica un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="3a9cf-137">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="3a9cf-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="3a9cf-138">-WriteAccelerator</span></span>
<span data-ttu-id="3a9cf-139">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco dati.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="3a9cf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9cf-140">CommonParameters</span></span>
<span data-ttu-id="3a9cf-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a9cf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9cf-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a9cf-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9cf-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a9cf-143">INPUTS</span></span>

### <span data-ttu-id="3a9cf-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3a9cf-144">PSVirtualMachine</span></span>
<span data-ttu-id="3a9cf-145">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3a9cf-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="3a9cf-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a9cf-146">OUTPUTS</span></span>

### <span data-ttu-id="3a9cf-147">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3a9cf-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3a9cf-148">Note</span><span class="sxs-lookup"><span data-stu-id="3a9cf-148">NOTES</span></span>

## <span data-ttu-id="3a9cf-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a9cf-149">RELATED LINKS</span></span>

[<span data-ttu-id="3a9cf-150">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a9cf-150">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="3a9cf-151">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a9cf-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


