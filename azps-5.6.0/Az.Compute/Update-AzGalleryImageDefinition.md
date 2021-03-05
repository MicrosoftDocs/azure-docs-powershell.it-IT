---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 09871f6d7876b5f197af515f531c85b8bf6a3d9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972062"
---
# <span data-ttu-id="8826b-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="8826b-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="8826b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8826b-102">SYNOPSIS</span></span>
<span data-ttu-id="8826b-103">Aggiornare la definizione di un'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8826b-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="8826b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8826b-104">SYNTAX</span></span>

### <span data-ttu-id="8826b-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="8826b-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8826b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8826b-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8826b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8826b-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8826b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8826b-108">DESCRIPTION</span></span>
<span data-ttu-id="8826b-109">Aggiornare la definizione di un'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8826b-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="8826b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8826b-110">EXAMPLES</span></span>

### <span data-ttu-id="8826b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8826b-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="8826b-112">Aggiornare la definizione di un'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8826b-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="8826b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8826b-113">PARAMETERS</span></span>

### <span data-ttu-id="8826b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8826b-114">-AsJob</span></span>
<span data-ttu-id="8826b-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8826b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8826b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8826b-116">-DefaultProfile</span></span>
<span data-ttu-id="8826b-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8826b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8826b-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8826b-118">-Description</span></span>
<span data-ttu-id="8826b-119">Descrizione della risorsa Definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8826b-119">The description of the gallery image Definition resource.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="8826b-120">-DisallowedDiskType</span></span>
<span data-ttu-id="8826b-121">Tipi di disco non consentiti.</span><span class="sxs-lookup"><span data-stu-id="8826b-121">The disallowed disk types.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="8826b-122">-EndOfLifeDate</span></span>
<span data-ttu-id="8826b-123">Data di fine del ciclo di vita della definizione immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="8826b-123">The end of life date of the gallery Image Definition</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="8826b-124">-Eula</span></span>
<span data-ttu-id="8826b-125">Contratto di licenza per la definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8826b-125">The Eula agreement for the gallery Image Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="8826b-126">-GalleryName</span></span>
<span data-ttu-id="8826b-127">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8826b-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="8826b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8826b-128">-InputObject</span></span>
<span data-ttu-id="8826b-129">Oggetto definizione immagine raccolta PS.</span><span class="sxs-lookup"><span data-stu-id="8826b-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="8826b-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="8826b-130">-MaximumMemory</span></span>
<span data-ttu-id="8826b-131">Il massimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="8826b-131">The maximum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="8826b-132">-MaximumVCPU</span></span>
<span data-ttu-id="8826b-133">Il massimo del core cpu consigliato</span><span class="sxs-lookup"><span data-stu-id="8826b-133">The maximum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="8826b-134">-MinimumMemory</span></span>
<span data-ttu-id="8826b-135">Il minimo di memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="8826b-135">The minimum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="8826b-136">-MinimumVCPU</span></span>
<span data-ttu-id="8826b-137">Il minimo del core di CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="8826b-137">The minimum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-138">-Name</span><span class="sxs-lookup"><span data-stu-id="8826b-138">-Name</span></span>
<span data-ttu-id="8826b-139">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8826b-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="8826b-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="8826b-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="8826b-141">URI dell'informativa sulla privacy.</span><span class="sxs-lookup"><span data-stu-id="8826b-141">The privacy statement uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="8826b-142">-PurchasePlanName</span></span>
<span data-ttu-id="8826b-143">ID del piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="8826b-143">The ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="8826b-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="8826b-145">ID prodotto per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="8826b-145">The product ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="8826b-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="8826b-147">ID editore per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="8826b-147">The publisher ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="8826b-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="8826b-149">URI della nota sulla versione.</span><span class="sxs-lookup"><span data-stu-id="8826b-149">The release note uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8826b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8826b-150">-ResourceGroupName</span></span>
<span data-ttu-id="8826b-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8826b-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="8826b-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8826b-152">-ResourceId</span></span>
<span data-ttu-id="8826b-153">ID risorsa per la definizione dell'immagine</span><span class="sxs-lookup"><span data-stu-id="8826b-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="8826b-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="8826b-154">-Tag</span></span>
<span data-ttu-id="8826b-155">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="8826b-155">Resource tags</span></span>

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

### <span data-ttu-id="8826b-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8826b-156">-Confirm</span></span>
<span data-ttu-id="8826b-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8826b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8826b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8826b-158">-WhatIf</span></span>
<span data-ttu-id="8826b-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8826b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8826b-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8826b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8826b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8826b-161">CommonParameters</span></span>
<span data-ttu-id="8826b-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8826b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8826b-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8826b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8826b-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="8826b-164">INPUTS</span></span>

### <span data-ttu-id="8826b-165">System.String</span><span class="sxs-lookup"><span data-stu-id="8826b-165">System.String</span></span>

### <span data-ttu-id="8826b-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="8826b-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="8826b-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="8826b-167">System.DateTime</span></span>

### <span data-ttu-id="8826b-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8826b-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8826b-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8826b-169">System.Int32</span></span>

### <span data-ttu-id="8826b-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8826b-170">System.String[]</span></span>

## <span data-ttu-id="8826b-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8826b-171">OUTPUTS</span></span>

### <span data-ttu-id="8826b-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="8826b-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="8826b-173">NOTE</span><span class="sxs-lookup"><span data-stu-id="8826b-173">NOTES</span></span>

## <span data-ttu-id="8826b-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8826b-174">RELATED LINKS</span></span>
