---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 81a7a64f1880e2ed9acb2fedd3f90df614f1619d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023331"
---
# <span data-ttu-id="37b7e-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="37b7e-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="37b7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="37b7e-103">Ottenere una quota di calcolo esistente.</span><span class="sxs-lookup"><span data-stu-id="37b7e-103">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="37b7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37b7e-104">SYNTAX</span></span>

### <span data-ttu-id="37b7e-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37b7e-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="37b7e-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="37b7e-106">Get</span></span>
```
Get-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="37b7e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="37b7e-107">GetViaIdentity</span></span>
```
Get-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="37b7e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37b7e-108">DESCRIPTION</span></span>
<span data-ttu-id="37b7e-109">Ottenere una quota di calcolo esistente.</span><span class="sxs-lookup"><span data-stu-id="37b7e-109">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="37b7e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37b7e-110">EXAMPLES</span></span>

### <span data-ttu-id="37b7e-111">Esempio 1: ottenere tutte le quote di calcolo</span><span class="sxs-lookup"><span data-stu-id="37b7e-111">Example 1: Get All Compute Quotas</span></span>
```powershell
PS C:\> Get-AzsComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ascancompquota433
Location                           : local
Name                               : ascancompquota433
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 100
VirtualMachineCount                : 100
```

<span data-ttu-id="37b7e-112">Esegui `Get-AzsComputeQuota` senza parametri per ottenere un elenco di tutte le quote di calcolo.</span><span class="sxs-lookup"><span data-stu-id="37b7e-112">Run `Get-AzsComputeQuota` with no parameters to get a list of all Compute Quotas.</span></span>

### <span data-ttu-id="37b7e-113">Esempio 2: ottenere la quota di calcolo per nome</span><span class="sxs-lookup"><span data-stu-id="37b7e-113">Example 2: Get Compute Quota by Name</span></span>
```powershell
PS C:\> Get-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="37b7e-114">Specificare il nome della quota nella riga di comando per recuperare una quota specifica.</span><span class="sxs-lookup"><span data-stu-id="37b7e-114">Specify the Quota's name on the command line to retrieve a specific quota.</span></span>

## <span data-ttu-id="37b7e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37b7e-115">PARAMETERS</span></span>

### <span data-ttu-id="37b7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b7e-116">-DefaultProfile</span></span>
<span data-ttu-id="37b7e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37b7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37b7e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37b7e-118">-InputObject</span></span>
<span data-ttu-id="37b7e-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="37b7e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="37b7e-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="37b7e-120">-Location</span></span>
<span data-ttu-id="37b7e-121">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="37b7e-121">Location of the resource.</span></span>

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

### <span data-ttu-id="37b7e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="37b7e-122">-Name</span></span>
<span data-ttu-id="37b7e-123">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="37b7e-123">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="37b7e-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37b7e-124">-SubscriptionId</span></span>
<span data-ttu-id="37b7e-125">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="37b7e-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="37b7e-126">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="37b7e-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="37b7e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b7e-127">CommonParameters</span></span>
<span data-ttu-id="37b7e-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b7e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b7e-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37b7e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b7e-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37b7e-130">INPUTS</span></span>

### <span data-ttu-id="37b7e-131">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="37b7e-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="37b7e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37b7e-132">OUTPUTS</span></span>

### <span data-ttu-id="37b7e-133">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="37b7e-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="37b7e-134">Note</span><span class="sxs-lookup"><span data-stu-id="37b7e-134">NOTES</span></span>

<span data-ttu-id="37b7e-135">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="37b7e-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37b7e-136">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37b7e-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="37b7e-137">INPUTOBJECT <IComputeAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="37b7e-137">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37b7e-138">`[DiskId <String>]`: GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="37b7e-138">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="37b7e-139">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="37b7e-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37b7e-140">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="37b7e-140">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="37b7e-141">`[MigrationId <String>]`: Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="37b7e-141">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="37b7e-142">`[Offer <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="37b7e-142">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="37b7e-143">`[Publisher <String>]`: Nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="37b7e-143">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="37b7e-144">`[QuotaName <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="37b7e-144">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="37b7e-145">`[Sku <String>]`: Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="37b7e-145">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="37b7e-146">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="37b7e-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="37b7e-147">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="37b7e-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="37b7e-148">`[Type <String>]`: Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="37b7e-148">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="37b7e-149">`[Version <String>]`: La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="37b7e-149">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="37b7e-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37b7e-150">RELATED LINKS</span></span>

