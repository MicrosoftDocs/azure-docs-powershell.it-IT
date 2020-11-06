---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 4115cabbeeb2a7c458ce52e80eb251cb972491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509968"
---
# <span data-ttu-id="f6237-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="f6237-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="f6237-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6237-102">SYNOPSIS</span></span>
<span data-ttu-id="f6237-103">Rimuove un disco di dati da un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="f6237-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6237-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6237-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <Image> [-Lun] <Int32> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6237-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6237-105">DESCRIPTION</span></span>
<span data-ttu-id="f6237-106">Il cmdlet **Remove-AzureRmImageDataDisk** rimuove un disco di dati da un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="f6237-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="f6237-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6237-107">EXAMPLES</span></span>

### <span data-ttu-id="f6237-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f6237-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="f6237-109">Questo comando rimuove il disco di dati dell'unità logica numero 1 dall'immagine esistente "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f6237-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f6237-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6237-110">PARAMETERS</span></span>

### <span data-ttu-id="f6237-111">-Immagine</span><span class="sxs-lookup"><span data-stu-id="f6237-111">-Image</span></span>
<span data-ttu-id="f6237-112">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="f6237-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6237-113">-Lun</span><span class="sxs-lookup"><span data-stu-id="f6237-113">-Lun</span></span>
<span data-ttu-id="f6237-114">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="f6237-114">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6237-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f6237-115">-Confirm</span></span>
<span data-ttu-id="f6237-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6237-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6237-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6237-117">-WhatIf</span></span>
<span data-ttu-id="f6237-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6237-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6237-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6237-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6237-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6237-120">CommonParameters</span></span>
<span data-ttu-id="f6237-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6237-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6237-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6237-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6237-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6237-123">INPUTS</span></span>

### <span data-ttu-id="f6237-124">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="f6237-124">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="f6237-125">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f6237-125">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f6237-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6237-126">OUTPUTS</span></span>

### <span data-ttu-id="f6237-127">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="f6237-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="f6237-128">Note</span><span class="sxs-lookup"><span data-stu-id="f6237-128">NOTES</span></span>

## <span data-ttu-id="f6237-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6237-129">RELATED LINKS</span></span>

