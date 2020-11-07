---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/convertto-azurermvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: 4aabd2a7b6e8b4b0b9037fc14189a0e14fdf8920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686260"
---
# <span data-ttu-id="5198f-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="5198f-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="5198f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5198f-102">SYNOPSIS</span></span>
<span data-ttu-id="5198f-103">Converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="5198f-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5198f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5198f-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5198f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5198f-105">DESCRIPTION</span></span>
<span data-ttu-id="5198f-106">Il cmdlet **ConvertTo-AzureRmVMManagedDisk** converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="5198f-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="5198f-107">Prima di richiamare l'operazione, la macchina virtuale deve essere arrestata.</span><span class="sxs-lookup"><span data-stu-id="5198f-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="5198f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5198f-108">EXAMPLES</span></span>

### <span data-ttu-id="5198f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5198f-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="5198f-110">Questo comando converte i dischi basati su BLOB della macchina virtuale denominata "VM01" nel gruppo di risorse "ResourceGroup01" in dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="5198f-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="5198f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5198f-111">PARAMETERS</span></span>

### <span data-ttu-id="5198f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5198f-112">-AsJob</span></span>
<span data-ttu-id="5198f-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5198f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5198f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5198f-114">-DefaultProfile</span></span>
<span data-ttu-id="5198f-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5198f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5198f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5198f-116">-ResourceGroupName</span></span>
<span data-ttu-id="5198f-117">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5198f-117">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5198f-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="5198f-118">-VMName</span></span>
<span data-ttu-id="5198f-119">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5198f-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5198f-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5198f-120">-Confirm</span></span>
<span data-ttu-id="5198f-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5198f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5198f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5198f-122">-WhatIf</span></span>
<span data-ttu-id="5198f-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5198f-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5198f-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5198f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5198f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5198f-125">CommonParameters</span></span>
<span data-ttu-id="5198f-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5198f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5198f-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5198f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5198f-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5198f-128">INPUTS</span></span>

### <span data-ttu-id="5198f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5198f-129">System.String</span></span>

## <span data-ttu-id="5198f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5198f-130">OUTPUTS</span></span>

### <span data-ttu-id="5198f-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5198f-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5198f-132">Note</span><span class="sxs-lookup"><span data-stu-id="5198f-132">NOTES</span></span>

## <span data-ttu-id="5198f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5198f-133">RELATED LINKS</span></span>
