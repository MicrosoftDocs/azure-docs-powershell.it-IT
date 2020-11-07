---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 7c62860f3829c07621c951175b00a4be4960c95f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675282"
---
# <span data-ttu-id="883bc-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="883bc-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="883bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="883bc-102">SYNOPSIS</span></span>
<span data-ttu-id="883bc-103">Eliminare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="883bc-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="883bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="883bc-104">SYNTAX</span></span>

### <span data-ttu-id="883bc-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="883bc-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883bc-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="883bc-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883bc-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="883bc-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="883bc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="883bc-108">DESCRIPTION</span></span>
<span data-ttu-id="883bc-109">Eliminare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="883bc-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="883bc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="883bc-110">EXAMPLES</span></span>

### <span data-ttu-id="883bc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="883bc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="883bc-112">Eliminare la versione dell'immagine della raccolta specificata.</span><span class="sxs-lookup"><span data-stu-id="883bc-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="883bc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="883bc-113">PARAMETERS</span></span>

### <span data-ttu-id="883bc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="883bc-114">-AsJob</span></span>
<span data-ttu-id="883bc-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="883bc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="883bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="883bc-116">-DefaultProfile</span></span>
<span data-ttu-id="883bc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="883bc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="883bc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="883bc-118">-Force</span></span>
<span data-ttu-id="883bc-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="883bc-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="883bc-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="883bc-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="883bc-121">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="883bc-121">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883bc-122">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="883bc-122">-GalleryName</span></span>
<span data-ttu-id="883bc-123">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="883bc-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883bc-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="883bc-124">-InputObject</span></span>
<span data-ttu-id="883bc-125">Oggetto versione della raccolta immagini PS</span><span class="sxs-lookup"><span data-stu-id="883bc-125">The PS Gallery Image Version Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="883bc-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="883bc-126">-Name</span></span>
<span data-ttu-id="883bc-127">Nome della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="883bc-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883bc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="883bc-128">-ResourceGroupName</span></span>
<span data-ttu-id="883bc-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="883bc-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="883bc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="883bc-130">-ResourceId</span></span>
<span data-ttu-id="883bc-131">ID risorsa per la versione dell'immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="883bc-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="883bc-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="883bc-132">-Confirm</span></span>
<span data-ttu-id="883bc-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="883bc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="883bc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="883bc-134">-WhatIf</span></span>
<span data-ttu-id="883bc-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="883bc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="883bc-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="883bc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="883bc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="883bc-137">CommonParameters</span></span>
<span data-ttu-id="883bc-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="883bc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="883bc-139">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="883bc-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="883bc-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="883bc-140">INPUTS</span></span>

### <span data-ttu-id="883bc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="883bc-141">System.String</span></span>

### <span data-ttu-id="883bc-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="883bc-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="883bc-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="883bc-143">OUTPUTS</span></span>

### <span data-ttu-id="883bc-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="883bc-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="883bc-145">Note</span><span class="sxs-lookup"><span data-stu-id="883bc-145">NOTES</span></span>

## <span data-ttu-id="883bc-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="883bc-146">RELATED LINKS</span></span>
