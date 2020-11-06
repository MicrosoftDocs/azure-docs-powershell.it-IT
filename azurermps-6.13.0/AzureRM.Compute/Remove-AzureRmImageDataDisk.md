---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 8ff2544aab072842ed851ae0c3768f57d180186d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511823"
---
# <span data-ttu-id="69ddc-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="69ddc-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="69ddc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="69ddc-103">Rimuove un disco di dati da un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="69ddc-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69ddc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69ddc-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69ddc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69ddc-105">DESCRIPTION</span></span>
<span data-ttu-id="69ddc-106">Il cmdlet **Remove-AzureRmImageDataDisk** rimuove un disco di dati da un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="69ddc-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="69ddc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69ddc-107">EXAMPLES</span></span>

### <span data-ttu-id="69ddc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="69ddc-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="69ddc-109">Questo comando rimuove il disco di dati dell'unità logica numero 1 dall'immagine esistente "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="69ddc-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="69ddc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69ddc-110">PARAMETERS</span></span>

### <span data-ttu-id="69ddc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ddc-111">-DefaultProfile</span></span>
<span data-ttu-id="69ddc-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69ddc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69ddc-113">-Immagine</span><span class="sxs-lookup"><span data-stu-id="69ddc-113">-Image</span></span>
<span data-ttu-id="69ddc-114">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="69ddc-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ddc-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="69ddc-115">-Lun</span></span>
<span data-ttu-id="69ddc-116">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="69ddc-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ddc-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="69ddc-117">-Confirm</span></span>
<span data-ttu-id="69ddc-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69ddc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69ddc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69ddc-119">-WhatIf</span></span>
<span data-ttu-id="69ddc-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69ddc-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69ddc-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69ddc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69ddc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ddc-122">CommonParameters</span></span>
<span data-ttu-id="69ddc-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ddc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ddc-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ddc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ddc-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69ddc-125">INPUTS</span></span>

### <span data-ttu-id="69ddc-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="69ddc-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="69ddc-127">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="69ddc-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="69ddc-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69ddc-128">OUTPUTS</span></span>

### <span data-ttu-id="69ddc-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="69ddc-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="69ddc-130">Note</span><span class="sxs-lookup"><span data-stu-id="69ddc-130">NOTES</span></span>

## <span data-ttu-id="69ddc-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69ddc-131">RELATED LINKS</span></span>
