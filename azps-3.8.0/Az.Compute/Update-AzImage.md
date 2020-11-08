---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020621"
---
# <span data-ttu-id="e0014-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e0014-101">Update-AzImage</span></span>

## <span data-ttu-id="e0014-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0014-102">SYNOPSIS</span></span>
<span data-ttu-id="e0014-103">Aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="e0014-103">Updates an image.</span></span>

## <span data-ttu-id="e0014-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0014-104">SYNTAX</span></span>

### <span data-ttu-id="e0014-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0014-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0014-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e0014-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0014-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e0014-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0014-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0014-108">DESCRIPTION</span></span>
<span data-ttu-id="e0014-109">Il cmdlet **Update-aziming** aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="e0014-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="e0014-110">Attualmente solo i tag possono essere aggiornati.</span><span class="sxs-lookup"><span data-stu-id="e0014-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="e0014-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0014-111">EXAMPLES</span></span>

### <span data-ttu-id="e0014-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e0014-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="e0014-113">Questo comando Aggiorna il valore di tag dell'immagine esistente "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e0014-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e0014-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0014-114">PARAMETERS</span></span>

### <span data-ttu-id="e0014-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0014-115">-AsJob</span></span>
<span data-ttu-id="e0014-116">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="e0014-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e0014-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0014-117">-DefaultProfile</span></span>
<span data-ttu-id="e0014-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0014-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0014-119">-Immagine</span><span class="sxs-lookup"><span data-stu-id="e0014-119">-Image</span></span>
<span data-ttu-id="e0014-120">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="e0014-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0014-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e0014-121">-ImageName</span></span>
<span data-ttu-id="e0014-122">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="e0014-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0014-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0014-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0014-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e0014-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0014-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0014-125">-ResourceId</span></span>
<span data-ttu-id="e0014-126">ID risorsa per l'immagine</span><span class="sxs-lookup"><span data-stu-id="e0014-126">The resource Id for the image</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0014-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0014-127">-Tag</span></span>
<span data-ttu-id="e0014-128">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="e0014-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0014-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0014-129">-Confirm</span></span>
<span data-ttu-id="e0014-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0014-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0014-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0014-131">-WhatIf</span></span>
<span data-ttu-id="e0014-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0014-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0014-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0014-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0014-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0014-134">CommonParameters</span></span>
<span data-ttu-id="e0014-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0014-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0014-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0014-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0014-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0014-137">INPUTS</span></span>

### <span data-ttu-id="e0014-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e0014-138">System.String</span></span>

### <span data-ttu-id="e0014-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="e0014-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e0014-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0014-140">OUTPUTS</span></span>

### <span data-ttu-id="e0014-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="e0014-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e0014-142">Note</span><span class="sxs-lookup"><span data-stu-id="e0014-142">NOTES</span></span>

## <span data-ttu-id="e0014-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0014-143">RELATED LINKS</span></span>
