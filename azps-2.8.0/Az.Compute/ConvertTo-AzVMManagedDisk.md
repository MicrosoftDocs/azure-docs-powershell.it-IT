---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 71cbd99ccd34341eb996cd4015f9e8c39d9c7fa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675453"
---
# <span data-ttu-id="670df-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="670df-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="670df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="670df-102">SYNOPSIS</span></span>
<span data-ttu-id="670df-103">Converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="670df-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="670df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="670df-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="670df-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="670df-105">DESCRIPTION</span></span>
<span data-ttu-id="670df-106">Il cmdlet **ConvertTo-AzVMManagedDisk** converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="670df-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="670df-107">Prima di richiamare l'operazione, la macchina virtuale deve essere arrestata.</span><span class="sxs-lookup"><span data-stu-id="670df-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="670df-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="670df-108">EXAMPLES</span></span>

### <span data-ttu-id="670df-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="670df-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="670df-110">Questo comando converte i dischi basati su BLOB della macchina virtuale denominata "VM01" nel gruppo di risorse "ResourceGroup01" in dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="670df-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="670df-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="670df-111">PARAMETERS</span></span>

### <span data-ttu-id="670df-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="670df-112">-AsJob</span></span>
<span data-ttu-id="670df-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="670df-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="670df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670df-114">-DefaultProfile</span></span>
<span data-ttu-id="670df-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="670df-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="670df-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670df-116">-ResourceGroupName</span></span>
<span data-ttu-id="670df-117">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="670df-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="670df-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="670df-118">-VMName</span></span>
<span data-ttu-id="670df-119">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="670df-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="670df-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="670df-120">-Confirm</span></span>
<span data-ttu-id="670df-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="670df-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="670df-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="670df-122">-WhatIf</span></span>
<span data-ttu-id="670df-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="670df-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="670df-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="670df-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="670df-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670df-125">CommonParameters</span></span>
<span data-ttu-id="670df-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="670df-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670df-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="670df-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670df-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="670df-128">INPUTS</span></span>

### <span data-ttu-id="670df-129">System. String</span><span class="sxs-lookup"><span data-stu-id="670df-129">System.String</span></span>

## <span data-ttu-id="670df-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="670df-130">OUTPUTS</span></span>

### <span data-ttu-id="670df-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="670df-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="670df-132">Note</span><span class="sxs-lookup"><span data-stu-id="670df-132">NOTES</span></span>

## <span data-ttu-id="670df-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="670df-133">RELATED LINKS</span></span>