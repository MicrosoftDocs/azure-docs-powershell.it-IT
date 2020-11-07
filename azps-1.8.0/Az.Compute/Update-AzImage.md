---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 10302f75bcbdb24c838f7785804368fd4716da87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836600"
---
# <span data-ttu-id="914f8-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="914f8-101">Update-AzImage</span></span>

## <span data-ttu-id="914f8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="914f8-102">SYNOPSIS</span></span>
<span data-ttu-id="914f8-103">Aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="914f8-103">Updates an image.</span></span>

## <span data-ttu-id="914f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="914f8-104">SYNTAX</span></span>

### <span data-ttu-id="914f8-105">ObjectParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="914f8-105">ObjectParameter (Default)</span></span>
```
Update-AzImage [-Image] <PSImage> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="914f8-106">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="914f8-106">DefaultParameter</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [[-Image] <PSImage>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="914f8-107">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="914f8-107">ResourceIdParameter</span></span>
```
Update-AzImage [-ResourceId] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="914f8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="914f8-108">DESCRIPTION</span></span>
<span data-ttu-id="914f8-109">Il cmdlet **Update-aziming** aggiorna un'immagine.</span><span class="sxs-lookup"><span data-stu-id="914f8-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="914f8-110">Attualmente solo i tag possono essere aggiornati.</span><span class="sxs-lookup"><span data-stu-id="914f8-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="914f8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="914f8-111">EXAMPLES</span></span>

### <span data-ttu-id="914f8-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="914f8-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="914f8-113">Questo comando Aggiorna il valore di tag dell'immagine esistente "Image01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="914f8-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="914f8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="914f8-114">PARAMETERS</span></span>

### <span data-ttu-id="914f8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="914f8-115">-AsJob</span></span>
<span data-ttu-id="914f8-116">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="914f8-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="914f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="914f8-117">-DefaultProfile</span></span>
<span data-ttu-id="914f8-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="914f8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="914f8-119">-Immagine</span><span class="sxs-lookup"><span data-stu-id="914f8-119">-Image</span></span>
<span data-ttu-id="914f8-120">Specifica un oggetto Image locale.</span><span class="sxs-lookup"><span data-stu-id="914f8-120">Specifies a local image object.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="914f8-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="914f8-121">-ImageName</span></span>
<span data-ttu-id="914f8-122">Specifica il nome di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="914f8-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="914f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="914f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="914f8-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="914f8-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="914f8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="914f8-125">-ResourceId</span></span>
<span data-ttu-id="914f8-126">ID risorsa per l'immagine</span><span class="sxs-lookup"><span data-stu-id="914f8-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="914f8-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="914f8-127">-Tag</span></span>
<span data-ttu-id="914f8-128">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="914f8-128">Resource tags</span></span>

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

### <span data-ttu-id="914f8-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="914f8-129">-Confirm</span></span>
<span data-ttu-id="914f8-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="914f8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="914f8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="914f8-131">-WhatIf</span></span>
<span data-ttu-id="914f8-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="914f8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="914f8-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="914f8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="914f8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="914f8-134">CommonParameters</span></span>
<span data-ttu-id="914f8-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="914f8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="914f8-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="914f8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="914f8-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="914f8-137">INPUTS</span></span>

### <span data-ttu-id="914f8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="914f8-138">System.String</span></span>

### <span data-ttu-id="914f8-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="914f8-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="914f8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="914f8-140">OUTPUTS</span></span>

### <span data-ttu-id="914f8-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="914f8-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="914f8-142">Note</span><span class="sxs-lookup"><span data-stu-id="914f8-142">NOTES</span></span>

## <span data-ttu-id="914f8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="914f8-143">RELATED LINKS</span></span>
