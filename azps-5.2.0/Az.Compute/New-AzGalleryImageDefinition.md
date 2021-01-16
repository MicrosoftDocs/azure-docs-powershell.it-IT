---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357041"
---
# <span data-ttu-id="932cf-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="932cf-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="932cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="932cf-102">SYNOPSIS</span></span>
<span data-ttu-id="932cf-103">Creare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="932cf-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="932cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="932cf-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="932cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="932cf-105">DESCRIPTION</span></span>
<span data-ttu-id="932cf-106">Creare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="932cf-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="932cf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="932cf-107">EXAMPLES</span></span>

### <span data-ttu-id="932cf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="932cf-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="932cf-109">Creare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="932cf-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="932cf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="932cf-110">PARAMETERS</span></span>

### <span data-ttu-id="932cf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="932cf-111">-AsJob</span></span>
<span data-ttu-id="932cf-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="932cf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="932cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="932cf-113">-DefaultProfile</span></span>
<span data-ttu-id="932cf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="932cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="932cf-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="932cf-115">-Description</span></span>
<span data-ttu-id="932cf-116">Descrizione della risorsa di definizione delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="932cf-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="932cf-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="932cf-117">-DisallowedDiskType</span></span>
<span data-ttu-id="932cf-118">Tipi di disco non consentiti.</span><span class="sxs-lookup"><span data-stu-id="932cf-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="932cf-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="932cf-119">-EndOfLifeDate</span></span>
<span data-ttu-id="932cf-120">Data di fine del ciclo di vita della definizione di immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="932cf-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="932cf-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="932cf-121">-Eula</span></span>
<span data-ttu-id="932cf-122">Contratto EULA per la definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="932cf-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="932cf-123">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="932cf-123">-GalleryName</span></span>
<span data-ttu-id="932cf-124">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="932cf-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="932cf-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="932cf-125">-HyperVGeneration</span></span>
<span data-ttu-id="932cf-126">Generazione di hypervisor della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="932cf-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="932cf-127">Applicabile solo ai dischi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="932cf-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="932cf-128">I valori consentiti sono V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="932cf-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="932cf-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="932cf-129">-Location</span></span>
<span data-ttu-id="932cf-130">Posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="932cf-130">Resource location</span></span>

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

### <span data-ttu-id="932cf-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="932cf-131">-MaximumMemory</span></span>
<span data-ttu-id="932cf-132">Il massimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="932cf-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="932cf-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="932cf-133">-MaximumVCPU</span></span>
<span data-ttu-id="932cf-134">Il massimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="932cf-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="932cf-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="932cf-135">-MinimumMemory</span></span>
<span data-ttu-id="932cf-136">Il minimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="932cf-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="932cf-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="932cf-137">-MinimumVCPU</span></span>
<span data-ttu-id="932cf-138">Il minimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="932cf-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="932cf-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="932cf-139">-Name</span></span>
<span data-ttu-id="932cf-140">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="932cf-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="932cf-141">-Offerta</span><span class="sxs-lookup"><span data-stu-id="932cf-141">-Offer</span></span>
<span data-ttu-id="932cf-142">Il nome della definizione di immagine della raccolta offre.</span><span class="sxs-lookup"><span data-stu-id="932cf-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="932cf-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="932cf-143">-OsState</span></span>
<span data-ttu-id="932cf-144">Stato del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="932cf-144">The state of OS</span></span>

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

### <span data-ttu-id="932cf-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="932cf-145">-OsType</span></span>
<span data-ttu-id="932cf-146">Tipo di sistema operativo</span><span class="sxs-lookup"><span data-stu-id="932cf-146">The type of OS</span></span>

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

### <span data-ttu-id="932cf-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="932cf-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="932cf-148">URI dell'informativa sulla privacy.</span><span class="sxs-lookup"><span data-stu-id="932cf-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="932cf-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="932cf-149">-Publisher</span></span>
<span data-ttu-id="932cf-150">Nome dell'editor di definizioni di immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="932cf-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="932cf-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="932cf-151">-PurchasePlanName</span></span>
<span data-ttu-id="932cf-152">ID per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="932cf-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="932cf-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="932cf-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="932cf-154">ID prodotto per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="932cf-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="932cf-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="932cf-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="932cf-156">ID Publisher per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="932cf-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="932cf-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="932cf-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="932cf-158">URI della nota di rilascio.</span><span class="sxs-lookup"><span data-stu-id="932cf-158">The release note uri.</span></span>

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

### <span data-ttu-id="932cf-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="932cf-159">-ResourceGroupName</span></span>
<span data-ttu-id="932cf-160">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="932cf-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="932cf-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="932cf-161">-Sku</span></span>
<span data-ttu-id="932cf-162">Nome della SKU di definizione delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="932cf-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="932cf-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="932cf-163">-Tag</span></span>
<span data-ttu-id="932cf-164">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="932cf-164">Resource tags</span></span>

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

### <span data-ttu-id="932cf-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="932cf-165">-Confirm</span></span>
<span data-ttu-id="932cf-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="932cf-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="932cf-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="932cf-167">-WhatIf</span></span>
<span data-ttu-id="932cf-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="932cf-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="932cf-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="932cf-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="932cf-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="932cf-170">CommonParameters</span></span>
<span data-ttu-id="932cf-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="932cf-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="932cf-172">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="932cf-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="932cf-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="932cf-173">INPUTS</span></span>

### <span data-ttu-id="932cf-174">System. String</span><span class="sxs-lookup"><span data-stu-id="932cf-174">System.String</span></span>

### <span data-ttu-id="932cf-175">Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="932cf-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="932cf-176">Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="932cf-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="932cf-177">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="932cf-177">System.DateTime</span></span>

### <span data-ttu-id="932cf-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="932cf-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="932cf-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="932cf-179">System.Int32</span></span>

### <span data-ttu-id="932cf-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="932cf-180">System.String[]</span></span>

## <span data-ttu-id="932cf-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="932cf-181">OUTPUTS</span></span>

### <span data-ttu-id="932cf-182">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="932cf-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="932cf-183">Note</span><span class="sxs-lookup"><span data-stu-id="932cf-183">NOTES</span></span>

## <span data-ttu-id="932cf-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="932cf-184">RELATED LINKS</span></span>
