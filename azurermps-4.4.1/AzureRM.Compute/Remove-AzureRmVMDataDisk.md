---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 774166f88e4ca94e5e21c2b96817596c082a429c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508700"
---
# <span data-ttu-id="aeeaf-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="aeeaf-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="aeeaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aeeaf-102">SYNOPSIS</span></span>
<span data-ttu-id="aeeaf-103">Rimuove un disco dati da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeeaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aeeaf-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeeaf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aeeaf-105">DESCRIPTION</span></span>
<span data-ttu-id="aeeaf-106">Il cmdlet **Remove-AzureRmVMDataDisk** rimuove un disco di dati da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="aeeaf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aeeaf-107">EXAMPLES</span></span>

### <span data-ttu-id="aeeaf-108">Esempio 1: rimuovere un disco di dati da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="aeeaf-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="aeeaf-109">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="aeeaf-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="aeeaf-110">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="aeeaf-111">Il secondo comando rimuove il disco di dati denominato Disk3 dalla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="aeeaf-112">Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="aeeaf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aeeaf-113">PARAMETERS</span></span>

### <span data-ttu-id="aeeaf-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="aeeaf-114">-DataDiskNames</span></span>
<span data-ttu-id="aeeaf-115">Specifica i nomi di uno o più dischi di dati rimossi da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aeeaf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeeaf-116">-DefaultProfile</span></span>
<span data-ttu-id="aeeaf-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aeeaf-118">-VM</span><span class="sxs-lookup"><span data-stu-id="aeeaf-118">-VM</span></span>
<span data-ttu-id="aeeaf-119">Specifica l'oggetto macchina virtuale locale da cui rimuovere un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="aeeaf-120">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="aeeaf-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aeeaf-121">-Confirm</span></span>
<span data-ttu-id="aeeaf-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="aeeaf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeeaf-123">-WhatIf</span></span>
<span data-ttu-id="aeeaf-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aeeaf-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="aeeaf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeeaf-126">CommonParameters</span></span>
<span data-ttu-id="aeeaf-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeeaf-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeeaf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeeaf-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aeeaf-129">INPUTS</span></span>

## <span data-ttu-id="aeeaf-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aeeaf-130">OUTPUTS</span></span>

## <span data-ttu-id="aeeaf-131">Note</span><span class="sxs-lookup"><span data-stu-id="aeeaf-131">NOTES</span></span>

## <span data-ttu-id="aeeaf-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aeeaf-132">RELATED LINKS</span></span>

[<span data-ttu-id="aeeaf-133">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="aeeaf-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="aeeaf-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aeeaf-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


