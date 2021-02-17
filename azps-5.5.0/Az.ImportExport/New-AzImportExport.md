---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188319"
---
# <span data-ttu-id="4af5d-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4af5d-101">New-AzImportExport</span></span>

## <span data-ttu-id="4af5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4af5d-102">SYNOPSIS</span></span>
<span data-ttu-id="4af5d-103">Crea un nuovo processo o aggiorna un processo esistente nella sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="4af5d-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="4af5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4af5d-104">SYNTAX</span></span>

```
New-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-ClientTenantId <String>] [-BackupDriveManifest] [-BlobListBlobPath <String[]>]
 [-BlobListBlobPathPrefix <String[]>] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DiagnosticsPath <String>] [-DriveList <IDriveStatus[]>]
 [-ExportBlobListblobPath <String>] [-IncompleteBlobListUri <String>] [-JobType <String>] [-Location <String>]
 [-LogLevel <String>] [-PercentComplete <Int32>] [-ProvisioningState <String>] [-ReturnAddressCity <String>]
 [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>]
 [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnPackageCarrierName <String>]
 [-ReturnPackageDriveCount <Int32>] [-ReturnPackageShipDate <String>] [-ReturnPackageTrackingNumber <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>]
 [-ShippingInformationCity <String>] [-ShippingInformationCountryOrRegion <String>]
 [-ShippingInformationPhone <String>] [-ShippingInformationPostalCode <String>]
 [-ShippingInformationRecipientName <String>] [-ShippingInformationStateOrProvince <String>]
 [-ShippingInformationStreetAddress1 <String>] [-ShippingInformationStreetAddress2 <String>] [-State <String>]
 [-StorageAccountId <String>] [-Tag <IPutJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4af5d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4af5d-105">DESCRIPTION</span></span>
<span data-ttu-id="4af5d-106">Crea un nuovo processo o aggiorna un processo esistente nella sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="4af5d-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="4af5d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4af5d-107">EXAMPLES</span></span>

### <span data-ttu-id="4af5d-108">Esempio 1: Creare un nuovo processo ImportExport</span><span class="sxs-lookup"><span data-stu-id="4af5d-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="4af5d-109">Questi cmdlet creano un nuovo processo ImportExport.</span><span class="sxs-lookup"><span data-stu-id="4af5d-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="4af5d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4af5d-110">PARAMETERS</span></span>

### <span data-ttu-id="4af5d-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="4af5d-111">-AcceptLanguage</span></span>
<span data-ttu-id="4af5d-112">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="4af5d-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="4af5d-113">-BackupDriveManifest</span></span>
<span data-ttu-id="4af5d-114">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="4af5d-114">Default value is false.</span></span>
<span data-ttu-id="4af5d-115">Indica se i file manifesto nelle unità devono essere copiati per bloccare BLOB.</span><span class="sxs-lookup"><span data-stu-id="4af5d-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="4af5d-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="4af5d-116">-BlobListBlobPath</span></span>
<span data-ttu-id="4af5d-117">Raccolta di stringhe di percorsi BLOB.</span><span class="sxs-lookup"><span data-stu-id="4af5d-117">A collection of blob-path strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="4af5d-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="4af5d-119">Raccolta di stringhe di prefissi BLOB.</span><span class="sxs-lookup"><span data-stu-id="4af5d-119">A collection of blob-prefix strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="4af5d-120">-CancelRequested</span></span>
<span data-ttu-id="4af5d-121">Indica se è stata inviata una richiesta per annullare il processo.</span><span class="sxs-lookup"><span data-stu-id="4af5d-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="4af5d-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="4af5d-122">-ClientTenantId</span></span>
<span data-ttu-id="4af5d-123">ID tenant del client che effettua la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4af5d-123">The tenant ID of the client making the request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af5d-124">-DefaultProfile</span></span>
<span data-ttu-id="4af5d-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4af5d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="4af5d-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="4af5d-127">Nome del corriere usato per spedire le unità di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="4af5d-127">The name of the carrier that is used to ship the import or export drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="4af5d-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="4af5d-129">Il numero di unità incluse nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4af5d-129">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="4af5d-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="4af5d-131">Data di spedizione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4af5d-131">The date when the package is shipped.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="4af5d-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="4af5d-133">Il numero di tracciamento del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4af5d-133">The tracking number of the package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="4af5d-134">-DiagnosticsPath</span></span>
<span data-ttu-id="4af5d-135">Directory BLOB virtuale in cui verranno archiviati i log di copia e le copie di backup dei file manifesto dell'unità (se abilitati).</span><span class="sxs-lookup"><span data-stu-id="4af5d-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="4af5d-136">-DriveList</span></span>
<span data-ttu-id="4af5d-137">Elenco di un massimo di dieci unità che costituiscono il processo.</span><span class="sxs-lookup"><span data-stu-id="4af5d-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="4af5d-138">L'elenco di unità è un elemento obbligatorio per un processo di importazione; non è specificato per i processi di esportazione.</span><span class="sxs-lookup"><span data-stu-id="4af5d-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="4af5d-139">Per creare, vedere la sezione NOTE per le proprietà DRIVELIST e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4af5d-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="4af5d-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="4af5d-141">URI relativo al BLOB di blocco che contiene l'elenco di percorsi BLOB o prefissi di percorso BLOB definiti in precedenza, a partire dal nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="4af5d-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="4af5d-142">Se il BLOB si trova nel contenitore radice, l'URI deve iniziare con $root.</span><span class="sxs-lookup"><span data-stu-id="4af5d-142">If the blob is in root container, the URI must begin with $root.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="4af5d-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="4af5d-144">Percorso BLOB che punta a un BLOB di blocco contenente un elenco di nomi DI BLOB non esportati a causa di spazio insufficiente sull'unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="4af5d-145">Se tutti i BLOB sono stati esportati correttamente, questo elemento non è incluso nella risposta.</span><span class="sxs-lookup"><span data-stu-id="4af5d-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="4af5d-146">-JobType</span></span>
<span data-ttu-id="4af5d-147">Tipo di processo</span><span class="sxs-lookup"><span data-stu-id="4af5d-147">The type of job</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-148">-Location</span><span class="sxs-lookup"><span data-stu-id="4af5d-148">-Location</span></span>
<span data-ttu-id="4af5d-149">Specifica la posizione di Azure supportata in cui deve essere creato il processo</span><span class="sxs-lookup"><span data-stu-id="4af5d-149">Specifies the supported Azure location where the job should be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="4af5d-150">-LogLevel</span></span>
<span data-ttu-id="4af5d-151">Il valore predefinito è Error.</span><span class="sxs-lookup"><span data-stu-id="4af5d-151">Default value is Error.</span></span>
<span data-ttu-id="4af5d-152">Indica se la registrazione degli errori o la registrazione dettagliata verrà abilitata.</span><span class="sxs-lookup"><span data-stu-id="4af5d-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-153">-Name</span><span class="sxs-lookup"><span data-stu-id="4af5d-153">-Name</span></span>
<span data-ttu-id="4af5d-154">Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="4af5d-154">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="4af5d-155">-PercentComplete</span></span>
<span data-ttu-id="4af5d-156">Percentuale complessiva completata per il processo.</span><span class="sxs-lookup"><span data-stu-id="4af5d-156">Overall percentage completed for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="4af5d-157">-ProvisioningState</span></span>
<span data-ttu-id="4af5d-158">Specifica lo stato di provisioning del processo.</span><span class="sxs-lookup"><span data-stu-id="4af5d-158">Specifies the provisioning state of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af5d-159">-ResourceGroupName</span></span>
<span data-ttu-id="4af5d-160">Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4af5d-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="4af5d-161">-ReturnAddressCity</span></span>
<span data-ttu-id="4af5d-162">Il nome della città da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-162">The city name to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="4af5d-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="4af5d-164">Il paese o l'area geografica da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-164">The country or region to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="4af5d-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="4af5d-166">Indirizzo di posta elettronica del destinatario delle unità restituite.</span><span class="sxs-lookup"><span data-stu-id="4af5d-166">Email address of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="4af5d-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="4af5d-168">Numero di telefono del destinatario delle unità restituite.</span><span class="sxs-lookup"><span data-stu-id="4af5d-168">Phone number of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="4af5d-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="4af5d-170">Codice postale da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-170">The postal code to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="4af5d-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="4af5d-172">Nome del destinatario che riceverà i dischi rigidi quando vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="4af5d-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="4af5d-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="4af5d-174">Lo stato o la provincia da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-174">The state or province to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="4af5d-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="4af5d-176">Prima riga dell'indirizzo da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-176">The first line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="4af5d-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="4af5d-178">Seconda riga dell'indirizzo da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-178">The second line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="4af5d-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="4af5d-180">Nome del corriere usato per spedire le unità di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="4af5d-180">The name of the carrier that is used to ship the import or export drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="4af5d-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="4af5d-182">Il numero di unità incluse nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4af5d-182">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="4af5d-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="4af5d-184">Data di spedizione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4af5d-184">The date when the package is shipped.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="4af5d-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="4af5d-186">Il numero di tracciamento del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4af5d-186">The tracking number of the package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="4af5d-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="4af5d-188">Numero di account del cliente con il corriere.</span><span class="sxs-lookup"><span data-stu-id="4af5d-188">The customer's account number with the carrier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="4af5d-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="4af5d-190">Nome del corriere.</span><span class="sxs-lookup"><span data-stu-id="4af5d-190">The carrier's name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="4af5d-191">-ShippingInformationCity</span></span>
<span data-ttu-id="4af5d-192">Il nome della città da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-192">The city name to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="4af5d-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="4af5d-194">Il paese o l'area geografica da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-194">The country or region to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="4af5d-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="4af5d-196">Numero di telefono del destinatario delle unità restituite.</span><span class="sxs-lookup"><span data-stu-id="4af5d-196">Phone number of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="4af5d-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="4af5d-198">Codice postale da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-198">The postal code to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="4af5d-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="4af5d-200">Nome del destinatario che riceverà i dischi rigidi quando vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="4af5d-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="4af5d-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="4af5d-202">Lo stato o la provincia da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-202">The state or province to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="4af5d-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="4af5d-204">Prima riga dell'indirizzo da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-204">The first line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="4af5d-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="4af5d-206">Seconda riga dell'indirizzo da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-206">The second line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-207">-State</span><span class="sxs-lookup"><span data-stu-id="4af5d-207">-State</span></span>
<span data-ttu-id="4af5d-208">Stato corrente del processo.</span><span class="sxs-lookup"><span data-stu-id="4af5d-208">Current state of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4af5d-209">-StorageAccountId</span></span>
<span data-ttu-id="4af5d-210">Identificatore di risorsa dell'account di archiviazione da cui verranno importati o esportati i dati.</span><span class="sxs-lookup"><span data-stu-id="4af5d-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4af5d-211">-SubscriptionId</span></span>
<span data-ttu-id="4af5d-212">ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="4af5d-212">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-213">-Tag</span><span class="sxs-lookup"><span data-stu-id="4af5d-213">-Tag</span></span>
<span data-ttu-id="4af5d-214">Specifica i tag che verranno assegnati al processo.</span><span class="sxs-lookup"><span data-stu-id="4af5d-214">Specifies the tags that will be assigned to the job.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IPutJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af5d-215">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4af5d-215">-Confirm</span></span>
<span data-ttu-id="4af5d-216">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4af5d-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4af5d-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4af5d-217">-WhatIf</span></span>
<span data-ttu-id="4af5d-218">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4af5d-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4af5d-219">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4af5d-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4af5d-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af5d-220">CommonParameters</span></span>
<span data-ttu-id="4af5d-221">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af5d-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af5d-222">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4af5d-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af5d-223">INPUT</span><span class="sxs-lookup"><span data-stu-id="4af5d-223">INPUTS</span></span>

## <span data-ttu-id="4af5d-224">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4af5d-224">OUTPUTS</span></span>

### <span data-ttu-id="4af5d-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="4af5d-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="4af5d-226">NOTE</span><span class="sxs-lookup"><span data-stu-id="4af5d-226">NOTES</span></span>

<span data-ttu-id="4af5d-227">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4af5d-227">ALIASES</span></span>

<span data-ttu-id="4af5d-228">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="4af5d-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4af5d-229">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4af5d-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4af5d-230">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4af5d-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4af5d-231">DRIVELIST <IDriveStatus[]>: elenco di un massimo di dieci unità che costituiscono il processo.</span><span class="sxs-lookup"><span data-stu-id="4af5d-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="4af5d-232">L'elenco di unità è un elemento obbligatorio per un processo di importazione; non è specificato per i processi di esportazione.</span><span class="sxs-lookup"><span data-stu-id="4af5d-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="4af5d-233">`[BitLockerKey <String>]`: chiave BitLocker usata per crittografare l'unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="4af5d-234">`[BytesSucceeded <Int64?>]`: i byte trasferiti correttamente per l'unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="4af5d-235">`[CopyStatus <String>]`: stato dettagliato sul processo di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="4af5d-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="4af5d-236">Questo campo non viene restituito nella risposta finché l'unità non è in stato di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="4af5d-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="4af5d-237">`[DriveHeaderHash <String>]`: valore hash dell'intestazione dell'unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="4af5d-238">`[DriveId <String>]`: numero di serie dell'hardware dell'unità, senza spazi.</span><span class="sxs-lookup"><span data-stu-id="4af5d-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="4af5d-239">`[ErrorLogUri <String>]`: UN URI che punta al BLOB contenente il log degli errori per l'operazione di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="4af5d-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="4af5d-240">`[ManifestFile <String>]`: il percorso relativo del file manifesto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="4af5d-241">`[ManifestHash <String>]`: hash MD5 codificato in Base16 del file manifesto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="4af5d-242">`[ManifestUri <String>]`: UN URI che punta al BLOB che contiene il file manifesto dell'unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="4af5d-243">`[PercentComplete <Int32?>]`: percentuale di completamento per l'unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="4af5d-244">`[State <DriveState?>]`: lo stato corrente dell'unità.</span><span class="sxs-lookup"><span data-stu-id="4af5d-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="4af5d-245">`[VerboseLogUri <String>]`: UN URI che punta al BLOB contenente il log dettagliato per l'operazione di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="4af5d-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="4af5d-246">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4af5d-246">RELATED LINKS</span></span>

