---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: 7b604c22878d3d76e66a6d615deb1b46cedaad32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974926"
---
# <span data-ttu-id="a04b9-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="a04b9-101">Update-AzImportExport</span></span>

## <span data-ttu-id="a04b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a04b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a04b9-103">Aggiorna proprietà specifiche di un processo.</span><span class="sxs-lookup"><span data-stu-id="a04b9-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="a04b9-104">È possibile chiamare questa operazione per notificare al servizio di importazione/esportazione che i dischi rigidi che comprendono il processo di importazione o esportazione sono stati spediti al data center Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a04b9-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="a04b9-105">Può anche essere usato per annullare un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="a04b9-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="a04b9-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a04b9-106">SYNTAX</span></span>

### <span data-ttu-id="a04b9-107">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a04b9-107">UpdateExpanded (Default)</span></span>
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a04b9-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a04b9-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a04b9-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a04b9-109">DESCRIPTION</span></span>
<span data-ttu-id="a04b9-110">Aggiorna proprietà specifiche di un processo.</span><span class="sxs-lookup"><span data-stu-id="a04b9-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="a04b9-111">È possibile chiamare questa operazione per notificare al servizio di importazione/esportazione che i dischi rigidi che comprendono il processo di importazione o esportazione sono stati spediti al data center Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a04b9-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="a04b9-112">Può anche essere usato per annullare un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="a04b9-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="a04b9-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a04b9-113">EXAMPLES</span></span>

### <span data-ttu-id="a04b9-114">Esempio 1: Aggiornare il processo ImportExport in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="a04b9-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="a04b9-115">Questo cmdlet aggiorna il processo ImportExport in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="a04b9-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="a04b9-116">Esempio 2: Aggiornare il processo ImportExport in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="a04b9-117">Questo cmdlet aggiorna il processo ImportExport in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="a04b9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a04b9-118">PARAMETERS</span></span>

### <span data-ttu-id="a04b9-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="a04b9-119">-AcceptLanguage</span></span>
<span data-ttu-id="a04b9-120">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="a04b9-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="a04b9-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="a04b9-121">-BackupDriveManifest</span></span>
<span data-ttu-id="a04b9-122">Indica se i file manifesto nelle unità devono essere copiati per bloccare BLOB.</span><span class="sxs-lookup"><span data-stu-id="a04b9-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="a04b9-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="a04b9-123">-CancelRequested</span></span>
<span data-ttu-id="a04b9-124">Se specificato, il valore deve essere vero.</span><span class="sxs-lookup"><span data-stu-id="a04b9-124">If specified, the value must be true.</span></span>
<span data-ttu-id="a04b9-125">Il servizio tenterà di annullare il processo.</span><span class="sxs-lookup"><span data-stu-id="a04b9-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="a04b9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a04b9-126">-DefaultProfile</span></span>
<span data-ttu-id="a04b9-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a04b9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a04b9-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="a04b9-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="a04b9-129">Nome del corriere usato per spedire le unità di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="a04b9-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="a04b9-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="a04b9-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="a04b9-131">Il numero di unità incluse nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a04b9-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="a04b9-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="a04b9-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="a04b9-133">Data di spedizione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a04b9-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="a04b9-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="a04b9-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="a04b9-135">Il numero di tracciamento del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a04b9-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="a04b9-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="a04b9-136">-DriveList</span></span>
<span data-ttu-id="a04b9-137">Elenco delle unità che costituiscono il processo.</span><span class="sxs-lookup"><span data-stu-id="a04b9-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="a04b9-138">Per creare, vedere la sezione NOTE per le proprietà DRIVELIST e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a04b9-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="a04b9-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a04b9-139">-InputObject</span></span>
<span data-ttu-id="a04b9-140">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a04b9-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a04b9-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="a04b9-141">-LogLevel</span></span>
<span data-ttu-id="a04b9-142">Indica se la registrazione degli errori o la registrazione dettagliata è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a04b9-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="a04b9-143">-Name</span><span class="sxs-lookup"><span data-stu-id="a04b9-143">-Name</span></span>
<span data-ttu-id="a04b9-144">Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="a04b9-144">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04b9-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a04b9-145">-ResourceGroupName</span></span>
<span data-ttu-id="a04b9-146">Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a04b9-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04b9-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="a04b9-147">-ReturnAddressCity</span></span>
<span data-ttu-id="a04b9-148">Il nome della città da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="a04b9-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="a04b9-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="a04b9-150">Il paese o l'area geografica da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="a04b9-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="a04b9-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="a04b9-152">Indirizzo di posta elettronica del destinatario delle unità restituite.</span><span class="sxs-lookup"><span data-stu-id="a04b9-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="a04b9-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="a04b9-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="a04b9-154">Numero di telefono del destinatario delle unità restituite.</span><span class="sxs-lookup"><span data-stu-id="a04b9-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="a04b9-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="a04b9-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="a04b9-156">Codice postale da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="a04b9-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="a04b9-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="a04b9-158">Nome del destinatario che riceverà i dischi rigidi quando vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="a04b9-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="a04b9-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="a04b9-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="a04b9-160">Lo stato o la provincia da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="a04b9-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="a04b9-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="a04b9-162">Prima riga dell'indirizzo da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="a04b9-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="a04b9-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="a04b9-164">Seconda riga dell'indirizzo da usare per restituire le unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="a04b9-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="a04b9-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="a04b9-166">Numero di account del cliente con il corriere.</span><span class="sxs-lookup"><span data-stu-id="a04b9-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="a04b9-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="a04b9-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="a04b9-168">Nome del corriere.</span><span class="sxs-lookup"><span data-stu-id="a04b9-168">The carrier's name.</span></span>

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

