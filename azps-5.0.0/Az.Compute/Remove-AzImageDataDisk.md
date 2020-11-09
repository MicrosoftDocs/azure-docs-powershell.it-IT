---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 20399a1b62062afa5585e78a9fdb229ad3781d33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300696"
---
# <span data-ttu-id="48f67-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="48f67-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="48f67-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48f67-102">SYNOPSIS</span></span>
<span data-ttu-id="48f67-103">Rimuove un disco di dati da un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="48f67-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="48f67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48f67-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48f67-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48f67-105">DESCRIPTION</span></span>
<span data-ttu-id="48f67-106">Il cmdlet **Remove-AzImageDataDisk** rimuove un disco di dati da un oggetto Image.</span><span class="sxs-lookup"><span data-stu-id="48f67-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="48f67-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48f67-107">EXAMPLES</span></span>

### <span data-ttu-id="48f67-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48f67-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="48f67-109">Questo comando rimuove il disco di dati dell'unità logica numero 1 dall'immagine esistente "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="48f67-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="48f67-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48f67-110">PARAMETERS</span></span>

### <span data-ttu-id="48f67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f67-111">-DefaultProfile</span></span>
<span data-ttu-id="48f67-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48f67-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f67-113">-Immagine</span><span class="sxs-lookup"><span data-stu-id="48f67-113">-Image</span></span>
<span data-ttu-id="48f67-114">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="48f67-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="48f67-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="48f67-115">-Lun</span></span>
<span data-ttu-id="48f67-116">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="48f67-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="48f67-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="48f67-117">-Confirm</span></span>
<span data-ttu-id="48f67-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48f67-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48f67-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f67-119">-WhatIf</span></span>
<span data-ttu-id="48f67-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48f67-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48f67-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48f67-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48f67-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f67-122">CommonParameters</span></span>
<span data-ttu-id="48f67-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48f67-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f67-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48f67-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f67-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48f67-125">INPUTS</span></span>

### <span data-ttu-id="48f67-126">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="48f67-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="48f67-127">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="48f67-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="48f67-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48f67-128">OUTPUTS</span></span>

### <span data-ttu-id="48f67-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="48f67-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="48f67-130">Note</span><span class="sxs-lookup"><span data-stu-id="48f67-130">NOTES</span></span>

## <span data-ttu-id="48f67-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48f67-131">RELATED LINKS</span></span>
