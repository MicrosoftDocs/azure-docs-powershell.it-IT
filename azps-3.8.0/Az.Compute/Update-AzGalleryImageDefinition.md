---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 042c29ca079978a4ce740dba7d8ced9b0387eaf4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020541"
---
# <span data-ttu-id="d11ff-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="d11ff-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="d11ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d11ff-102">SYNOPSIS</span></span>
<span data-ttu-id="d11ff-103">Aggiornare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d11ff-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="d11ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d11ff-104">SYNTAX</span></span>

### <span data-ttu-id="d11ff-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d11ff-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d11ff-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d11ff-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d11ff-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d11ff-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d11ff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d11ff-108">DESCRIPTION</span></span>
<span data-ttu-id="d11ff-109">Aggiornare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d11ff-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="d11ff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d11ff-110">EXAMPLES</span></span>

### <span data-ttu-id="d11ff-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d11ff-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="d11ff-112">Aggiornare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d11ff-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="d11ff-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d11ff-113">PARAMETERS</span></span>

### <span data-ttu-id="d11ff-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d11ff-114">-AsJob</span></span>
<span data-ttu-id="d11ff-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d11ff-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d11ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11ff-116">-DefaultProfile</span></span>
<span data-ttu-id="d11ff-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d11ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d11ff-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d11ff-118">-Description</span></span>
<span data-ttu-id="d11ff-119">Descrizione della risorsa di definizione delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d11ff-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="d11ff-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="d11ff-120">-DisallowedDiskType</span></span>
<span data-ttu-id="d11ff-121">Tipi di disco non consentiti.</span><span class="sxs-lookup"><span data-stu-id="d11ff-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="d11ff-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="d11ff-122">-EndOfLifeDate</span></span>
<span data-ttu-id="d11ff-123">Data di fine del ciclo di vita della definizione di immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="d11ff-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="d11ff-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="d11ff-124">-Eula</span></span>
<span data-ttu-id="d11ff-125">Contratto EULA per la definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d11ff-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="d11ff-126">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="d11ff-126">-GalleryName</span></span>
<span data-ttu-id="d11ff-127">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d11ff-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="d11ff-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d11ff-128">-InputObject</span></span>
<span data-ttu-id="d11ff-129">Oggetto definizione immagine della raccolta PS.</span><span class="sxs-lookup"><span data-stu-id="d11ff-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="d11ff-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="d11ff-130">-MaximumMemory</span></span>
<span data-ttu-id="d11ff-131">Il massimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="d11ff-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="d11ff-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="d11ff-132">-MaximumVCPU</span></span>
<span data-ttu-id="d11ff-133">Il massimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="d11ff-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="d11ff-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="d11ff-134">-MinimumMemory</span></span>
<span data-ttu-id="d11ff-135">Il minimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="d11ff-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="d11ff-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="d11ff-136">-MinimumVCPU</span></span>
<span data-ttu-id="d11ff-137">Il minimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="d11ff-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="d11ff-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="d11ff-138">-Name</span></span>
<span data-ttu-id="d11ff-139">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d11ff-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="d11ff-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="d11ff-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="d11ff-141">URI dell'informativa sulla privacy.</span><span class="sxs-lookup"><span data-stu-id="d11ff-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="d11ff-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="d11ff-142">-PurchasePlanName</span></span>
<span data-ttu-id="d11ff-143">ID per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="d11ff-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="d11ff-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="d11ff-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="d11ff-145">ID prodotto per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="d11ff-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="d11ff-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="d11ff-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="d11ff-147">ID Publisher per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="d11ff-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="d11ff-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="d11ff-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="d11ff-149">URI della nota di rilascio.</span><span class="sxs-lookup"><span data-stu-id="d11ff-149">The release note uri.</span></span>

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

### <span data-ttu-id="d11ff-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d11ff-150">-ResourceGroupName</span></span>
<span data-ttu-id="d11ff-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d11ff-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="d11ff-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d11ff-152">-ResourceId</span></span>
<span data-ttu-id="d11ff-153">ID risorsa per la definizione di immagine</span><span class="sxs-lookup"><span data-stu-id="d11ff-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="d11ff-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="d11ff-154">-Tag</span></span>
<span data-ttu-id="d11ff-155">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="d11ff-155">Resource tags</span></span>

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

### <span data-ttu-id="d11ff-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d11ff-156">-Confirm</span></span>
<span data-ttu-id="d11ff-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d11ff-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d11ff-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d11ff-158">-WhatIf</span></span>
<span data-ttu-id="d11ff-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d11ff-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d11ff-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d11ff-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d11ff-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11ff-161">CommonParameters</span></span>
<span data-ttu-id="d11ff-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d11ff-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11ff-163">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d11ff-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11ff-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d11ff-164">INPUTS</span></span>

### <span data-ttu-id="d11ff-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d11ff-165">System.String</span></span>

### <span data-ttu-id="d11ff-166">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="d11ff-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="d11ff-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="d11ff-167">System.DateTime</span></span>

### <span data-ttu-id="d11ff-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d11ff-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d11ff-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d11ff-169">System.Int32</span></span>

### <span data-ttu-id="d11ff-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="d11ff-170">System.String[]</span></span>

## <span data-ttu-id="d11ff-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d11ff-171">OUTPUTS</span></span>

### <span data-ttu-id="d11ff-172">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="d11ff-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="d11ff-173">Note</span><span class="sxs-lookup"><span data-stu-id="d11ff-173">NOTES</span></span>

## <span data-ttu-id="d11ff-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d11ff-174">RELATED LINKS</span></span>
