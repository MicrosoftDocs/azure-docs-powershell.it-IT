---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 882b9f0afe9670f9e7b6f0651b3f3a96003d4668
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863829"
---
# <span data-ttu-id="118cf-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="118cf-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="118cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="118cf-102">SYNOPSIS</span></span>
<span data-ttu-id="118cf-103">Converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="118cf-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="118cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="118cf-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="118cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="118cf-105">DESCRIPTION</span></span>
<span data-ttu-id="118cf-106">Il cmdlet **ConvertTo-AzVMManagedDisk** converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="118cf-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="118cf-107">Prima di richiamare l'operazione, la macchina virtuale deve essere arrestata.</span><span class="sxs-lookup"><span data-stu-id="118cf-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="118cf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="118cf-108">EXAMPLES</span></span>

### <span data-ttu-id="118cf-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="118cf-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="118cf-110">Questo comando converte i dischi basati su BLOB della macchina virtuale denominata "VM01" nel gruppo di risorse "ResourceGroup01" in dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="118cf-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="118cf-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="118cf-111">PARAMETERS</span></span>

### <span data-ttu-id="118cf-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="118cf-112">-AsJob</span></span>
<span data-ttu-id="118cf-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="118cf-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="118cf-114">-DefaultProfile</span></span>
<span data-ttu-id="118cf-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="118cf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="118cf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="118cf-116">-ResourceGroupName</span></span>
<span data-ttu-id="118cf-117">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="118cf-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="118cf-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="118cf-118">-VMName</span></span>
<span data-ttu-id="118cf-119">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="118cf-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="118cf-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="118cf-120">-Confirm</span></span>
<span data-ttu-id="118cf-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="118cf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="118cf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="118cf-122">-WhatIf</span></span>
<span data-ttu-id="118cf-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="118cf-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="118cf-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="118cf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="118cf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="118cf-125">CommonParameters</span></span>
<span data-ttu-id="118cf-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="118cf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="118cf-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="118cf-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="118cf-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="118cf-128">INPUTS</span></span>

### <span data-ttu-id="118cf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="118cf-129">System.String</span></span>

## <span data-ttu-id="118cf-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="118cf-130">OUTPUTS</span></span>

### <span data-ttu-id="118cf-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="118cf-131">System.Object</span></span>

## <span data-ttu-id="118cf-132">Note</span><span class="sxs-lookup"><span data-stu-id="118cf-132">NOTES</span></span>

## <span data-ttu-id="118cf-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="118cf-133">RELATED LINKS</span></span>

