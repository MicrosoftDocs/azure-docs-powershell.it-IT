---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 445029c41e27cce14bff2ac14d826adf28f3c9ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685443"
---
# <span data-ttu-id="fdfa0-101">Update-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="fdfa0-101">Update-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="fdfa0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdfa0-102">SYNOPSIS</span></span>
<span data-ttu-id="fdfa0-103">Aggiornare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-103">Update a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdfa0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdfa0-104">SYNTAX</span></span>

### <span data-ttu-id="fdfa0-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fdfa0-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfa0-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="fdfa0-106">ResourceIdParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdfa0-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="fdfa0-107">ObjectParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdfa0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdfa0-108">DESCRIPTION</span></span>
<span data-ttu-id="fdfa0-109">Aggiornare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="fdfa0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdfa0-110">EXAMPLES</span></span>

### <span data-ttu-id="fdfa0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fdfa0-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="fdfa0-112">Aggiornare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="fdfa0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdfa0-113">PARAMETERS</span></span>

### <span data-ttu-id="fdfa0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdfa0-114">-AsJob</span></span>
<span data-ttu-id="fdfa0-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fdfa0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdfa0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdfa0-116">-DefaultProfile</span></span>
<span data-ttu-id="fdfa0-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdfa0-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdfa0-118">-Description</span></span>
<span data-ttu-id="fdfa0-119">Descrizione della risorsa di definizione delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="fdfa0-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="fdfa0-120">-DisallowedDiskType</span></span>
<span data-ttu-id="fdfa0-121">Tipi di disco non consentiti.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="fdfa0-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="fdfa0-122">-EndOfLifeDate</span></span>
<span data-ttu-id="fdfa0-123">Data di fine del ciclo di vita della definizione di immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="fdfa0-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="fdfa0-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="fdfa0-124">-Eula</span></span>
<span data-ttu-id="fdfa0-125">Contratto EULA per la definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="fdfa0-126">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="fdfa0-126">-GalleryName</span></span>
<span data-ttu-id="fdfa0-127">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="fdfa0-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdfa0-128">-InputObject</span></span>
<span data-ttu-id="fdfa0-129">Oggetto definizione immagine della raccolta PS.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="fdfa0-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="fdfa0-130">-MaximumMemory</span></span>
<span data-ttu-id="fdfa0-131">Il massimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="fdfa0-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="fdfa0-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="fdfa0-132">-MaximumVCPU</span></span>
<span data-ttu-id="fdfa0-133">Il massimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="fdfa0-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="fdfa0-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="fdfa0-134">-MinimumMemory</span></span>
<span data-ttu-id="fdfa0-135">Il minimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="fdfa0-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="fdfa0-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="fdfa0-136">-MinimumVCPU</span></span>
<span data-ttu-id="fdfa0-137">Il minimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="fdfa0-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="fdfa0-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdfa0-138">-Name</span></span>
<span data-ttu-id="fdfa0-139">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="fdfa0-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="fdfa0-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="fdfa0-141">URI dell'informativa sulla privacy.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="fdfa0-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="fdfa0-142">-PurchasePlanName</span></span>
<span data-ttu-id="fdfa0-143">ID per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fdfa0-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="fdfa0-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="fdfa0-145">ID prodotto per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fdfa0-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="fdfa0-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="fdfa0-147">ID Publisher per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fdfa0-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="fdfa0-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="fdfa0-149">URI della nota di rilascio.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-149">The release note uri.</span></span>

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

### <span data-ttu-id="fdfa0-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdfa0-150">-ResourceGroupName</span></span>
<span data-ttu-id="fdfa0-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="fdfa0-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdfa0-152">-ResourceId</span></span>
<span data-ttu-id="fdfa0-153">ID risorsa per la definizione di immagine</span><span class="sxs-lookup"><span data-stu-id="fdfa0-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="fdfa0-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="fdfa0-154">-Tag</span></span>
<span data-ttu-id="fdfa0-155">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="fdfa0-155">Resource tags</span></span>

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

### <span data-ttu-id="fdfa0-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fdfa0-156">-Confirm</span></span>
<span data-ttu-id="fdfa0-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdfa0-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdfa0-158">-WhatIf</span></span>
<span data-ttu-id="fdfa0-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdfa0-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdfa0-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdfa0-161">CommonParameters</span></span>
<span data-ttu-id="fdfa0-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdfa0-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdfa0-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdfa0-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdfa0-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdfa0-164">INPUTS</span></span>

### <span data-ttu-id="fdfa0-165">System. String</span><span class="sxs-lookup"><span data-stu-id="fdfa0-165">System.String</span></span>

### <span data-ttu-id="fdfa0-166">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="fdfa0-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="fdfa0-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="fdfa0-167">System.DateTime</span></span>

### <span data-ttu-id="fdfa0-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fdfa0-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fdfa0-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fdfa0-169">System.Int32</span></span>

### <span data-ttu-id="fdfa0-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="fdfa0-170">System.String[]</span></span>

## <span data-ttu-id="fdfa0-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdfa0-171">OUTPUTS</span></span>

### <span data-ttu-id="fdfa0-172">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="fdfa0-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="fdfa0-173">Note</span><span class="sxs-lookup"><span data-stu-id="fdfa0-173">NOTES</span></span>

## <span data-ttu-id="fdfa0-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdfa0-174">RELATED LINKS</span></span>
