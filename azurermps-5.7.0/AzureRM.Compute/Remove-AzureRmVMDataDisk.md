---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 3c1edb8302ac0921a8f396230637b842d88eab77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686006"
---
# <span data-ttu-id="3ac71-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3ac71-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="3ac71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ac71-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac71-103">Rimuove un disco dati da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ac71-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ac71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ac71-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ac71-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ac71-105">DESCRIPTION</span></span>
<span data-ttu-id="3ac71-106">Il cmdlet **Remove-AzureRmVMDataDisk** rimuove un disco di dati da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ac71-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="3ac71-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ac71-107">EXAMPLES</span></span>

### <span data-ttu-id="3ac71-108">Esempio 1: rimuovere un disco di dati da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="3ac71-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="3ac71-109">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="3ac71-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="3ac71-110">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="3ac71-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="3ac71-111">Il secondo comando rimuove il disco di dati denominato Disk3 dalla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="3ac71-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="3ac71-112">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3ac71-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="3ac71-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ac71-113">PARAMETERS</span></span>

### <span data-ttu-id="3ac71-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="3ac71-114">-DataDiskNames</span></span>
<span data-ttu-id="3ac71-115">Specifica i nomi di uno o più dischi di dati rimossi da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ac71-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac71-116">-VM</span><span class="sxs-lookup"><span data-stu-id="3ac71-116">-VM</span></span>
<span data-ttu-id="3ac71-117">Specifica l'oggetto macchina virtuale locale da cui rimuovere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="3ac71-117">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="3ac71-118">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="3ac71-118">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="3ac71-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ac71-119">-Confirm</span></span>
<span data-ttu-id="3ac71-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ac71-120">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac71-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ac71-121">-WhatIf</span></span>
<span data-ttu-id="3ac71-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ac71-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ac71-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ac71-123">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac71-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac71-124">CommonParameters</span></span>
<span data-ttu-id="3ac71-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ac71-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac71-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ac71-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac71-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ac71-127">INPUTS</span></span>

### <span data-ttu-id="3ac71-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3ac71-128">None</span></span>
<span data-ttu-id="3ac71-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3ac71-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ac71-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ac71-130">OUTPUTS</span></span>

## <span data-ttu-id="3ac71-131">Note</span><span class="sxs-lookup"><span data-stu-id="3ac71-131">NOTES</span></span>

## <span data-ttu-id="3ac71-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ac71-132">RELATED LINKS</span></span>

[<span data-ttu-id="3ac71-133">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3ac71-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="3ac71-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3ac71-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


