---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 6b618511c5d3d8a636fb96fa335314bf3c4ee5bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203386"
---
# <span data-ttu-id="fbbac-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fbbac-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="fbbac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbbac-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbac-103">Rimuove un disco dati da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fbbac-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="fbbac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbbac-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbbac-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbbac-105">DESCRIPTION</span></span>
<span data-ttu-id="fbbac-106">Il cmdlet **Remove-AzVMDataDisk** rimuove un disco di dati da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fbbac-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="fbbac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbbac-107">EXAMPLES</span></span>

### <span data-ttu-id="fbbac-108">Esempio 1: rimuovere un disco di dati da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="fbbac-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="fbbac-109">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="fbbac-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="fbbac-110">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fbbac-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fbbac-111">Il secondo comando rimuove il disco di dati denominato Disk3 dalla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fbbac-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="fbbac-112">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fbbac-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="fbbac-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbbac-113">PARAMETERS</span></span>

### <span data-ttu-id="fbbac-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="fbbac-114">-DataDiskNames</span></span>
<span data-ttu-id="fbbac-115">Specifica i nomi di uno o più dischi di dati rimossi da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbbac-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbac-116">-DefaultProfile</span></span>
<span data-ttu-id="fbbac-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbbac-118">-VM</span><span class="sxs-lookup"><span data-stu-id="fbbac-118">-VM</span></span>
<span data-ttu-id="fbbac-119">Specifica l'oggetto macchina virtuale locale da cui rimuovere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="fbbac-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="fbbac-120">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="fbbac-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="fbbac-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fbbac-121">-Confirm</span></span>
<span data-ttu-id="fbbac-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbbac-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbac-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbbac-123">-WhatIf</span></span>
<span data-ttu-id="fbbac-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbbac-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbbac-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbbac-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbac-126">CommonParameters</span></span>
<span data-ttu-id="fbbac-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbac-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbbac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbac-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbbac-129">INPUTS</span></span>

### <span data-ttu-id="fbbac-130">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fbbac-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fbbac-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbbac-131">OUTPUTS</span></span>

### <span data-ttu-id="fbbac-132">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fbbac-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fbbac-133">Note</span><span class="sxs-lookup"><span data-stu-id="fbbac-133">NOTES</span></span>

## <span data-ttu-id="fbbac-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbbac-134">RELATED LINKS</span></span>

[<span data-ttu-id="fbbac-135">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fbbac-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="fbbac-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="fbbac-136">Get-AzVM</span></span>](./Get-AzVM.md)


