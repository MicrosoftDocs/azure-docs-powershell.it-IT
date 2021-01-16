---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364514"
---
# <span data-ttu-id="69637-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="69637-101">New-AzImportExport</span></span>

## <span data-ttu-id="69637-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69637-102">SYNOPSIS</span></span>
<span data-ttu-id="69637-103">Crea un nuovo processo o aggiorna un processo esistente nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="69637-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="69637-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69637-104">SYNTAX</span></span>

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

## <span data-ttu-id="69637-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69637-105">DESCRIPTION</span></span>
<span data-ttu-id="69637-106">Crea un nuovo processo o aggiorna un processo esistente nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="69637-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="69637-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69637-107">EXAMPLES</span></span>

### <span data-ttu-id="69637-108">Esempio 1: creare un nuovo processo di ImportExport</span><span class="sxs-lookup"><span data-stu-id="69637-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="69637-109">Questi cmdlet creano un nuovo processo di ImportExport.</span><span class="sxs-lookup"><span data-stu-id="69637-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="69637-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69637-110">PARAMETERS</span></span>

### <span data-ttu-id="69637-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="69637-111">-AcceptLanguage</span></span>
<span data-ttu-id="69637-112">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="69637-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="69637-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="69637-113">-BackupDriveManifest</span></span>
<span data-ttu-id="69637-114">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="69637-114">Default value is false.</span></span>
<span data-ttu-id="69637-115">Indica se i file manifesto delle unità devono essere copiati per bloccare i BLOB.</span><span class="sxs-lookup"><span data-stu-id="69637-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="69637-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="69637-116">-BlobListBlobPath</span></span>
<span data-ttu-id="69637-117">Una raccolta di stringhe di percorsi BLOB.</span><span class="sxs-lookup"><span data-stu-id="69637-117">A collection of blob-path strings.</span></span>

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

### <span data-ttu-id="69637-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="69637-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="69637-119">Una raccolta di stringhe di prefisso BLOB.</span><span class="sxs-lookup"><span data-stu-id="69637-119">A collection of blob-prefix strings.</span></span>

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

### <span data-ttu-id="69637-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="69637-120">-CancelRequested</span></span>
<span data-ttu-id="69637-121">Indica se una richiesta è stata inviata per annullare il processo.</span><span class="sxs-lookup"><span data-stu-id="69637-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="69637-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="69637-122">-ClientTenantId</span></span>
<span data-ttu-id="69637-123">ID tenant del client che effettua la richiesta.</span><span class="sxs-lookup"><span data-stu-id="69637-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="69637-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69637-124">-DefaultProfile</span></span>
<span data-ttu-id="69637-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69637-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69637-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="69637-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="69637-127">Nome del vettore usato per spedire le unità di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="69637-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="69637-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="69637-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="69637-129">Il numero di unità incluse nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="69637-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="69637-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="69637-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="69637-131">Data in cui viene spedito il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="69637-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="69637-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="69637-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="69637-133">Numero di tracking del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="69637-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="69637-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="69637-134">-DiagnosticsPath</span></span>
<span data-ttu-id="69637-135">Directory BLOB virtuale in cui vengono archiviati i registri di copia e i backup dei file di manifesto dell'unità (se abilitati).</span><span class="sxs-lookup"><span data-stu-id="69637-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="69637-136">-Unità</span><span class="sxs-lookup"><span data-stu-id="69637-136">-DriveList</span></span>
<span data-ttu-id="69637-137">Elenco di un massimo di dieci unità che costituiscono il processo.</span><span class="sxs-lookup"><span data-stu-id="69637-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="69637-138">L'elenco di unità è un elemento obbligatorio per un processo di importazione; non viene specificato per i processi di esportazione.</span><span class="sxs-lookup"><span data-stu-id="69637-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="69637-139">Per creare una tabella hash, vedere la sezione Note per le proprietà dell'unità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="69637-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="69637-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="69637-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="69637-141">URI relativo al BLOB del blocco che contiene l'elenco di percorsi BLOB o di prefissi di percorso BLOB come definiti sopra, a partire dal nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="69637-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="69637-142">Se il BLOB è nel contenitore radice, l'URI deve iniziare con $root.</span><span class="sxs-lookup"><span data-stu-id="69637-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="69637-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="69637-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="69637-144">Un percorso BLOB che punta a un BLOB di blocco che contiene un elenco di nomi BLOB non esportati a causa dello spazio di unità insufficiente.</span><span class="sxs-lookup"><span data-stu-id="69637-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="69637-145">Se tutti i BLOB sono stati esportati correttamente, questo elemento non è incluso nella risposta.</span><span class="sxs-lookup"><span data-stu-id="69637-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="69637-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="69637-146">-JobType</span></span>
<span data-ttu-id="69637-147">Tipo di processo</span><span class="sxs-lookup"><span data-stu-id="69637-147">The type of job</span></span>

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

