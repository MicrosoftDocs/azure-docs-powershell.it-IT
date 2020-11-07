---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 04d53c657c4747d0a4057a82e8160598fa57bc9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684750"
---
# <span data-ttu-id="e926b-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="e926b-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="e926b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e926b-102">SYNOPSIS</span></span>
<span data-ttu-id="e926b-103">Eliminare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e926b-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="e926b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e926b-104">SYNTAX</span></span>

### <span data-ttu-id="e926b-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e926b-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e926b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e926b-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e926b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e926b-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e926b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e926b-108">DESCRIPTION</span></span>
<span data-ttu-id="e926b-109">Eliminare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e926b-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="e926b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e926b-110">EXAMPLES</span></span>

### <span data-ttu-id="e926b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e926b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="e926b-112">Rimuovere la definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e926b-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="e926b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e926b-113">PARAMETERS</span></span>

### <span data-ttu-id="e926b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e926b-114">-AsJob</span></span>
<span data-ttu-id="e926b-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e926b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e926b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e926b-116">-DefaultProfile</span></span>
<span data-ttu-id="e926b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e926b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e926b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e926b-118">-Force</span></span>
<span data-ttu-id="e926b-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e926b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e926b-120">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="e926b-120">-GalleryName</span></span>
<span data-ttu-id="e926b-121">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e926b-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="e926b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e926b-122">-InputObject</span></span>
<span data-ttu-id="e926b-123">Oggetto definizione immagine della raccolta PS</span><span class="sxs-lookup"><span data-stu-id="e926b-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e926b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e926b-124">-Name</span></span>
<span data-ttu-id="e926b-125">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e926b-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e926b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e926b-126">-ResourceGroupName</span></span>
<span data-ttu-id="e926b-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e926b-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="e926b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e926b-128">-ResourceId</span></span>
<span data-ttu-id="e926b-129">ID risorsa per la definizione di immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="e926b-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="e926b-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e926b-130">-Confirm</span></span>
<span data-ttu-id="e926b-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e926b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e926b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e926b-132">-WhatIf</span></span>
<span data-ttu-id="e926b-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e926b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e926b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e926b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e926b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e926b-135">CommonParameters</span></span>
<span data-ttu-id="e926b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e926b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e926b-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e926b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e926b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e926b-138">INPUTS</span></span>

### <span data-ttu-id="e926b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e926b-139">System.String</span></span>

### <span data-ttu-id="e926b-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="e926b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="e926b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e926b-141">OUTPUTS</span></span>

### <span data-ttu-id="e926b-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e926b-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e926b-143">Note</span><span class="sxs-lookup"><span data-stu-id="e926b-143">NOTES</span></span>

## <span data-ttu-id="e926b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e926b-144">RELATED LINKS</span></span>
