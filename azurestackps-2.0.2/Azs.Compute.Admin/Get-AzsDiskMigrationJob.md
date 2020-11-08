---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: 96c14cd8d8d48b6212ed0e4c7b0d5934754912a5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030494"
---
# <span data-ttu-id="0c3e5-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0c3e5-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="0c3e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3e5-103">Restituisce il processo di migrazione disco richiesto.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-103">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="0c3e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c3e5-104">SYNTAX</span></span>

### <span data-ttu-id="0c3e5-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c3e5-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] [-SubscriptionId <String[]>] [-Status <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0c3e5-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="0c3e5-106">Get</span></span>
```
Get-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0c3e5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0c3e5-107">GetViaIdentity</span></span>
```
Get-AzsDiskMigrationJob -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0c3e5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c3e5-108">DESCRIPTION</span></span>
<span data-ttu-id="0c3e5-109">Restituisce il processo di migrazione disco richiesto.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-109">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="0c3e5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c3e5-110">EXAMPLES</span></span>

### <span data-ttu-id="0c3e5-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="0c3e5-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob
```

<span data-ttu-id="0c3e5-112">Restituisce un elenco dei processi di migrazione del disco gestito nella posizione locale.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-112">Returns a list of managed disk migration jobs at the location local.</span></span>

### <span data-ttu-id="0c3e5-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="0c3e5-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob -Name TestNewDiskMigrationJob

CreationTime : 2/26/2020 10:45:41 AM
EndTime      : 2/26/2020 10:46:32 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestNewDiskMigrationJob
Location     : redmond
MigrationId  : TestNewDiskMigrationJob
Name         : redmond/TestNewDiskMigrationJob
StartTime    : 2/26/2020 10:45:41 AM
Status       : Succeeded
Subtask      : {edacd0f6-760a-43f9-a188-8833751f89ce, f1ee38a4-5c27-4728-a12b-36976c565042}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_1
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="0c3e5-114">Ottenere un processo di migrazione del disco gestito specifico.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-114">Get a specific managed disk migration job.</span></span>

## <span data-ttu-id="0c3e5-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c3e5-115">PARAMETERS</span></span>

### <span data-ttu-id="0c3e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3e5-116">-DefaultProfile</span></span>
<span data-ttu-id="0c3e5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c3e5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c3e5-118">-InputObject</span></span>
<span data-ttu-id="0c3e5-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0c3e5-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0c3e5-120">-Location</span></span>
<span data-ttu-id="0c3e5-121">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-121">Location of the resource.</span></span>

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

### <span data-ttu-id="0c3e5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c3e5-122">-Name</span></span>
<span data-ttu-id="0c3e5-123">Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-123">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0c3e5-124">-Stato</span><span class="sxs-lookup"><span data-stu-id="0c3e5-124">-Status</span></span>
<span data-ttu-id="0c3e5-125">Parametri dello stato del processo di migrazione del disco.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-125">The parameters of disk migration job status.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0c3e5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c3e5-126">-SubscriptionId</span></span>
<span data-ttu-id="0c3e5-127">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-127">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0c3e5-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0c3e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3e5-129">CommonParameters</span></span>
<span data-ttu-id="0c3e5-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3e5-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c3e5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3e5-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c3e5-132">INPUTS</span></span>

### <span data-ttu-id="0c3e5-133">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0c3e5-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="0c3e5-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c3e5-134">OUTPUTS</span></span>

### <span data-ttu-id="0c3e5-135">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0c3e5-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="0c3e5-136">Note</span><span class="sxs-lookup"><span data-stu-id="0c3e5-136">NOTES</span></span>

<span data-ttu-id="0c3e5-137">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0c3e5-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0c3e5-139">INPUTOBJECT <IComputeAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="0c3e5-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0c3e5-140">`[DiskId <String>]`: GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="0c3e5-141">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="0c3e5-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0c3e5-142">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="0c3e5-143">`[MigrationId <String>]`: Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="0c3e5-144">`[Offer <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="0c3e5-145">`[Publisher <String>]`: Nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="0c3e5-146">`[QuotaName <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="0c3e5-147">`[Sku <String>]`: Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="0c3e5-148">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0c3e5-149">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0c3e5-150">`[Type <String>]`: Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="0c3e5-151">`[Version <String>]`: La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c3e5-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="0c3e5-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c3e5-152">RELATED LINKS</span></span>