### <span data-ttu-id="69637-148">-Posizione</span><span class="sxs-lookup"><span data-stu-id="69637-148">-Location</span></span>
<span data-ttu-id="69637-149">Specifica il percorso di Azure supportato in cui deve essere creato il processo</span><span class="sxs-lookup"><span data-stu-id="69637-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="69637-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="69637-150">-LogLevel</span></span>
<span data-ttu-id="69637-151">Il valore predefinito è Error.</span><span class="sxs-lookup"><span data-stu-id="69637-151">Default value is Error.</span></span>
<span data-ttu-id="69637-152">Indica se la registrazione degli errori o la registrazione dettagliata verrà abilitata.</span><span class="sxs-lookup"><span data-stu-id="69637-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="69637-153">-Nome</span><span class="sxs-lookup"><span data-stu-id="69637-153">-Name</span></span>
<span data-ttu-id="69637-154">Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="69637-154">The name of the import/export job.</span></span>

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

### <span data-ttu-id="69637-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="69637-155">-PercentComplete</span></span>
<span data-ttu-id="69637-156">Percentuale complessiva completata per il processo.</span><span class="sxs-lookup"><span data-stu-id="69637-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="69637-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="69637-157">-ProvisioningState</span></span>
<span data-ttu-id="69637-158">Specifica lo stato di provisioning del processo.</span><span class="sxs-lookup"><span data-stu-id="69637-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="69637-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69637-159">-ResourceGroupName</span></span>
<span data-ttu-id="69637-160">Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="69637-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="69637-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="69637-161">-ReturnAddressCity</span></span>
<span data-ttu-id="69637-162">Il nome della città da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="69637-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="69637-164">Paese o area geografica da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="69637-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="69637-166">Indirizzo di posta elettronica del destinatario delle unità restituite.</span><span class="sxs-lookup"><span data-stu-id="69637-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="69637-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="69637-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="69637-168">Numero di telefono del destinatario delle unità restituite.</span><span class="sxs-lookup"><span data-stu-id="69637-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="69637-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="69637-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="69637-170">Codice postale da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="69637-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="69637-172">Nome del destinatario che riceverà i dischi rigidi quando vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="69637-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="69637-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="69637-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="69637-174">Lo stato o la provincia da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="69637-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="69637-176">La prima riga dell'indirizzo di strada da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="69637-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="69637-178">Seconda riga dell'indirizzo di strada da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="69637-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="69637-180">Nome del vettore usato per spedire le unità di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="69637-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="69637-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="69637-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="69637-182">Il numero di unità incluse nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="69637-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="69637-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="69637-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="69637-184">Data in cui viene spedito il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="69637-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="69637-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="69637-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="69637-186">Numero di tracking del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="69637-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="69637-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="69637-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="69637-188">Numero di account del cliente con il vettore.</span><span class="sxs-lookup"><span data-stu-id="69637-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="69637-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="69637-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="69637-190">Nome del vettore.</span><span class="sxs-lookup"><span data-stu-id="69637-190">The carrier's name.</span></span>

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

### <span data-ttu-id="69637-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="69637-191">-ShippingInformationCity</span></span>
<span data-ttu-id="69637-192">Il nome della città da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="69637-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="69637-194">Paese o area geografica da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="69637-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="69637-196">Numero di telefono del destinatario delle unità restituite.</span><span class="sxs-lookup"><span data-stu-id="69637-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="69637-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="69637-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="69637-198">Codice postale da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="69637-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="69637-200">Nome del destinatario che riceverà i dischi rigidi quando vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="69637-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="69637-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="69637-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="69637-202">Lo stato o la provincia da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="69637-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="69637-204">La prima riga dell'indirizzo di strada da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="69637-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="69637-206">Seconda riga dell'indirizzo di strada da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="69637-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="69637-207">-Stato</span><span class="sxs-lookup"><span data-stu-id="69637-207">-State</span></span>
<span data-ttu-id="69637-208">Stato corrente del processo.</span><span class="sxs-lookup"><span data-stu-id="69637-208">Current state of the job.</span></span>

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

