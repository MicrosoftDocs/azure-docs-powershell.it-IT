---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: bbfe3018cdf0560b7c7776217ceda7cfe7b77048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521092"
---
# <span data-ttu-id="dbdf1-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="dbdf1-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="dbdf1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbdf1-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdf1-103">Converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbdf1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbdf1-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbdf1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbdf1-105">DESCRIPTION</span></span>
<span data-ttu-id="dbdf1-106">Il cmdlet **ConvertTo-AzureRmVMManagedDisk** converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="dbdf1-107">Prima di richiamare l'operazione, la macchina virtuale deve essere arrestata.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="dbdf1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbdf1-108">EXAMPLES</span></span>

### <span data-ttu-id="dbdf1-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dbdf1-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="dbdf1-110">Questo comando converte i dischi basati su BLOB della macchina virtuale denominata "VM01" nel gruppo di risorse "ResourceGroup01" in dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="dbdf1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbdf1-111">PARAMETERS</span></span>

### <span data-ttu-id="dbdf1-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbdf1-112">-ResourceGroupName</span></span>
<span data-ttu-id="dbdf1-113">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-113">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbdf1-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="dbdf1-114">-VMName</span></span>
<span data-ttu-id="dbdf1-115">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-115">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbdf1-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dbdf1-116">-Confirm</span></span>
<span data-ttu-id="dbdf1-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbdf1-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbdf1-118">-WhatIf</span></span>
<span data-ttu-id="dbdf1-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbdf1-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbdf1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdf1-121">CommonParameters</span></span>
<span data-ttu-id="dbdf1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbdf1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdf1-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbdf1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdf1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbdf1-124">INPUTS</span></span>

### <span data-ttu-id="dbdf1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dbdf1-125">System.String</span></span>

## <span data-ttu-id="dbdf1-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbdf1-126">OUTPUTS</span></span>

### <span data-ttu-id="dbdf1-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="dbdf1-127">System.Object</span></span>

## <span data-ttu-id="dbdf1-128">Note</span><span class="sxs-lookup"><span data-stu-id="dbdf1-128">NOTES</span></span>

## <span data-ttu-id="dbdf1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbdf1-129">RELATED LINKS</span></span>

