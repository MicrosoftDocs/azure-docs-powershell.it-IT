---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487136"
---
# <span data-ttu-id="376da-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="376da-101">Update-AzImportExport</span></span>

## <span data-ttu-id="376da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="376da-102">SYNOPSIS</span></span>
<span data-ttu-id="376da-103">Aggiorna le proprietà specifiche di un processo.</span><span class="sxs-lookup"><span data-stu-id="376da-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="376da-104">Puoi chiamare questa operazione per notificare al servizio di importazione/esportazione che i dischi rigidi che includono il processo di importazione o esportazione sono stati spediti al Data Center Microsoft.</span><span class="sxs-lookup"><span data-stu-id="376da-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="376da-105">Può essere usato anche per annullare un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="376da-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="376da-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="376da-106">SYNTAX</span></span>

### <span data-ttu-id="376da-107">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="376da-107">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="376da-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="376da-108">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="376da-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="376da-109">DESCRIPTION</span></span>
<span data-ttu-id="376da-110">Aggiorna le proprietà specifiche di un processo.</span><span class="sxs-lookup"><span data-stu-id="376da-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="376da-111">Puoi chiamare questa operazione per notificare al servizio di importazione/esportazione che i dischi rigidi che includono il processo di importazione o esportazione sono stati spediti al Data Center Microsoft.</span><span class="sxs-lookup"><span data-stu-id="376da-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="376da-112">Può essere usato anche per annullare un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="376da-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="376da-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="376da-113">EXAMPLES</span></span>

### <span data-ttu-id="376da-114">Esempio 1: aggiornare il processo di ImportExport in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="376da-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="376da-115">Questo cmdlet aggiorna ImportExport processo in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="376da-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="376da-116">Esempio 2: aggiornare il processo di ImportExport per identità.</span><span class="sxs-lookup"><span data-stu-id="376da-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="376da-117">Questo cmdlet aggiorna ImportExport processo per identità.</span><span class="sxs-lookup"><span data-stu-id="376da-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="376da-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="376da-118">PARAMETERS</span></span>

### <span data-ttu-id="376da-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="376da-119">-AcceptLanguage</span></span>
<span data-ttu-id="376da-120">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="376da-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="376da-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="376da-121">-BackupDriveManifest</span></span>
<span data-ttu-id="376da-122">Indica se i file manifesto delle unità devono essere copiati per bloccare i BLOB.</span><span class="sxs-lookup"><span data-stu-id="376da-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="376da-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="376da-123">-CancelRequested</span></span>
<span data-ttu-id="376da-124">Se specificato, il valore deve essere vero.</span><span class="sxs-lookup"><span data-stu-id="376da-124">If specified, the value must be true.</span></span>
<span data-ttu-id="376da-125">Il servizio tenterà di annullare il processo.</span><span class="sxs-lookup"><span data-stu-id="376da-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="376da-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376da-126">-DefaultProfile</span></span>
<span data-ttu-id="376da-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="376da-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="376da-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="376da-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="376da-129">Nome del vettore usato per spedire le unità di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="376da-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="376da-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="376da-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="376da-131">Il numero di unità incluse nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="376da-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="376da-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="376da-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="376da-133">Data in cui viene spedito il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="376da-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="376da-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="376da-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="376da-135">Numero di tracking del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="376da-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="376da-136">-Unità</span><span class="sxs-lookup"><span data-stu-id="376da-136">-DriveList</span></span>
<span data-ttu-id="376da-137">Elenco di unità che compongono il processo.</span><span class="sxs-lookup"><span data-stu-id="376da-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="376da-138">Per creare una tabella hash, vedere la sezione Note per le proprietà dell'unità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="376da-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="376da-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="376da-139">-InputObject</span></span>
<span data-ttu-id="376da-140">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="376da-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="376da-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="376da-141">-LogLevel</span></span>
<span data-ttu-id="376da-142">Indica se è abilitata la registrazione degli errori o la registrazione dettagliata.</span><span class="sxs-lookup"><span data-stu-id="376da-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="376da-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="376da-143">-Name</span></span>
<span data-ttu-id="376da-144">Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="376da-144">The name of the import/export job.</span></span>

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

### <span data-ttu-id="376da-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="376da-145">-ResourceGroupName</span></span>
<span data-ttu-id="376da-146">Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="376da-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="376da-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="376da-147">-ReturnAddressCity</span></span>
<span data-ttu-id="376da-148">Il nome della città da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="376da-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="376da-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="376da-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="376da-150">Paese o area geografica da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="376da-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="376da-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="376da-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="376da-152">Indirizzo di posta elettronica del destinatario delle unità restituite.</span><span class="sxs-lookup"><span data-stu-id="376da-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="376da-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="376da-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="376da-154">Numero di telefono del destinatario delle unità restituite.</span><span class="sxs-lookup"><span data-stu-id="376da-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="376da-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="376da-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="376da-156">Codice postale da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="376da-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="376da-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="376da-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="376da-158">Nome del destinatario che riceverà i dischi rigidi quando vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="376da-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="376da-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="376da-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="376da-160">Lo stato o la provincia da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="376da-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="376da-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="376da-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="376da-162">La prima riga dell'indirizzo di strada da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="376da-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="376da-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="376da-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="376da-164">Seconda riga dell'indirizzo di strada da usare per la restituzione delle unità.</span><span class="sxs-lookup"><span data-stu-id="376da-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="376da-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="376da-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="376da-166">Numero di account del cliente con il vettore.</span><span class="sxs-lookup"><span data-stu-id="376da-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="376da-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="376da-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="376da-168">Nome del vettore.</span><span class="sxs-lookup"><span data-stu-id="376da-168">The carrier's name.</span></span>

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