### <span data-ttu-id="69637-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="69637-209">-StorageAccountId</span></span>
<span data-ttu-id="69637-210">Identificatore delle risorse dell'account di archiviazione in cui verranno importati o esportati i dati.</span><span class="sxs-lookup"><span data-stu-id="69637-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="69637-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69637-211">-SubscriptionId</span></span>
<span data-ttu-id="69637-212">ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="69637-212">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="69637-213">-Tag</span><span class="sxs-lookup"><span data-stu-id="69637-213">-Tag</span></span>
<span data-ttu-id="69637-214">Specifica i tag che verranno assegnati al processo.</span><span class="sxs-lookup"><span data-stu-id="69637-214">Specifies the tags that will be assigned to the job.</span></span>

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

### <span data-ttu-id="69637-215">-Confermare</span><span class="sxs-lookup"><span data-stu-id="69637-215">-Confirm</span></span>
<span data-ttu-id="69637-216">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69637-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69637-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69637-217">-WhatIf</span></span>
<span data-ttu-id="69637-218">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69637-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69637-219">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69637-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69637-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69637-220">CommonParameters</span></span>
<span data-ttu-id="69637-221">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69637-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69637-222">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69637-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69637-223">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69637-223">INPUTS</span></span>

## <span data-ttu-id="69637-224">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69637-224">OUTPUTS</span></span>

### <span data-ttu-id="69637-225">Microsoft. Azure. PowerShell. Cmdlets. ImportExport. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="69637-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="69637-226">Note</span><span class="sxs-lookup"><span data-stu-id="69637-226">NOTES</span></span>

<span data-ttu-id="69637-227">ALIAS</span><span class="sxs-lookup"><span data-stu-id="69637-227">ALIASES</span></span>

<span data-ttu-id="69637-228">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69637-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69637-229">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="69637-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69637-230">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="69637-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69637-231"><IDriveStatus [] >: elenco di unità fino a dieci che costituiscono il processo.</span><span class="sxs-lookup"><span data-stu-id="69637-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="69637-232">L'elenco di unità è un elemento obbligatorio per un processo di importazione; non viene specificato per i processi di esportazione.</span><span class="sxs-lookup"><span data-stu-id="69637-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="69637-233">`[BitLockerKey <String>]`: Chiave di BitLocker usata per crittografare l'unità.</span><span class="sxs-lookup"><span data-stu-id="69637-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="69637-234">`[BytesSucceeded <Int64?>]`: Byte trasferiti correttamente per l'unità.</span><span class="sxs-lookup"><span data-stu-id="69637-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="69637-235">`[CopyStatus <String>]`: Stato dettagliato del processo di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="69637-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="69637-236">Questo campo non viene restituito nella risposta finché l'unità non si trova nello stato di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="69637-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="69637-237">`[DriveHeaderHash <String>]`: Valore hash dell'intestazione dell'unità.</span><span class="sxs-lookup"><span data-stu-id="69637-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="69637-238">`[DriveId <String>]`: Numero seriale hardware dell'unità, senza spazi.</span><span class="sxs-lookup"><span data-stu-id="69637-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="69637-239">`[ErrorLogUri <String>]`: URI che punta al BLOB che contiene il log degli errori per l'operazione di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="69637-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="69637-240">`[ManifestFile <String>]`: Percorso relativo del file manifesto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="69637-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="69637-241">`[ManifestHash <String>]`: L'hash MD5 con codifica Base16 del file manifesto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="69637-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="69637-242">`[ManifestUri <String>]`: URI che punta al BLOB che contiene il file manifesto dell'unità.</span><span class="sxs-lookup"><span data-stu-id="69637-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="69637-243">`[PercentComplete <Int32?>]`: Percentuale completata per l'unità.</span><span class="sxs-lookup"><span data-stu-id="69637-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="69637-244">`[State <DriveState?>]`: Lo stato corrente dell'unità.</span><span class="sxs-lookup"><span data-stu-id="69637-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="69637-245">`[VerboseLogUri <String>]`: URI che punta al BLOB contenente il log dettagliato per l'operazione di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="69637-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="69637-246">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69637-246">RELATED LINKS</span></span>

