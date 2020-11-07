---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 054462398a0f7b3e8710928000f9c10fb42f04db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686008"
---
# <span data-ttu-id="b3b9c-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="b3b9c-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="b3b9c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b9c-103">Rimuove un'immagine.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3b9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3b9c-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3b9c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="b3b9c-106">Il cmdlet **Remove-AzureRmImage** rimuove un'immagine.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="b3b9c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3b9c-107">EXAMPLES</span></span>

### <span data-ttu-id="b3b9c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3b9c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="b3b9c-109">Questo comando rimuove l'immagine denominata "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b3b9c-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b3b9c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3b9c-110">PARAMETERS</span></span>

### <span data-ttu-id="b3b9c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b3b9c-111">-Force</span></span>
<span data-ttu-id="b3b9c-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b9c-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b3b9c-113">-ImageName</span></span>
<span data-ttu-id="b3b9c-114">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-114">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="b3b9c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b9c-115">-ResourceGroupName</span></span>
<span data-ttu-id="b3b9c-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b3b9c-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3b9c-117">-Confirm</span></span>
<span data-ttu-id="b3b9c-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3b9c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3b9c-119">-WhatIf</span></span>
<span data-ttu-id="b3b9c-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3b9c-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3b9c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b9c-122">CommonParameters</span></span>
<span data-ttu-id="b3b9c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b9c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b9c-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3b9c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b9c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3b9c-125">INPUTS</span></span>

### <span data-ttu-id="b3b9c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b3b9c-126">System.String</span></span>

## <span data-ttu-id="b3b9c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3b9c-127">OUTPUTS</span></span>

### <span data-ttu-id="b3b9c-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="b3b9c-128">System.Object</span></span>

## <span data-ttu-id="b3b9c-129">Note</span><span class="sxs-lookup"><span data-stu-id="b3b9c-129">NOTES</span></span>

## <span data-ttu-id="b3b9c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3b9c-130">RELATED LINKS</span></span>