### <span data-ttu-id="376da-169">-Stato</span><span class="sxs-lookup"><span data-stu-id="376da-169">-State</span></span>
<span data-ttu-id="376da-170">Se specificato, il valore deve essere shipping, che indica al servizio di importazione/esportazione che il pacchetto per il processo è stato spedito.</span><span class="sxs-lookup"><span data-stu-id="376da-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="376da-171">Le proprietà ReturnAddress e DeliveryPackage devono essere state impostate in questa richiesta o in una richiesta precedente, altrimenti la richiesta non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="376da-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="376da-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="376da-172">-SubscriptionId</span></span>
<span data-ttu-id="376da-173">ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="376da-173">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="376da-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="376da-174">-Tag</span></span>
<span data-ttu-id="376da-175">Specifica i tag che verranno assegnati al processo</span><span class="sxs-lookup"><span data-stu-id="376da-175">Specifies the tags that will be assigned to the job</span></span>

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

### <span data-ttu-id="376da-176">-Confermare</span><span class="sxs-lookup"><span data-stu-id="376da-176">-Confirm</span></span>
<span data-ttu-id="376da-177">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="376da-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="376da-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="376da-178">-WhatIf</span></span>
<span data-ttu-id="376da-179">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="376da-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="376da-180">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="376da-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="376da-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376da-181">CommonParameters</span></span>
<span data-ttu-id="376da-182">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="376da-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376da-183">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="376da-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376da-184">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="376da-184">INPUTS</span></span>

### <span data-ttu-id="376da-185">Microsoft. Azure. PowerShell. Cmdlets. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="376da-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="376da-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="376da-186">OUTPUTS</span></span>

### <span data-ttu-id="376da-187">Microsoft. Azure. PowerShell. Cmdlets. ImportExport. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="376da-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="376da-188">Note</span><span class="sxs-lookup"><span data-stu-id="376da-188">NOTES</span></span>

<span data-ttu-id="376da-189">ALIAS</span><span class="sxs-lookup"><span data-stu-id="376da-189">ALIASES</span></span>

<span data-ttu-id="376da-190">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="376da-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="376da-191">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="376da-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="376da-192">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="376da-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="376da-193"><IDriveStatus [] >: elenco delle unità che costituiscono il processo.</span><span class="sxs-lookup"><span data-stu-id="376da-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="376da-194">`[BitLockerKey <String>]`: Chiave di BitLocker usata per crittografare l'unità.</span><span class="sxs-lookup"><span data-stu-id="376da-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="376da-195">`[BytesSucceeded <Int64?>]`: Byte trasferiti correttamente per l'unità.</span><span class="sxs-lookup"><span data-stu-id="376da-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="376da-196">`[CopyStatus <String>]`: Stato dettagliato del processo di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="376da-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="376da-197">Questo campo non viene restituito nella risposta finché l'unità non si trova nello stato di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="376da-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="376da-198">`[DriveHeaderHash <String>]`: Valore hash dell'intestazione dell'unità.</span><span class="sxs-lookup"><span data-stu-id="376da-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="376da-199">`[DriveId <String>]`: Numero seriale hardware dell'unità, senza spazi.</span><span class="sxs-lookup"><span data-stu-id="376da-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="376da-200">`[ErrorLogUri <String>]`: URI che punta al BLOB che contiene il log degli errori per l'operazione di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="376da-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="376da-201">`[ManifestFile <String>]`: Percorso relativo del file manifesto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="376da-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="376da-202">`[ManifestHash <String>]`: L'hash MD5 con codifica Base16 del file manifesto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="376da-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="376da-203">`[ManifestUri <String>]`: URI che punta al BLOB che contiene il file manifesto dell'unità.</span><span class="sxs-lookup"><span data-stu-id="376da-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="376da-204">`[PercentComplete <Int32?>]`: Percentuale completata per l'unità.</span><span class="sxs-lookup"><span data-stu-id="376da-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="376da-205">`[State <DriveState?>]`: Lo stato corrente dell'unità.</span><span class="sxs-lookup"><span data-stu-id="376da-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="376da-206">`[VerboseLogUri <String>]`: URI che punta al BLOB contenente il log dettagliato per l'operazione di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="376da-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="376da-207">INPUTOBJECT <IImportExportIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="376da-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="376da-208">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="376da-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="376da-209">`[JobName <String>]`: Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="376da-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="376da-210">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="376da-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="376da-211">Ad esempio, ovest degli Stati Uniti o westus.</span><span class="sxs-lookup"><span data-stu-id="376da-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="376da-212">`[ResourceGroupName <String>]`: Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="376da-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="376da-213">`[SubscriptionId <String>]`: ID abbonamento per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="376da-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="376da-214">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="376da-214">RELATED LINKS</span></span>

