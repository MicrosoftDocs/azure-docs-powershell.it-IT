---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: b7c5155706b968973bef6a5cf1ce2285caee819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508284"
---
# <span data-ttu-id="cf358-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="cf358-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="cf358-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf358-102">SYNOPSIS</span></span>
<span data-ttu-id="cf358-103">Aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="cf358-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf358-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf358-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf358-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf358-105">DESCRIPTION</span></span>
<span data-ttu-id="cf358-106">Il cmdlet **Update-AzureRmImage** aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="cf358-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="cf358-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf358-107">EXAMPLES</span></span>

### <span data-ttu-id="cf358-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cf358-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="cf358-109">Questo comando rimuove il disco di dati dell'unità logica numero 1 dall'immagine esistente "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cf358-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cf358-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf358-110">PARAMETERS</span></span>

### <span data-ttu-id="cf358-111">-Immagine</span><span class="sxs-lookup"><span data-stu-id="cf358-111">-Image</span></span>
<span data-ttu-id="cf358-112">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="cf358-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf358-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="cf358-113">-ImageName</span></span>
<span data-ttu-id="cf358-114">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="cf358-114">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="cf358-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf358-115">-ResourceGroupName</span></span>
<span data-ttu-id="cf358-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf358-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cf358-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf358-117">-Confirm</span></span>
<span data-ttu-id="cf358-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf358-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf358-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf358-119">-WhatIf</span></span>
<span data-ttu-id="cf358-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf358-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf358-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf358-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf358-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf358-122">CommonParameters</span></span>
<span data-ttu-id="cf358-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf358-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf358-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf358-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf358-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf358-125">INPUTS</span></span>

### <span data-ttu-id="cf358-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cf358-126">System.String</span></span>
<span data-ttu-id="cf358-127">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="cf358-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="cf358-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf358-128">OUTPUTS</span></span>

### <span data-ttu-id="cf358-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="cf358-129">System.Object</span></span>

## <span data-ttu-id="cf358-130">Note</span><span class="sxs-lookup"><span data-stu-id="cf358-130">NOTES</span></span>

## <span data-ttu-id="cf358-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf358-131">RELATED LINKS</span></span>

