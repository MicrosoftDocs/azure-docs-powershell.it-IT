---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362347"
---
# <span data-ttu-id="e2130-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e2130-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="e2130-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2130-102">SYNOPSIS</span></span>
<span data-ttu-id="e2130-103">Eliminare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e2130-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="e2130-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2130-104">SYNTAX</span></span>

### <span data-ttu-id="e2130-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2130-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2130-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e2130-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2130-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e2130-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2130-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2130-108">DESCRIPTION</span></span>
<span data-ttu-id="e2130-109">Eliminare una versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e2130-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="e2130-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2130-110">EXAMPLES</span></span>

### <span data-ttu-id="e2130-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e2130-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="e2130-112">Eliminare la versione dell'immagine della raccolta specificata.</span><span class="sxs-lookup"><span data-stu-id="e2130-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="e2130-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2130-113">PARAMETERS</span></span>

### <span data-ttu-id="e2130-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2130-114">-AsJob</span></span>
<span data-ttu-id="e2130-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e2130-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2130-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2130-116">-DefaultProfile</span></span>
<span data-ttu-id="e2130-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2130-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2130-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e2130-118">-Force</span></span>
<span data-ttu-id="e2130-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e2130-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2130-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e2130-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="e2130-121">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e2130-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="e2130-122">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="e2130-122">-GalleryName</span></span>
<span data-ttu-id="e2130-123">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e2130-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="e2130-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2130-124">-InputObject</span></span>
<span data-ttu-id="e2130-125">Oggetto versione della raccolta immagini PS</span><span class="sxs-lookup"><span data-stu-id="e2130-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="e2130-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2130-126">-Name</span></span>
<span data-ttu-id="e2130-127">Nome della versione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e2130-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="e2130-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2130-128">-ResourceGroupName</span></span>
<span data-ttu-id="e2130-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2130-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="e2130-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2130-130">-ResourceId</span></span>
<span data-ttu-id="e2130-131">ID risorsa per la versione dell'immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="e2130-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="e2130-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2130-132">-Confirm</span></span>
<span data-ttu-id="e2130-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2130-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2130-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2130-134">-WhatIf</span></span>
<span data-ttu-id="e2130-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2130-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2130-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2130-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2130-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2130-137">CommonParameters</span></span>
<span data-ttu-id="e2130-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2130-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2130-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2130-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2130-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2130-140">INPUTS</span></span>

### <span data-ttu-id="e2130-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e2130-141">System.String</span></span>

### <span data-ttu-id="e2130-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e2130-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="e2130-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2130-143">OUTPUTS</span></span>

### <span data-ttu-id="e2130-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e2130-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e2130-145">Note</span><span class="sxs-lookup"><span data-stu-id="e2130-145">NOTES</span></span>

## <span data-ttu-id="e2130-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2130-146">RELATED LINKS</span></span>
