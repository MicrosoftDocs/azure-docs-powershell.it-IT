---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: ccca83cdbebcf73df9059807dc5b030e4ab21736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686586"
---
# <span data-ttu-id="7bc4c-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="7bc4c-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="7bc4c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7bc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc4c-103">Aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bc4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bc4c-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bc4c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bc4c-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc4c-106">Il cmdlet **Update-AzureRmImage** aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="7bc4c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bc4c-107">EXAMPLES</span></span>

### <span data-ttu-id="7bc4c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7bc4c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="7bc4c-109">Questo comando rimuove il disco di dati dell'unità logica numero 1 dall'immagine esistente "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="7bc4c-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7bc4c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7bc4c-110">PARAMETERS</span></span>

### <span data-ttu-id="7bc4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc4c-111">-DefaultProfile</span></span>
<span data-ttu-id="7bc4c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bc4c-113">-Immagine</span><span class="sxs-lookup"><span data-stu-id="7bc4c-113">-Image</span></span>
<span data-ttu-id="7bc4c-114">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc4c-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="7bc4c-115">-ImageName</span></span>
<span data-ttu-id="7bc4c-116">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-116">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="7bc4c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc4c-117">-ResourceGroupName</span></span>
<span data-ttu-id="7bc4c-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7bc4c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7bc4c-119">-Confirm</span></span>
<span data-ttu-id="7bc4c-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bc4c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc4c-121">-WhatIf</span></span>
<span data-ttu-id="7bc4c-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bc4c-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bc4c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc4c-124">CommonParameters</span></span>
<span data-ttu-id="7bc4c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc4c-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc4c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc4c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7bc4c-127">INPUTS</span></span>

### <span data-ttu-id="7bc4c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7bc4c-128">System.String</span></span>
<span data-ttu-id="7bc4c-129">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="7bc4c-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="7bc4c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bc4c-130">OUTPUTS</span></span>

### <span data-ttu-id="7bc4c-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="7bc4c-131">System.Object</span></span>

## <span data-ttu-id="7bc4c-132">Note</span><span class="sxs-lookup"><span data-stu-id="7bc4c-132">NOTES</span></span>

## <span data-ttu-id="7bc4c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bc4c-133">RELATED LINKS</span></span>

