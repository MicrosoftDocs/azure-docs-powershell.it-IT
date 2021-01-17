---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477867"
---
# <span data-ttu-id="ed926-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ed926-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="ed926-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed926-102">SYNOPSIS</span></span>
<span data-ttu-id="ed926-103">Converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="ed926-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="ed926-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed926-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed926-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed926-105">DESCRIPTION</span></span>
<span data-ttu-id="ed926-106">Il cmdlet **ConvertTo-AzVMManagedDisk** converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="ed926-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="ed926-107">Prima di richiamare l'operazione, la macchina virtuale deve essere arrestata.</span><span class="sxs-lookup"><span data-stu-id="ed926-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="ed926-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed926-108">EXAMPLES</span></span>

### <span data-ttu-id="ed926-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed926-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="ed926-110">Questo comando converte i dischi basati su BLOB della macchina virtuale denominata "VM01" nel gruppo di risorse "ResourceGroup01" in dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="ed926-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="ed926-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed926-111">PARAMETERS</span></span>

### <span data-ttu-id="ed926-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed926-112">-AsJob</span></span>
<span data-ttu-id="ed926-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ed926-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed926-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed926-114">-DefaultProfile</span></span>
<span data-ttu-id="ed926-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed926-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed926-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed926-116">-ResourceGroupName</span></span>
<span data-ttu-id="ed926-117">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ed926-117">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="ed926-118">-VMName</span></span>
<span data-ttu-id="ed926-119">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ed926-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed926-120">-Confirm</span></span>
<span data-ttu-id="ed926-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed926-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed926-122">-WhatIf</span></span>
<span data-ttu-id="ed926-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed926-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed926-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed926-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed926-125">CommonParameters</span></span>
<span data-ttu-id="ed926-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed926-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed926-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed926-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed926-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed926-128">INPUTS</span></span>

### <span data-ttu-id="ed926-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ed926-129">System.String</span></span>

## <span data-ttu-id="ed926-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed926-130">OUTPUTS</span></span>

### <span data-ttu-id="ed926-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ed926-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ed926-132">Note</span><span class="sxs-lookup"><span data-stu-id="ed926-132">NOTES</span></span>

## <span data-ttu-id="ed926-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed926-133">RELATED LINKS</span></span>