### <span data-ttu-id="a04b9-169">-State</span><span class="sxs-lookup"><span data-stu-id="a04b9-169">-State</span></span>
<span data-ttu-id="a04b9-170">Se specificato, il valore deve essere In spedizione, che indica al servizio di importazione/esportazione che il pacchetto per il processo è stato spedito.</span><span class="sxs-lookup"><span data-stu-id="a04b9-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="a04b9-171">Le proprietà ReturnAddress e DeliveryPackage devono essere state impostate in questa richiesta o in una richiesta precedente, altrimenti la richiesta non riesce.</span><span class="sxs-lookup"><span data-stu-id="a04b9-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="a04b9-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a04b9-172">-SubscriptionId</span></span>
<span data-ttu-id="a04b9-173">ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="a04b9-173">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04b9-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="a04b9-174">-Tag</span></span>
<span data-ttu-id="a04b9-175">Specifica i tag che verranno assegnati al processo</span><span class="sxs-lookup"><span data-stu-id="a04b9-175">Specifies the tags that will be assigned to the job</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04b9-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a04b9-176">-Confirm</span></span>
<span data-ttu-id="a04b9-177">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a04b9-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a04b9-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a04b9-178">-WhatIf</span></span>
<span data-ttu-id="a04b9-179">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a04b9-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a04b9-180">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a04b9-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a04b9-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a04b9-181">CommonParameters</span></span>
<span data-ttu-id="a04b9-182">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a04b9-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a04b9-183">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a04b9-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a04b9-184">INPUT</span><span class="sxs-lookup"><span data-stu-id="a04b9-184">INPUTS</span></span>

### <span data-ttu-id="a04b9-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="a04b9-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="a04b9-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a04b9-186">OUTPUTS</span></span>

### <span data-ttu-id="a04b9-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="a04b9-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="a04b9-188">NOTE</span><span class="sxs-lookup"><span data-stu-id="a04b9-188">NOTES</span></span>

<span data-ttu-id="a04b9-189">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a04b9-189">ALIASES</span></span>

<span data-ttu-id="a04b9-190">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a04b9-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a04b9-191">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a04b9-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a04b9-192">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a04b9-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a04b9-193">DRIVELIST <IDriveStatus[]>: elenco delle unità che costituiscono il processo.</span><span class="sxs-lookup"><span data-stu-id="a04b9-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="a04b9-194">`[BitLockerKey <String>]`: chiave BitLocker usata per crittografare l'unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="a04b9-195">`[BytesSucceeded <Int64?>]`: i byte trasferiti correttamente per l'unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="a04b9-196">`[CopyStatus <String>]`: stato dettagliato sul processo di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="a04b9-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="a04b9-197">Questo campo non viene restituito nella risposta finché l'unità non è in stato di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="a04b9-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="a04b9-198">`[DriveHeaderHash <String>]`: valore hash dell'intestazione dell'unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="a04b9-199">`[DriveId <String>]`: numero di serie dell'hardware dell'unità, senza spazi.</span><span class="sxs-lookup"><span data-stu-id="a04b9-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="a04b9-200">`[ErrorLogUri <String>]`: UN URI che punta al BLOB contenente il log degli errori per l'operazione di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="a04b9-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="a04b9-201">`[ManifestFile <String>]`: il percorso relativo del file manifesto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="a04b9-202">`[ManifestHash <String>]`: hash MD5 codificato in Base16 del file manifesto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="a04b9-203">`[ManifestUri <String>]`: UN URI che punta al BLOB che contiene il file manifesto dell'unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="a04b9-204">`[PercentComplete <Int32?>]`: percentuale di completamento per l'unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="a04b9-205">`[State <DriveState?>]`: lo stato corrente dell'unità.</span><span class="sxs-lookup"><span data-stu-id="a04b9-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="a04b9-206">`[VerboseLogUri <String>]`: URI che punta al BLOB contenente il log dettagliato per l'operazione di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="a04b9-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="a04b9-207">INPUTOBJECT <IImportExportIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a04b9-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a04b9-208">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a04b9-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a04b9-209">`[JobName <String>]`: nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="a04b9-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="a04b9-210">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="a04b9-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="a04b9-211">Ad esempio, Stati Uniti occidentali o Ovest.</span><span class="sxs-lookup"><span data-stu-id="a04b9-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="a04b9-212">`[ResourceGroupName <String>]`: il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a04b9-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="a04b9-213">`[SubscriptionId <String>]`: ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="a04b9-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="a04b9-214">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a04b9-214">RELATED LINKS</span></span>

