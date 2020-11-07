---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: ea8b069be4b153e6e4ca295a917e1c3e81629094
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866562"
---
# <span data-ttu-id="95b70-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="95b70-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="95b70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95b70-102">SYNOPSIS</span></span>
<span data-ttu-id="95b70-103">Rimuove un disco dati da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="95b70-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95b70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95b70-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95b70-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95b70-105">DESCRIPTION</span></span>
<span data-ttu-id="95b70-106">Il cmdlet **Remove-AzureRmVMDataDisk** rimuove un disco di dati da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="95b70-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="95b70-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95b70-107">EXAMPLES</span></span>

### <span data-ttu-id="95b70-108">Esempio 1: rimuovere un disco di dati da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="95b70-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="95b70-109">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="95b70-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="95b70-110">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="95b70-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="95b70-111">Il secondo comando rimuove il disco di dati denominato Disk3 dalla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="95b70-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="95b70-112">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="95b70-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="95b70-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95b70-113">PARAMETERS</span></span>

### <span data-ttu-id="95b70-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="95b70-114">-DataDiskNames</span></span>
<span data-ttu-id="95b70-115">Specifica i nomi di uno o più dischi di dati rimossi da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95b70-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="95b70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b70-116">-DefaultProfile</span></span>
<span data-ttu-id="95b70-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95b70-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95b70-118">-VM</span><span class="sxs-lookup"><span data-stu-id="95b70-118">-VM</span></span>
<span data-ttu-id="95b70-119">Specifica l'oggetto macchina virtuale locale da cui rimuovere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="95b70-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="95b70-120">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="95b70-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="95b70-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="95b70-121">-Confirm</span></span>
<span data-ttu-id="95b70-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95b70-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="95b70-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95b70-123">-WhatIf</span></span>
<span data-ttu-id="95b70-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95b70-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95b70-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95b70-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="95b70-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b70-126">CommonParameters</span></span>
<span data-ttu-id="95b70-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95b70-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b70-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b70-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b70-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95b70-129">INPUTS</span></span>

### <span data-ttu-id="95b70-130">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="95b70-130">PSVirtualMachine</span></span>
<span data-ttu-id="95b70-131">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="95b70-131">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="95b70-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95b70-132">OUTPUTS</span></span>

### <span data-ttu-id="95b70-133">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="95b70-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="95b70-134">Note</span><span class="sxs-lookup"><span data-stu-id="95b70-134">NOTES</span></span>

## <span data-ttu-id="95b70-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95b70-135">RELATED LINKS</span></span>

[<span data-ttu-id="95b70-136">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="95b70-136">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="95b70-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95b70-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


