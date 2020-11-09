---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310914"
---
# <span data-ttu-id="3e2c7-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="3e2c7-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="3e2c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="3e2c7-103">Creare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="3e2c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e2c7-104">SYNTAX</span></span>

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

## <span data-ttu-id="3e2c7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e2c7-105">DESCRIPTION</span></span>
<span data-ttu-id="3e2c7-106">Creare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="3e2c7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e2c7-107">EXAMPLES</span></span>

### <span data-ttu-id="3e2c7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e2c7-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="3e2c7-109">Creare una definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="3e2c7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e2c7-110">PARAMETERS</span></span>

### <span data-ttu-id="3e2c7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e2c7-111">-AsJob</span></span>
<span data-ttu-id="3e2c7-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3e2c7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e2c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e2c7-113">-DefaultProfile</span></span>
<span data-ttu-id="3e2c7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e2c7-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e2c7-115">-Description</span></span>
<span data-ttu-id="3e2c7-116">Descrizione della risorsa di definizione delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="3e2c7-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="3e2c7-117">-DisallowedDiskType</span></span>
<span data-ttu-id="3e2c7-118">Tipi di disco non consentiti.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="3e2c7-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="3e2c7-119">-EndOfLifeDate</span></span>
<span data-ttu-id="3e2c7-120">Data di fine del ciclo di vita della definizione di immagine della raccolta</span><span class="sxs-lookup"><span data-stu-id="3e2c7-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="3e2c7-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="3e2c7-121">-Eula</span></span>
<span data-ttu-id="3e2c7-122">Contratto EULA per la definizione di immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="3e2c7-123">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="3e2c7-123">-GalleryName</span></span>
<span data-ttu-id="3e2c7-124">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="3e2c7-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="3e2c7-125">-HyperVGeneration</span></span>
<span data-ttu-id="3e2c7-126">Generazione di hypervisor della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="3e2c7-127">Applicabile solo ai dischi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="3e2c7-128">I valori consentiti sono V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="3e2c7-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3e2c7-129">-Location</span></span>
<span data-ttu-id="3e2c7-130">Posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="3e2c7-130">Resource location</span></span>

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

### <span data-ttu-id="3e2c7-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="3e2c7-131">-MaximumMemory</span></span>
<span data-ttu-id="3e2c7-132">Il massimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="3e2c7-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="3e2c7-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="3e2c7-133">-MaximumVCPU</span></span>
<span data-ttu-id="3e2c7-134">Il massimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="3e2c7-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="3e2c7-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="3e2c7-135">-MinimumMemory</span></span>
<span data-ttu-id="3e2c7-136">Il minimo della memoria consigliata</span><span class="sxs-lookup"><span data-stu-id="3e2c7-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="3e2c7-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="3e2c7-137">-MinimumVCPU</span></span>
<span data-ttu-id="3e2c7-138">Il minimo del nucleo CPU consigliato</span><span class="sxs-lookup"><span data-stu-id="3e2c7-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="3e2c7-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e2c7-139">-Name</span></span>
<span data-ttu-id="3e2c7-140">Nome della definizione dell'immagine della raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="3e2c7-141">-Offerta</span><span class="sxs-lookup"><span data-stu-id="3e2c7-141">-Offer</span></span>
<span data-ttu-id="3e2c7-142">Il nome della definizione di immagine della raccolta offre.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="3e2c7-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="3e2c7-143">-OsState</span></span>
<span data-ttu-id="3e2c7-144">Stato del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3e2c7-144">The state of OS</span></span>

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

### <span data-ttu-id="3e2c7-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="3e2c7-145">-OsType</span></span>
<span data-ttu-id="3e2c7-146">Tipo di sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3e2c7-146">The type of OS</span></span>

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

### <span data-ttu-id="3e2c7-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="3e2c7-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="3e2c7-148">URI dell'informativa sulla privacy.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="3e2c7-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3e2c7-149">-Publisher</span></span>
<span data-ttu-id="3e2c7-150">Nome dell'editor di definizioni di immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="3e2c7-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="3e2c7-151">-PurchasePlanName</span></span>
<span data-ttu-id="3e2c7-152">ID per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="3e2c7-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="3e2c7-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="3e2c7-154">ID prodotto per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="3e2c7-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="3e2c7-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="3e2c7-156">ID Publisher per il piano di acquisto.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="3e2c7-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="3e2c7-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="3e2c7-158">URI della nota di rilascio.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-158">The release note uri.</span></span>

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

### <span data-ttu-id="3e2c7-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e2c7-159">-ResourceGroupName</span></span>
<span data-ttu-id="3e2c7-160">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="3e2c7-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="3e2c7-161">-Sku</span></span>
<span data-ttu-id="3e2c7-162">Nome della SKU di definizione delle immagini della raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="3e2c7-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="3e2c7-163">-Tag</span></span>
<span data-ttu-id="3e2c7-164">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="3e2c7-164">Resource tags</span></span>

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

### <span data-ttu-id="3e2c7-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e2c7-165">-Confirm</span></span>
<span data-ttu-id="3e2c7-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e2c7-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e2c7-167">-WhatIf</span></span>
<span data-ttu-id="3e2c7-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e2c7-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e2c7-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2c7-170">CommonParameters</span></span>
<span data-ttu-id="3e2c7-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2c7-172">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e2c7-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2c7-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e2c7-173">INPUTS</span></span>

### <span data-ttu-id="3e2c7-174">System. String</span><span class="sxs-lookup"><span data-stu-id="3e2c7-174">System.String</span></span>

### <span data-ttu-id="3e2c7-175">Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="3e2c7-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="3e2c7-176">Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="3e2c7-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="3e2c7-177">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="3e2c7-177">System.DateTime</span></span>

### <span data-ttu-id="3e2c7-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3e2c7-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3e2c7-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3e2c7-179">System.Int32</span></span>

### <span data-ttu-id="3e2c7-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="3e2c7-180">System.String[]</span></span>

## <span data-ttu-id="3e2c7-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e2c7-181">OUTPUTS</span></span>

### <span data-ttu-id="3e2c7-182">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="3e2c7-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="3e2c7-183">Note</span><span class="sxs-lookup"><span data-stu-id="3e2c7-183">NOTES</span></span>

## <span data-ttu-id="3e2c7-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e2c7-184">RELATED LINKS</span></span>
