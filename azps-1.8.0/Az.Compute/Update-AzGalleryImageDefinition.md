---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 338e65e4795f3b676a1f88e8a8281a41aee5a0c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836604"
---
# <span data-ttu-id="c91f2-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="c91f2-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="c91f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c91f2-102">SYNOPSIS</span></span>
<span data-ttu-id="c91f2-103">Aggiornare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c91f2-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="c91f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c91f2-104">SYNTAX</span></span>

### <span data-ttu-id="c91f2-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c91f2-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c91f2-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c91f2-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c91f2-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="c91f2-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c91f2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c91f2-108">DESCRIPTION</span></span>
<span data-ttu-id="c91f2-109">Aggiornare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c91f2-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="c91f2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c91f2-110">EXAMPLES</span></span>

### <span data-ttu-id="c91f2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c91f2-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="c91f2-112">Aggiornare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c91f2-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="c91f2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c91f2-113">PARAMETERS</span></span>

### <span data-ttu-id="c91f2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c91f2-114">-AsJob</span></span>
<span data-ttu-id="c91f2-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c91f2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c91f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c91f2-116">-DefaultProfile</span></span>
<span data-ttu-id="c91f2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c91f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c91f2-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c91f2-118">-Description</span></span>
<span data-ttu-id="c91f2-119">Descrizione della risorsa di definizione delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c91f2-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="c91f2-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="c91f2-120">-DisallowedDiskType</span></span>
<span data-ttu-id="c91f2-121">Tipi di disco non consentiti.</span><span class="sxs-lookup"><span data-stu-id="c91f2-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="c91f2-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="c91f2-122">-EndOfLifeDate</span></span>
<span data-ttu-id="c91f2-123">Data di fine del ciclo di vita della definizione di immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="c91f2-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="c91f2-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="c91f2-124">-Eula</span></span>
<span data-ttu-id="c91f2-125">Contratto EULA per la definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c91f2-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="c91f2-126">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="c91f2-126">-GalleryName</span></span>
<span data-ttu-id="c91f2-127">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c91f2-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="c91f2-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c91f2-128">-InputObject</span></span>
<span data-ttu-id="c91f2-129">Oggetto definizione immagine della raccolta PS.</span><span class="sxs-lookup"><span data-stu-id="c91f2-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="c91f2-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="c91f2-130">-MaximumMemory</span></span>
<span data-ttu-id="c91f2-131">Il massimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="c91f2-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="c91f2-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="c91f2-132">-MaximumVCPU</span></span>
<span data-ttu-id="c91f2-133">Il massimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="c91f2-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="c91f2-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="c91f2-134">-MinimumMemory</span></span>
<span data-ttu-id="c91f2-135">Il minimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="c91f2-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="c91f2-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="c91f2-136">-MinimumVCPU</span></span>
<span data-ttu-id="c91f2-137">Il minimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="c91f2-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="c91f2-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="c91f2-138">-Name</span></span>
<span data-ttu-id="c91f2-139">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c91f2-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="c91f2-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="c91f2-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="c91f2-141">URI dell'informativa sulla privacy.</span><span class="sxs-lookup"><span data-stu-id="c91f2-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="c91f2-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="c91f2-142">-PurchasePlanName</span></span>
<span data-ttu-id="c91f2-143">ID per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="c91f2-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="c91f2-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="c91f2-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="c91f2-145">ID prodotto per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="c91f2-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="c91f2-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="c91f2-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="c91f2-147">ID Publisher per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="c91f2-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="c91f2-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="c91f2-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="c91f2-149">URI della nota di rilascio.</span><span class="sxs-lookup"><span data-stu-id="c91f2-149">The release note uri.</span></span>

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

### <span data-ttu-id="c91f2-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c91f2-150">-ResourceGroupName</span></span>
<span data-ttu-id="c91f2-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c91f2-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="c91f2-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c91f2-152">-ResourceId</span></span>
<span data-ttu-id="c91f2-153">ID risorsa per la definizione di immagine</span><span class="sxs-lookup"><span data-stu-id="c91f2-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="c91f2-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="c91f2-154">-Tag</span></span>
<span data-ttu-id="c91f2-155">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="c91f2-155">Resource tags</span></span>

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

### <span data-ttu-id="c91f2-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c91f2-156">-Confirm</span></span>
<span data-ttu-id="c91f2-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c91f2-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c91f2-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c91f2-158">-WhatIf</span></span>
<span data-ttu-id="c91f2-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c91f2-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c91f2-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c91f2-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c91f2-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c91f2-161">CommonParameters</span></span>
<span data-ttu-id="c91f2-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c91f2-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c91f2-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c91f2-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c91f2-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c91f2-164">INPUTS</span></span>

### <span data-ttu-id="c91f2-165">System. String</span><span class="sxs-lookup"><span data-stu-id="c91f2-165">System.String</span></span>

### <span data-ttu-id="c91f2-166">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="c91f2-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="c91f2-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="c91f2-167">System.DateTime</span></span>

### <span data-ttu-id="c91f2-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c91f2-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c91f2-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c91f2-169">System.Int32</span></span>

### <span data-ttu-id="c91f2-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="c91f2-170">System.String[]</span></span>

## <span data-ttu-id="c91f2-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c91f2-171">OUTPUTS</span></span>

### <span data-ttu-id="c91f2-172">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="c91f2-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="c91f2-173">Note</span><span class="sxs-lookup"><span data-stu-id="c91f2-173">NOTES</span></span>

## <span data-ttu-id="c91f2-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c91f2-174">RELATED LINKS</span></span>
