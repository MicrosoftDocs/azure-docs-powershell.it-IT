---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199342"
---
# <span data-ttu-id="37a49-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="37a49-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="37a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37a49-102">SYNOPSIS</span></span>
<span data-ttu-id="37a49-103">Converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="37a49-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="37a49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37a49-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37a49-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="37a49-105">DESCRIPTION</span></span>
<span data-ttu-id="37a49-106">Il cmdlet **ConvertTo-AzVMManagedDisk** converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="37a49-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="37a49-107">La macchina virtuale deve essere deassegnata prima di richiamare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="37a49-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="37a49-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37a49-108">EXAMPLES</span></span>

### <span data-ttu-id="37a49-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="37a49-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="37a49-110">Questo comando converte i dischi basati su BLOB della macchina virtuale denominata 'VM01' nel gruppo di risorse 'ResourceGroup01' in dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="37a49-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="37a49-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37a49-111">PARAMETERS</span></span>

### <span data-ttu-id="37a49-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37a49-112">-AsJob</span></span>
<span data-ttu-id="37a49-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="37a49-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37a49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a49-114">-DefaultProfile</span></span>
<span data-ttu-id="37a49-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37a49-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37a49-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a49-116">-ResourceGroupName</span></span>
<span data-ttu-id="37a49-117">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37a49-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="37a49-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="37a49-118">-VMName</span></span>
<span data-ttu-id="37a49-119">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="37a49-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="37a49-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37a49-120">-Confirm</span></span>
<span data-ttu-id="37a49-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37a49-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37a49-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37a49-122">-WhatIf</span></span>
<span data-ttu-id="37a49-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37a49-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37a49-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37a49-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37a49-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a49-125">CommonParameters</span></span>
<span data-ttu-id="37a49-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37a49-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a49-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37a49-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a49-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="37a49-128">INPUTS</span></span>

### <span data-ttu-id="37a49-129">System.String</span><span class="sxs-lookup"><span data-stu-id="37a49-129">System.String</span></span>

## <span data-ttu-id="37a49-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37a49-130">OUTPUTS</span></span>

### <span data-ttu-id="37a49-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="37a49-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="37a49-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="37a49-132">NOTES</span></span>

## <span data-ttu-id="37a49-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37a49-133">RELATED LINKS</span></span>
