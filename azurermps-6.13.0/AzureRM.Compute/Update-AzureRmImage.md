---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: 34c4eefe2792de239b2f3ae2a9348704497a4bd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686449"
---
# <span data-ttu-id="133a1-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="133a1-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="133a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="133a1-102">SYNOPSIS</span></span>
<span data-ttu-id="133a1-103">Aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="133a1-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="133a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="133a1-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="133a1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="133a1-105">DESCRIPTION</span></span>
<span data-ttu-id="133a1-106">Il cmdlet **Update-AzureRmImage** aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="133a1-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="133a1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="133a1-107">EXAMPLES</span></span>

### <span data-ttu-id="133a1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="133a1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="133a1-109">Questo comando rimuove il disco di dati dell'unità logica numero 1 dall'immagine esistente "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="133a1-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="133a1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="133a1-110">PARAMETERS</span></span>

### <span data-ttu-id="133a1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="133a1-111">-AsJob</span></span>
<span data-ttu-id="133a1-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="133a1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="133a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133a1-113">-DefaultProfile</span></span>
<span data-ttu-id="133a1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="133a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="133a1-115">-Immagine</span><span class="sxs-lookup"><span data-stu-id="133a1-115">-Image</span></span>
<span data-ttu-id="133a1-116">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="133a1-116">Specifies a local image object.</span></span>

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

### <span data-ttu-id="133a1-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="133a1-117">-ImageName</span></span>
<span data-ttu-id="133a1-118">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="133a1-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="133a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="133a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="133a1-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="133a1-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="133a1-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="133a1-121">-Confirm</span></span>
<span data-ttu-id="133a1-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="133a1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="133a1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="133a1-123">-WhatIf</span></span>
<span data-ttu-id="133a1-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="133a1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="133a1-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="133a1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="133a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133a1-126">CommonParameters</span></span>
<span data-ttu-id="133a1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="133a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133a1-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="133a1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133a1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="133a1-129">INPUTS</span></span>

### <span data-ttu-id="133a1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="133a1-130">System.String</span></span>

### <span data-ttu-id="133a1-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="133a1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>
<span data-ttu-id="133a1-132">Parametri: image (ByValue)</span><span class="sxs-lookup"><span data-stu-id="133a1-132">Parameters: Image (ByValue)</span></span>

## <span data-ttu-id="133a1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="133a1-133">OUTPUTS</span></span>

### <span data-ttu-id="133a1-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="133a1-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="133a1-135">Note</span><span class="sxs-lookup"><span data-stu-id="133a1-135">NOTES</span></span>

## <span data-ttu-id="133a1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="133a1-136">RELATED LINKS</span></span>
