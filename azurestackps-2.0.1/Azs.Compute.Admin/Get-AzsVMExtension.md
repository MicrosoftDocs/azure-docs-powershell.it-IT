---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsvmextension
schema: 2.0.0
ms.openlocfilehash: c2214f01b35e68ba22f9dbfc6fe9e602badb9ba9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023330"
---
# <span data-ttu-id="de37a-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="de37a-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="de37a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de37a-102">SYNOPSIS</span></span>
<span data-ttu-id="de37a-103">Restituisce l'immagine dell'estensione della macchina virtuale richiesta che corrisponde a Publisher, tipo, versione.</span><span class="sxs-lookup"><span data-stu-id="de37a-103">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="de37a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de37a-104">SYNTAX</span></span>

### <span data-ttu-id="de37a-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de37a-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="de37a-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="de37a-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="de37a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="de37a-107">GetViaIdentity</span></span>
```
Get-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="de37a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de37a-108">DESCRIPTION</span></span>
<span data-ttu-id="de37a-109">Restituisce l'immagine dell'estensione della macchina virtuale richiesta che corrisponde a Publisher, tipo, versione.</span><span class="sxs-lookup"><span data-stu-id="de37a-109">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="de37a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de37a-110">EXAMPLES</span></span>

### <span data-ttu-id="de37a-111">Esempio 1: ottenere tutte le estensioni della VM</span><span class="sxs-lookup"><span data-stu-id="de37a-111">Example 1:  Get All VM Extensions</span></span>
```powershell
PS C:\> Get-AzsVMExtension

ExtensionType            : IaaSDiagnostics
TypeHandlerVersion       : 1.11.3.12
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/northwest/artifactTypes/VMExtension/publishers/Microsoft.Azure.Diagnostics/types/IaaSDia
                           gnostics/versions/1.11.3.12
IsSystemExtension        : False
Location                 : northwest
Name                     :
ProvisioningState        : Succeeded
Publisher                : Microsoft.Azure.Diagnostics
SourceBlobUri            :
SupportMultipleExtension : False
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Windows

...
```

<span data-ttu-id="de37a-112">Ottenere un elenco di tutti i VMExtensions lasciando vuoto tutti i parametri.</span><span class="sxs-lookup"><span data-stu-id="de37a-112">Get a list of all VMExtensions by leaving all parameters blank.</span></span>

## <span data-ttu-id="de37a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de37a-113">PARAMETERS</span></span>

### <span data-ttu-id="de37a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de37a-114">-DefaultProfile</span></span>
<span data-ttu-id="de37a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de37a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de37a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de37a-116">-InputObject</span></span>
<span data-ttu-id="de37a-117">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="de37a-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="de37a-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="de37a-118">-Location</span></span>
<span data-ttu-id="de37a-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="de37a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="de37a-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="de37a-120">-Publisher</span></span>
<span data-ttu-id="de37a-121">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="de37a-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="de37a-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de37a-122">-SubscriptionId</span></span>
<span data-ttu-id="de37a-123">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="de37a-123">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="de37a-124">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="de37a-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="de37a-125">-Digitare</span><span class="sxs-lookup"><span data-stu-id="de37a-125">-Type</span></span>
<span data-ttu-id="de37a-126">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="de37a-126">Type of extension.</span></span>

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

### <span data-ttu-id="de37a-127">-Versione</span><span class="sxs-lookup"><span data-stu-id="de37a-127">-Version</span></span>
<span data-ttu-id="de37a-128">La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="de37a-128">The version of the resource.</span></span>

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

### <span data-ttu-id="de37a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de37a-129">CommonParameters</span></span>
<span data-ttu-id="de37a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de37a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de37a-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de37a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de37a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de37a-132">INPUTS</span></span>

### <span data-ttu-id="de37a-133">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="de37a-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="de37a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de37a-134">OUTPUTS</span></span>

### <span data-ttu-id="de37a-135">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="de37a-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="de37a-136">Note</span><span class="sxs-lookup"><span data-stu-id="de37a-136">NOTES</span></span>

<span data-ttu-id="de37a-137">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="de37a-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="de37a-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="de37a-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="de37a-139">INPUTOBJECT <IComputeAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="de37a-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="de37a-140">`[DiskId <String>]`: GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="de37a-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="de37a-141">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="de37a-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="de37a-142">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="de37a-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="de37a-143">`[MigrationId <String>]`: Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="de37a-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="de37a-144">`[Offer <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="de37a-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="de37a-145">`[Publisher <String>]`: Nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="de37a-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="de37a-146">`[QuotaName <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="de37a-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="de37a-147">`[Sku <String>]`: Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="de37a-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="de37a-148">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="de37a-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="de37a-149">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="de37a-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="de37a-150">`[Type <String>]`: Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="de37a-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="de37a-151">`[Version <String>]`: La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="de37a-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="de37a-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de37a-152">RELATED LINKS</span></span>

