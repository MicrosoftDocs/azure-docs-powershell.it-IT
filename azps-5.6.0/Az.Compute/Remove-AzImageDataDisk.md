---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 77f01dc2161188660ecdc46086e6c53a29e520f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983294"
---
# <span data-ttu-id="8e15e-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="8e15e-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="8e15e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e15e-102">SYNOPSIS</span></span>
<span data-ttu-id="8e15e-103">Rimuove un disco dati da un oggetto immagine.</span><span class="sxs-lookup"><span data-stu-id="8e15e-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="8e15e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e15e-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e15e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8e15e-105">DESCRIPTION</span></span>
<span data-ttu-id="8e15e-106">Il cmdlet **Remove-AzImageDataDisk** rimuove un disco dati da un oggetto immagine.</span><span class="sxs-lookup"><span data-stu-id="8e15e-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="8e15e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e15e-107">EXAMPLES</span></span>

### <span data-ttu-id="8e15e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8e15e-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="8e15e-109">Questo comando rimuove il disco dati dell'unità logica numero 1 dall'immagine esistente 'Image01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="8e15e-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8e15e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e15e-110">PARAMETERS</span></span>

### <span data-ttu-id="8e15e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e15e-111">-DefaultProfile</span></span>
<span data-ttu-id="8e15e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e15e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e15e-113">-Image</span><span class="sxs-lookup"><span data-stu-id="8e15e-113">-Image</span></span>
<span data-ttu-id="8e15e-114">Specifica un oggetto immagine locale.</span><span class="sxs-lookup"><span data-stu-id="8e15e-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="8e15e-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="8e15e-115">-Lun</span></span>
<span data-ttu-id="8e15e-116">Specifica il numero di unità logiche (LUN).</span><span class="sxs-lookup"><span data-stu-id="8e15e-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="8e15e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e15e-117">-Confirm</span></span>
<span data-ttu-id="8e15e-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e15e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e15e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e15e-119">-WhatIf</span></span>
<span data-ttu-id="8e15e-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e15e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e15e-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e15e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e15e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e15e-122">CommonParameters</span></span>
<span data-ttu-id="8e15e-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e15e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e15e-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8e15e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e15e-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="8e15e-125">INPUTS</span></span>

### <span data-ttu-id="8e15e-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="8e15e-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="8e15e-127">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8e15e-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8e15e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e15e-128">OUTPUTS</span></span>

### <span data-ttu-id="8e15e-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="8e15e-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="8e15e-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="8e15e-130">NOTES</span></span>

## <span data-ttu-id="8e15e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e15e-131">RELATED LINKS</span></span>
