---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimagedatadisk
schema: 2.0.0
ms.openlocfilehash: b7e691d3bfea45fc8fc45725ddfe782418c12ab7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866723"
---
# <span data-ttu-id="42758-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="42758-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="42758-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42758-102">SYNOPSIS</span></span>
<span data-ttu-id="42758-103">Rimuove un disco di dati da un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="42758-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42758-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42758-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42758-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42758-105">DESCRIPTION</span></span>
<span data-ttu-id="42758-106">Il cmdlet **Remove-AzureRmImageDataDisk** rimuove un disco di dati da un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="42758-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="42758-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42758-107">EXAMPLES</span></span>

### <span data-ttu-id="42758-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="42758-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="42758-109">Questo comando rimuove il disco di dati dell'unità logica numero 1 dall'immagine esistente "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="42758-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="42758-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42758-110">PARAMETERS</span></span>

### <span data-ttu-id="42758-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42758-111">-DefaultProfile</span></span>
<span data-ttu-id="42758-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42758-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42758-113">-Immagine</span><span class="sxs-lookup"><span data-stu-id="42758-113">-Image</span></span>
<span data-ttu-id="42758-114">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="42758-114">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42758-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="42758-115">-Lun</span></span>
<span data-ttu-id="42758-116">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="42758-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="42758-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="42758-117">-Confirm</span></span>
<span data-ttu-id="42758-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42758-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42758-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42758-119">-WhatIf</span></span>
<span data-ttu-id="42758-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42758-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42758-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42758-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42758-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42758-122">CommonParameters</span></span>
<span data-ttu-id="42758-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42758-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42758-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42758-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42758-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42758-125">INPUTS</span></span>

### <span data-ttu-id="42758-126">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="42758-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="42758-127">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="42758-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="42758-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42758-128">OUTPUTS</span></span>

### <span data-ttu-id="42758-129">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="42758-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="42758-130">Note</span><span class="sxs-lookup"><span data-stu-id="42758-130">NOTES</span></span>

## <span data-ttu-id="42758-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42758-131">RELATED LINKS</span></span>

