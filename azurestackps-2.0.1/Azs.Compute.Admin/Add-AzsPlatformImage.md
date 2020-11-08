---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: 127cbe1efb710fff04420590985e97ee72a196a9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023300"
---
# <span data-ttu-id="666fd-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="666fd-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="666fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="666fd-102">SYNOPSIS</span></span>
<span data-ttu-id="666fd-103">Crea una nuova immagine della piattaforma con l'editore, l'offerta, le SKU e la versione specificati.</span><span class="sxs-lookup"><span data-stu-id="666fd-103">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="666fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="666fd-104">SYNTAX</span></span>

### <span data-ttu-id="666fd-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="666fd-105">CreateExpanded (Default)</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-BillingPartNumber <String>] [-DataDisks <IDataDisk[]>] [-OsType <OSType>]
 [-OsUri <String>] [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="666fd-106">Creare</span><span class="sxs-lookup"><span data-stu-id="666fd-106">Create</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 -NewImage <IPlatformImageParameters> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="666fd-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="666fd-107">CreateViaIdentity</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> -NewImage <IPlatformImageParameters>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="666fd-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="666fd-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-BillingPartNumber <String>]
 [-DataDisks <IDataDisk[]>] [-OsType <OSType>] [-OsUri <String>] [-ProvisioningState <ProvisioningState>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="666fd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="666fd-109">DESCRIPTION</span></span>
<span data-ttu-id="666fd-110">Crea una nuova immagine della piattaforma con l'editore, l'offerta, le SKU e la versione specificati.</span><span class="sxs-lookup"><span data-stu-id="666fd-110">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="666fd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="666fd-111">EXAMPLES</span></span>

### <span data-ttu-id="666fd-112">Esempio 1: Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="666fd-112">Example 1: Add-AzsPlatformImage</span></span>
```powershell
PS C:\> Add-AzsPlatformImage -Offer "asdf" -Publisher "asdf" -Sku "asdf" -Version "1.0.0" -OsType Windows -OsUri "https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https&sig=CKkE2r9MJc%2FK40PjRB5Tfz6DArxNd0akD90IvKJX95g%3D"

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
#Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="666fd-113">Aggiungere un'immagine della piattaforma da archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="666fd-113">Add a Platform Image from Blob Storage.</span></span> <span data-ttu-id="666fd-114">USA SasUri per specificare la posizione di PlatformImage oppure usa un URL accessibile pubblicamente.</span><span class="sxs-lookup"><span data-stu-id="666fd-114">Use the a SasUri to specify the location of the PlatformImage, or use a publicly accessible URL.</span></span>

## <span data-ttu-id="666fd-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="666fd-115">PARAMETERS</span></span>

### <span data-ttu-id="666fd-116">Exception. Message</span><span class="sxs-lookup"><span data-stu-id="666fd-116">Exception.Message</span></span>
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

### <span data-ttu-id="666fd-117">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="666fd-117">-BillingPartNumber</span></span>
<span data-ttu-id="666fd-118">Il numero di parte viene usato per fatturare i costi del software.</span><span class="sxs-lookup"><span data-stu-id="666fd-118">The part number is used to bill for software costs.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-119">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="666fd-119">-DataDisks</span></span>
<span data-ttu-id="666fd-120">Dischi di dati usati dall'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="666fd-120">Data disks used by the platform image.</span></span>
<span data-ttu-id="666fd-121">Per creare una tabella hash, vedere la sezione Note per le proprietà dei dischi DataDisk.</span><span class="sxs-lookup"><span data-stu-id="666fd-121">To construct, see NOTES section for DATADISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IDataDisk[]
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666fd-122">-DefaultProfile</span></span>
<span data-ttu-id="666fd-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="666fd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="666fd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="666fd-124">-InputObject</span></span>
<span data-ttu-id="666fd-125">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="666fd-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="666fd-126">-Location</span></span>
<span data-ttu-id="666fd-127">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="666fd-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-128">-NewImage</span><span class="sxs-lookup"><span data-stu-id="666fd-128">-NewImage</span></span>
<span data-ttu-id="666fd-129">Parametri usati per creare una nuova immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="666fd-129">Parameters used to create a new platform image.</span></span>
<span data-ttu-id="666fd-130">Per costruire, vedere la sezione Note per le proprietà di NEWIMAGE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="666fd-130">To construct, see NOTES section for NEWIMAGE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-131">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="666fd-131">-NoWait</span></span>
<span data-ttu-id="666fd-132">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="666fd-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="666fd-133">-Offerta</span><span class="sxs-lookup"><span data-stu-id="666fd-133">-Offer</span></span>
<span data-ttu-id="666fd-134">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="666fd-134">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-135">-OsType</span><span class="sxs-lookup"><span data-stu-id="666fd-135">-OsType</span></span>
<span data-ttu-id="666fd-136">Tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="666fd-136">Operating system type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-137">-OsUri</span><span class="sxs-lookup"><span data-stu-id="666fd-137">-OsUri</span></span>
<span data-ttu-id="666fd-138">Posizione del disco.</span><span class="sxs-lookup"><span data-stu-id="666fd-138">Location of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-139">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="666fd-139">-ProvisioningState</span></span>
<span data-ttu-id="666fd-140">Stato di provisioning dell'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="666fd-140">Provisioning status of the platform image.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-141">-Publisher</span><span class="sxs-lookup"><span data-stu-id="666fd-141">-Publisher</span></span>
<span data-ttu-id="666fd-142">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="666fd-142">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="666fd-143">-Sku</span></span>
<span data-ttu-id="666fd-144">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="666fd-144">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="666fd-145">-SubscriptionId</span></span>
<span data-ttu-id="666fd-146">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="666fd-146">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="666fd-147">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="666fd-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-148">-Versione</span><span class="sxs-lookup"><span data-stu-id="666fd-148">-Version</span></span>
<span data-ttu-id="666fd-149">La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="666fd-149">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="666fd-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="666fd-150">-Confirm</span></span>
<span data-ttu-id="666fd-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="666fd-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="666fd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="666fd-152">-WhatIf</span></span>
<span data-ttu-id="666fd-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="666fd-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="666fd-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="666fd-154">The cmdlet is not run.</span></span>

### <span data-ttu-id="666fd-155">Exception. Message</span><span class="sxs-lookup"><span data-stu-id="666fd-155">Exception.Message</span></span>

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

### <span data-ttu-id="666fd-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666fd-156">CommonParameters</span></span>
<span data-ttu-id="666fd-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="666fd-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666fd-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="666fd-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666fd-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="666fd-159">INPUTS</span></span>

### <span data-ttu-id="666fd-160">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IPlatformImageParameters</span><span class="sxs-lookup"><span data-stu-id="666fd-160">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters</span></span>

### <span data-ttu-id="666fd-161">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="666fd-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="666fd-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="666fd-162">OUTPUTS</span></span>

### <span data-ttu-id="666fd-163">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="666fd-163">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="666fd-164">Note</span><span class="sxs-lookup"><span data-stu-id="666fd-164">NOTES</span></span>

<span data-ttu-id="666fd-165">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="666fd-165">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="666fd-166">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="666fd-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="666fd-167">Datadisks <IDataDisk [] >: dischi di dati usati dall'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="666fd-167">DATADISKS <IDataDisk[]>: Data disks used by the platform image.</span></span>
  - <span data-ttu-id="666fd-168">`[Lun <Int32?>]`: Numero di unità logica.</span><span class="sxs-lookup"><span data-stu-id="666fd-168">`[Lun <Int32?>]`: Logical unit number.</span></span>
  - <span data-ttu-id="666fd-169">`[Uri <String>]`: Posizione del modello di disco.</span><span class="sxs-lookup"><span data-stu-id="666fd-169">`[Uri <String>]`: Location of the disk template.</span></span>

<span data-ttu-id="666fd-170">INPUTOBJECT <IComputeAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="666fd-170">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="666fd-171">`[DiskId <String>]`: GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="666fd-171">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="666fd-172">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="666fd-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="666fd-173">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="666fd-173">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="666fd-174">`[MigrationId <String>]`: Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="666fd-174">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="666fd-175">`[Offer <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="666fd-175">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="666fd-176">`[Publisher <String>]`: Nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="666fd-176">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="666fd-177">`[QuotaName <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="666fd-177">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="666fd-178">`[Sku <String>]`: Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="666fd-178">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="666fd-179">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="666fd-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="666fd-180">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="666fd-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="666fd-181">`[Type <String>]`: Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="666fd-181">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="666fd-182">`[Version <String>]`: La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="666fd-182">`[Version <String>]`: The version of the resource.</span></span>

<span data-ttu-id="666fd-183">NEWIMAGE <IPlatformImageParameters> : parametri usati per creare una nuova immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="666fd-183">NEWIMAGE <IPlatformImageParameters>: Parameters used to create a new platform image.</span></span>
  - <span data-ttu-id="666fd-184">`[DataDisk <IDataDisk[]>]`: Dischi di dati usati dall'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="666fd-184">`[DataDisk <IDataDisk[]>]`: Data disks used by the platform image.</span></span>
    - <span data-ttu-id="666fd-185">`[Lun <Int32?>]`: Numero di unità logica.</span><span class="sxs-lookup"><span data-stu-id="666fd-185">`[Lun <Int32?>]`: Logical unit number.</span></span>
    - <span data-ttu-id="666fd-186">`[Uri <String>]`: Posizione del modello di disco.</span><span class="sxs-lookup"><span data-stu-id="666fd-186">`[Uri <String>]`: Location of the disk template.</span></span>
  - <span data-ttu-id="666fd-187">`[DetailBillingPartNumber <String>]`: Il numero di parte viene usato per fatturare i costi del software.</span><span class="sxs-lookup"><span data-stu-id="666fd-187">`[DetailBillingPartNumber <String>]`: The part number is used to bill for software costs.</span></span>
  - <span data-ttu-id="666fd-188">`[OSDiskOstype <OSType?>]`: Tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="666fd-188">`[OSDiskOstype <OSType?>]`: Operating system type.</span></span>
  - <span data-ttu-id="666fd-189">`[OSDiskUri <String>]`: Posizione del disco.</span><span class="sxs-lookup"><span data-stu-id="666fd-189">`[OSDiskUri <String>]`: Location of the disk.</span></span>
  - <span data-ttu-id="666fd-190">`[ProvisioningState <ProvisioningState?>]`: Stato di provisioning dell'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="666fd-190">`[ProvisioningState <ProvisioningState?>]`: Provisioning status of the platform image.</span></span>

## <span data-ttu-id="666fd-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="666fd-191">RELATED LINKS</span></span>

