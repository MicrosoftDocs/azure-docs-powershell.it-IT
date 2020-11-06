---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 2f961f144bc322cb1b1b12001ed006bc783ed67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518180"
---
# <span data-ttu-id="098ee-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="098ee-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="098ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="098ee-102">SYNOPSIS</span></span>
<span data-ttu-id="098ee-103">Modifica le proprietà di un disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="098ee-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="098ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="098ee-104">SYNTAX</span></span>

### <span data-ttu-id="098ee-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="098ee-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="098ee-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="098ee-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="098ee-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="098ee-107">DESCRIPTION</span></span>
<span data-ttu-id="098ee-108">Il cmdlet **set-AzureRmVMDataDisk** modifica le proprietà di un disco di dati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="098ee-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="098ee-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="098ee-109">EXAMPLES</span></span>

### <span data-ttu-id="098ee-110">Esempio 1: modificare la modalità di memorizzazione nella cache di un disco di dati</span><span class="sxs-lookup"><span data-stu-id="098ee-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="098ee-111">Il primo comando ottiene la macchina virtuale denominata ContosoVM07 tramite **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="098ee-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="098ee-112">Il comando lo archivia nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="098ee-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="098ee-113">Il secondo comando consente di modificare la modalità di memorizzazione nella cache per il disco di dati denominato DataDisk01 nella macchina virtuale in $VM.</span><span class="sxs-lookup"><span data-stu-id="098ee-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="098ee-114">Il comando passa il risultato al cmdlet Update-AzureRmVM, che implementa le modifiche.</span><span class="sxs-lookup"><span data-stu-id="098ee-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="098ee-115">Una modifica alla modalità di memorizzazione nella cache fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="098ee-115">A change to the caching mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="098ee-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="098ee-116">PARAMETERS</span></span>

### <span data-ttu-id="098ee-117">-Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="098ee-117">-Caching</span></span>
<span data-ttu-id="098ee-118">Specifica la modalità di memorizzazione nella cache del disco.</span><span class="sxs-lookup"><span data-stu-id="098ee-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="098ee-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="098ee-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="098ee-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="098ee-120">ReadOnly</span></span>
- <span data-ttu-id="098ee-121">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="098ee-121">ReadWrite</span></span>

<span data-ttu-id="098ee-122">Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="098ee-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="098ee-123">La modifica di questo valore fa sì che la macchina virtuale venga riavviata.</span><span class="sxs-lookup"><span data-stu-id="098ee-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="098ee-124">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="098ee-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="098ee-125">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="098ee-125">-DiskSizeInGB</span></span>
<span data-ttu-id="098ee-126">Specifica le dimensioni, in gigabyte, per il disco dati.</span><span class="sxs-lookup"><span data-stu-id="098ee-126">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="098ee-127">-Lun</span><span class="sxs-lookup"><span data-stu-id="098ee-127">-Lun</span></span>
<span data-ttu-id="098ee-128">Specifica il numero di unità logica (LUN) del disco di dati modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="098ee-128">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="098ee-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="098ee-129">-Name</span></span>
<span data-ttu-id="098ee-130">Specifica il nome del disco di dati modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="098ee-130">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="098ee-131">-VM</span><span class="sxs-lookup"><span data-stu-id="098ee-131">-VM</span></span>
<span data-ttu-id="098ee-132">Specifica la macchina virtuale per cui questo cmdlet modifica un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="098ee-132">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="098ee-133">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="098ee-133">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="098ee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098ee-134">CommonParameters</span></span>
<span data-ttu-id="098ee-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="098ee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098ee-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="098ee-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098ee-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="098ee-137">INPUTS</span></span>

### <span data-ttu-id="098ee-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="098ee-138">None</span></span>
<span data-ttu-id="098ee-139">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="098ee-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="098ee-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="098ee-140">OUTPUTS</span></span>

## <span data-ttu-id="098ee-141">Note</span><span class="sxs-lookup"><span data-stu-id="098ee-141">NOTES</span></span>

## <span data-ttu-id="098ee-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="098ee-142">RELATED LINKS</span></span>

[<span data-ttu-id="098ee-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="098ee-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="098ee-144">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="098ee-144">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


