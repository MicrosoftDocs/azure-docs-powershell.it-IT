---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
ms.openlocfilehash: f1309453384f028c51bea20703d6ec75cc8a3a36
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867117"
---
# <span data-ttu-id="e43ea-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="e43ea-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="e43ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e43ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e43ea-103">Aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="e43ea-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e43ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e43ea-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e43ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e43ea-105">DESCRIPTION</span></span>
<span data-ttu-id="e43ea-106">Il cmdlet **Update-AzureRmImage** aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="e43ea-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="e43ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e43ea-107">EXAMPLES</span></span>

### <span data-ttu-id="e43ea-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e43ea-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="e43ea-109">Questo comando rimuove il disco di dati dell'unità logica numero 1 dall'immagine esistente "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e43ea-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e43ea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e43ea-110">PARAMETERS</span></span>

### <span data-ttu-id="e43ea-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e43ea-111">-AsJob</span></span>
<span data-ttu-id="e43ea-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e43ea-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e43ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43ea-113">-DefaultProfile</span></span>
<span data-ttu-id="e43ea-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e43ea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e43ea-115">-Immagine</span><span class="sxs-lookup"><span data-stu-id="e43ea-115">-Image</span></span>
<span data-ttu-id="e43ea-116">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="e43ea-116">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e43ea-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e43ea-117">-ImageName</span></span>
<span data-ttu-id="e43ea-118">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="e43ea-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="e43ea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43ea-119">-ResourceGroupName</span></span>
<span data-ttu-id="e43ea-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e43ea-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e43ea-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e43ea-121">-Confirm</span></span>
<span data-ttu-id="e43ea-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e43ea-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e43ea-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e43ea-123">-WhatIf</span></span>
<span data-ttu-id="e43ea-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e43ea-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e43ea-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e43ea-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e43ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43ea-126">CommonParameters</span></span>
<span data-ttu-id="e43ea-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e43ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43ea-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e43ea-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43ea-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e43ea-129">INPUTS</span></span>

### <span data-ttu-id="e43ea-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e43ea-130">System.String</span></span>
<span data-ttu-id="e43ea-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="e43ea-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e43ea-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e43ea-132">OUTPUTS</span></span>

### <span data-ttu-id="e43ea-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="e43ea-133">System.Object</span></span>

## <span data-ttu-id="e43ea-134">Note</span><span class="sxs-lookup"><span data-stu-id="e43ea-134">NOTES</span></span>

## <span data-ttu-id="e43ea-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e43ea-135">RELATED LINKS</span></span>

