---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
ms.openlocfilehash: c2a65eeb742d4182dfad0cd32be1d78951977096
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511828"
---
# <span data-ttu-id="50c90-101">Remove-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="50c90-101">Remove-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="50c90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50c90-102">SYNOPSIS</span></span>
<span data-ttu-id="50c90-103">Eliminare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50c90-103">Delete a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50c90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50c90-104">SYNTAX</span></span>

### <span data-ttu-id="50c90-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50c90-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50c90-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="50c90-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50c90-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="50c90-107">ObjectParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50c90-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50c90-108">DESCRIPTION</span></span>
<span data-ttu-id="50c90-109">Eliminare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50c90-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="50c90-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50c90-110">EXAMPLES</span></span>

### <span data-ttu-id="50c90-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50c90-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="50c90-112">Eliminare la versione dell'immagine della raccolta specificata.</span><span class="sxs-lookup"><span data-stu-id="50c90-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="50c90-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50c90-113">PARAMETERS</span></span>

### <span data-ttu-id="50c90-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50c90-114">-AsJob</span></span>
<span data-ttu-id="50c90-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="50c90-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50c90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c90-116">-DefaultProfile</span></span>
<span data-ttu-id="50c90-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50c90-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50c90-118">-Force</span><span class="sxs-lookup"><span data-stu-id="50c90-118">-Force</span></span>
<span data-ttu-id="50c90-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="50c90-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50c90-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="50c90-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="50c90-121">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50c90-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="50c90-122">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="50c90-122">-GalleryName</span></span>
<span data-ttu-id="50c90-123">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50c90-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="50c90-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50c90-124">-InputObject</span></span>
<span data-ttu-id="50c90-125">Oggetto versione della raccolta immagini PS</span><span class="sxs-lookup"><span data-stu-id="50c90-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="50c90-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="50c90-126">-Name</span></span>
<span data-ttu-id="50c90-127">Nome della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="50c90-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="50c90-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50c90-128">-ResourceGroupName</span></span>
<span data-ttu-id="50c90-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50c90-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="50c90-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50c90-130">-ResourceId</span></span>
<span data-ttu-id="50c90-131">ID risorsa per la versione dell'immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="50c90-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="50c90-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50c90-132">-Confirm</span></span>
<span data-ttu-id="50c90-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50c90-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50c90-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50c90-134">-WhatIf</span></span>
<span data-ttu-id="50c90-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50c90-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50c90-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50c90-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50c90-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c90-137">CommonParameters</span></span>
<span data-ttu-id="50c90-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c90-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c90-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50c90-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c90-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50c90-140">INPUTS</span></span>

### <span data-ttu-id="50c90-141">System. String</span><span class="sxs-lookup"><span data-stu-id="50c90-141">System.String</span></span>

### <span data-ttu-id="50c90-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="50c90-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="50c90-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50c90-143">OUTPUTS</span></span>

### <span data-ttu-id="50c90-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="50c90-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="50c90-145">Note</span><span class="sxs-lookup"><span data-stu-id="50c90-145">NOTES</span></span>

## <span data-ttu-id="50c90-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50c90-146">RELATED LINKS</span></span>
