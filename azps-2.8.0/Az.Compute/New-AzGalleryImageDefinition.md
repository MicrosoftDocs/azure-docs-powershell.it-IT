---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: 7b2a0399be6412c3e33754a8e91b1a6120b5ec9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675340"
---
# <span data-ttu-id="56af0-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="56af0-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="56af0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56af0-102">SYNOPSIS</span></span>
<span data-ttu-id="56af0-103">Creare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="56af0-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="56af0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56af0-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>]
 [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>]
 [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56af0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56af0-105">DESCRIPTION</span></span>
<span data-ttu-id="56af0-106">Creare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="56af0-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="56af0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56af0-107">EXAMPLES</span></span>

### <span data-ttu-id="56af0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56af0-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="56af0-109">Creare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="56af0-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="56af0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56af0-110">PARAMETERS</span></span>

### <span data-ttu-id="56af0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56af0-111">-AsJob</span></span>
<span data-ttu-id="56af0-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="56af0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56af0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56af0-113">-DefaultProfile</span></span>
<span data-ttu-id="56af0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56af0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56af0-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="56af0-115">-Description</span></span>
<span data-ttu-id="56af0-116">Descrizione della risorsa di definizione delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="56af0-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="56af0-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="56af0-117">-DisallowedDiskType</span></span>
<span data-ttu-id="56af0-118">Tipi di disco non consentiti.</span><span class="sxs-lookup"><span data-stu-id="56af0-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="56af0-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="56af0-119">-EndOfLifeDate</span></span>
<span data-ttu-id="56af0-120">Data di fine del ciclo di vita della definizione di immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="56af0-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="56af0-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="56af0-121">-Eula</span></span>
<span data-ttu-id="56af0-122">Contratto EULA per la definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="56af0-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="56af0-123">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="56af0-123">-GalleryName</span></span>
<span data-ttu-id="56af0-124">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="56af0-124">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af0-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="56af0-125">-Location</span></span>
<span data-ttu-id="56af0-126">Posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="56af0-126">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af0-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="56af0-127">-MaximumMemory</span></span>
<span data-ttu-id="56af0-128">Il massimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="56af0-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="56af0-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="56af0-129">-MaximumVCPU</span></span>
<span data-ttu-id="56af0-130">Il massimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="56af0-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="56af0-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="56af0-131">-MinimumMemory</span></span>
<span data-ttu-id="56af0-132">Il minimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="56af0-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="56af0-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="56af0-133">-MinimumVCPU</span></span>
<span data-ttu-id="56af0-134">Il minimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="56af0-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="56af0-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="56af0-135">-Name</span></span>
<span data-ttu-id="56af0-136">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="56af0-136">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af0-137">-Offerta</span><span class="sxs-lookup"><span data-stu-id="56af0-137">-Offer</span></span>
<span data-ttu-id="56af0-138">Il nome della definizione di immagine della raccolta offre.</span><span class="sxs-lookup"><span data-stu-id="56af0-138">The name of the gallery Image Definition offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af0-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="56af0-139">-OsState</span></span>
<span data-ttu-id="56af0-140">Stato del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="56af0-140">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af0-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="56af0-141">-OsType</span></span>
<span data-ttu-id="56af0-142">Tipo di sistema operativo</span><span class="sxs-lookup"><span data-stu-id="56af0-142">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af0-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="56af0-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="56af0-144">URI dell'informativa sulla privacy.</span><span class="sxs-lookup"><span data-stu-id="56af0-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="56af0-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="56af0-145">-Publisher</span></span>
<span data-ttu-id="56af0-146">Nome dell'editor di definizioni di immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="56af0-146">The name of the gallery Image Definition publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af0-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="56af0-147">-PurchasePlanName</span></span>
<span data-ttu-id="56af0-148">ID per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="56af0-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="56af0-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="56af0-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="56af0-150">ID prodotto per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="56af0-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="56af0-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="56af0-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="56af0-152">ID Publisher per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="56af0-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="56af0-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="56af0-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="56af0-154">URI della nota di rilascio.</span><span class="sxs-lookup"><span data-stu-id="56af0-154">The release note uri.</span></span>

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

### <span data-ttu-id="56af0-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56af0-155">-ResourceGroupName</span></span>
<span data-ttu-id="56af0-156">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56af0-156">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af0-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="56af0-157">-Sku</span></span>
<span data-ttu-id="56af0-158">Nome della SKU di definizione delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="56af0-158">The name of the gallery Image Definition SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af0-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="56af0-159">-Tag</span></span>
<span data-ttu-id="56af0-160">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="56af0-160">Resource tags</span></span>

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

### <span data-ttu-id="56af0-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56af0-161">-Confirm</span></span>
<span data-ttu-id="56af0-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56af0-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56af0-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56af0-163">-WhatIf</span></span>
<span data-ttu-id="56af0-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56af0-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56af0-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56af0-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56af0-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56af0-166">CommonParameters</span></span>
<span data-ttu-id="56af0-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56af0-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56af0-168">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56af0-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56af0-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56af0-169">INPUTS</span></span>

### <span data-ttu-id="56af0-170">System. String</span><span class="sxs-lookup"><span data-stu-id="56af0-170">System.String</span></span>

### <span data-ttu-id="56af0-171">Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="56af0-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="56af0-172">Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="56af0-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="56af0-173">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="56af0-173">System.DateTime</span></span>

### <span data-ttu-id="56af0-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="56af0-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="56af0-175">System. Int32</span><span class="sxs-lookup"><span data-stu-id="56af0-175">System.Int32</span></span>

### <span data-ttu-id="56af0-176">System. String []</span><span class="sxs-lookup"><span data-stu-id="56af0-176">System.String[]</span></span>

## <span data-ttu-id="56af0-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56af0-177">OUTPUTS</span></span>

### <span data-ttu-id="56af0-178">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="56af0-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="56af0-179">Note</span><span class="sxs-lookup"><span data-stu-id="56af0-179">NOTES</span></span>

## <span data-ttu-id="56af0-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56af0-180">RELATED LINKS</span></span>
