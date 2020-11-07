---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: d91e930c486fea5c7a17e5a8f7d8f8d30a88b351
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93864030"
---
# <span data-ttu-id="dd917-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="dd917-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="dd917-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd917-102">SYNOPSIS</span></span>
<span data-ttu-id="dd917-103">Restituisce l'immagine della piattaforma specifica che corrisponde a Publisher, offer, SKU e Version.</span><span class="sxs-lookup"><span data-stu-id="dd917-103">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="dd917-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd917-104">SYNTAX</span></span>

### <span data-ttu-id="dd917-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd917-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd917-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="dd917-106">Get</span></span>
```
Get-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dd917-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dd917-107">GetViaIdentity</span></span>
```
Get-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dd917-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd917-108">DESCRIPTION</span></span>
<span data-ttu-id="dd917-109">Restituisce l'immagine della piattaforma specifica che corrisponde a Publisher, offer, SKU e Version.</span><span class="sxs-lookup"><span data-stu-id="dd917-109">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="dd917-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd917-110">EXAMPLES</span></span>

### <span data-ttu-id="dd917-111">Esempio 1: ottenere tutte le immagini della piattaforma</span><span class="sxs-lookup"><span data-stu-id="dd917-111">Example 1: Get All Platform Images</span></span>
```powershell
PS C:\> Get-AzsPlatformImage

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/loc
                    al/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=r
                    wdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="dd917-112">Ottenere un elenco di tutte le immagini della piattaforma lasciando vuoto tutti i parametri.</span><span class="sxs-lookup"><span data-stu-id="dd917-112">Get a list of all Platform Images by leaving all parameters blank.</span></span>

### <span data-ttu-id="dd917-113">Esempio 2: ottenere un'immagine della piattaforma specifica</span><span class="sxs-lookup"><span data-stu-id="dd917-113">Example 2: Get Specific Platform Image</span></span>
```powershell
PS C:\> Get-AzsPlatformImage -Offer ExampleOffer -Publisher ExamplePublisher -Location local -Sku ExampleSku -Version 1.0.0

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifa
                    ctTypes/platformImage/publishers/ExamplePublisher/offers/ExampleOffer/skus/ExampleSku/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&s
                    e=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="dd917-114">Specificare l'offerta, l'editore, la posizione, il SKU e la versione per recuperare un'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="dd917-114">Specify the Offer, Publisher, Location, Sku, and Version to retrieve a Platform Image.</span></span>

## <span data-ttu-id="dd917-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd917-115">PARAMETERS</span></span>

### <span data-ttu-id="dd917-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd917-116">-DefaultProfile</span></span>
<span data-ttu-id="dd917-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd917-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd917-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd917-118">-InputObject</span></span>
<span data-ttu-id="dd917-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="dd917-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="dd917-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="dd917-120">-Location</span></span>
<span data-ttu-id="dd917-121">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd917-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd917-122">-Offerta</span><span class="sxs-lookup"><span data-stu-id="dd917-122">-Offer</span></span>
<span data-ttu-id="dd917-123">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="dd917-123">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd917-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="dd917-124">-Publisher</span></span>
<span data-ttu-id="dd917-125">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="dd917-125">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd917-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="dd917-126">-Sku</span></span>
<span data-ttu-id="dd917-127">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="dd917-127">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd917-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd917-128">-SubscriptionId</span></span>
<span data-ttu-id="dd917-129">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dd917-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dd917-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="dd917-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd917-131">-Versione</span><span class="sxs-lookup"><span data-stu-id="dd917-131">-Version</span></span>
<span data-ttu-id="dd917-132">La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd917-132">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd917-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd917-133">CommonParameters</span></span>
<span data-ttu-id="dd917-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd917-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd917-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd917-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd917-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd917-136">INPUTS</span></span>

### <span data-ttu-id="dd917-137">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="dd917-137">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="dd917-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd917-138">OUTPUTS</span></span>

### <span data-ttu-id="dd917-139">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="dd917-139">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="dd917-140">Note</span><span class="sxs-lookup"><span data-stu-id="dd917-140">NOTES</span></span>

<span data-ttu-id="dd917-141">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="dd917-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd917-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd917-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dd917-143">INPUTOBJECT <IComputeAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="dd917-143">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd917-144">`[DiskId <String>]`: GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="dd917-144">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="dd917-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="dd917-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd917-146">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd917-146">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="dd917-147">`[MigrationId <String>]`: Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="dd917-147">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="dd917-148">`[Offer <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="dd917-148">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="dd917-149">`[Publisher <String>]`: Nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="dd917-149">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="dd917-150">`[QuotaName <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="dd917-150">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="dd917-151">`[Sku <String>]`: Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="dd917-151">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="dd917-152">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dd917-152">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dd917-153">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="dd917-153">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dd917-154">`[Type <String>]`: Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="dd917-154">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="dd917-155">`[Version <String>]`: La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd917-155">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="dd917-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd917-156">RELATED LINKS</span></span>

