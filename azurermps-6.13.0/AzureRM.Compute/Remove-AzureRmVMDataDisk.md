---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: e0f8b1d4e47cfe488fcba02228bd35c09f4d3ac6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507583"
---
# <span data-ttu-id="b1e05-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b1e05-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="b1e05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1e05-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e05-103">Rimuove un disco dati da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b1e05-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1e05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1e05-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1e05-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1e05-105">DESCRIPTION</span></span>
<span data-ttu-id="b1e05-106">Il cmdlet **Remove-AzureRmVMDataDisk** rimuove un disco di dati da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b1e05-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="b1e05-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1e05-107">EXAMPLES</span></span>

### <span data-ttu-id="b1e05-108">Esempio 1: rimuovere un disco di dati da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b1e05-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="b1e05-109">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="b1e05-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="b1e05-110">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b1e05-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b1e05-111">Il secondo comando rimuove il disco di dati denominato Disk3 dalla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b1e05-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b1e05-112">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b1e05-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="b1e05-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1e05-113">PARAMETERS</span></span>

### <span data-ttu-id="b1e05-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="b1e05-114">-DataDiskNames</span></span>
<span data-ttu-id="b1e05-115">Specifica i nomi di uno o più dischi di dati rimossi da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1e05-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1e05-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1e05-116">-DefaultProfile</span></span>
<span data-ttu-id="b1e05-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1e05-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1e05-118">-VM</span><span class="sxs-lookup"><span data-stu-id="b1e05-118">-VM</span></span>
<span data-ttu-id="b1e05-119">Specifica l'oggetto macchina virtuale locale da cui rimuovere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="b1e05-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="b1e05-120">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="b1e05-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="b1e05-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1e05-121">-Confirm</span></span>
<span data-ttu-id="b1e05-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1e05-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1e05-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1e05-123">-WhatIf</span></span>
<span data-ttu-id="b1e05-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1e05-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1e05-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1e05-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1e05-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e05-126">CommonParameters</span></span>
<span data-ttu-id="b1e05-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1e05-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e05-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1e05-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e05-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1e05-129">INPUTS</span></span>

### <span data-ttu-id="b1e05-130">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b1e05-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b1e05-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1e05-131">OUTPUTS</span></span>

### <span data-ttu-id="b1e05-132">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b1e05-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b1e05-133">Note</span><span class="sxs-lookup"><span data-stu-id="b1e05-133">NOTES</span></span>

## <span data-ttu-id="b1e05-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1e05-134">RELATED LINKS</span></span>

[<span data-ttu-id="b1e05-135">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b1e05-135">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="b1e05-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b1e05-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


