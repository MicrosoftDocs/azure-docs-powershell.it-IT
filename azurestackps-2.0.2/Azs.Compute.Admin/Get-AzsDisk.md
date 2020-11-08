---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030537"
---
# <span data-ttu-id="24cf0-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="24cf0-101">Get-AzsDisk</span></span>

## <span data-ttu-id="24cf0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24cf0-102">SYNOPSIS</span></span>
<span data-ttu-id="24cf0-103">Restituisce il disco.</span><span class="sxs-lookup"><span data-stu-id="24cf0-103">Returns the disk.</span></span>

## <span data-ttu-id="24cf0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24cf0-104">SYNTAX</span></span>

### <span data-ttu-id="24cf0-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24cf0-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="24cf0-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="24cf0-106">Get</span></span>
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="24cf0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="24cf0-107">GetViaIdentity</span></span>
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="24cf0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24cf0-108">DESCRIPTION</span></span>
<span data-ttu-id="24cf0-109">Restituisce il disco.</span><span class="sxs-lookup"><span data-stu-id="24cf0-109">Returns the disk.</span></span>

## <span data-ttu-id="24cf0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24cf0-110">EXAMPLES</span></span>

### <span data-ttu-id="24cf0-111">Esempio 1: ottenere tutti i dischi</span><span class="sxs-lookup"><span data-stu-id="24cf0-111">Example 1: Get All Disks</span></span> 
```powershell
PS C:\> Get-AzsDisk
```

<span data-ttu-id="24cf0-112">Senza parametri, `Get-AzsDisk` verranno elencati tutti i dischi.</span><span class="sxs-lookup"><span data-stu-id="24cf0-112">Without any parameters, `Get-AzsDisk` will list all Disks.</span></span>

### <span data-ttu-id="24cf0-113">Esempio 2: ottenere un disco per nome</span><span class="sxs-lookup"><span data-stu-id="24cf0-113">Example 2: Get a Disk by Name</span></span>
```powershell
PS C:\> Get-AzsDisk -Name "426b8945-8a24-42ad-acdc-c26f16202489"

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="24cf0-114">Specifica un disco per il suo `Name` recupero.</span><span class="sxs-lookup"><span data-stu-id="24cf0-114">Specify a disk by its `Name` to retrieve it.</span></span>

### <span data-ttu-id="24cf0-115">Esempio 3: ottenere un numero specificato di dischi</span><span class="sxs-lookup"><span data-stu-id="24cf0-115">Example 3: Get a Specified number of Disks</span></span>
```powershell
PS C:\>  Get-AzsDisk -Count 3

ActualSizeGb    : 24
DiskId          : 20f1619e-4210-47f6-81e6-b89e3028df06
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/20f1619e-4210-47f6-81e6-b89e3028df06
Location        : northwest
ManagedBy       :
Name            : northwest/20f1619e-4210-47f6-81e6-b89e3028df06
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/RG1/providers/Microsoft.Compute/Di
                  sks/TEST_OsDisk_1_20f1619e421047f681e6b89e3028df06

ActualSizeGb    : 24
DiskId          : 38a767e4-4ceb-49fb-a53c-48de9b08aaae
DiskSku         : Standard_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/38a767e4-4ceb-49fb-a53c-48de9b08aaae
Location        : northwest
ManagedBy       :
Name            : northwest/38a767e4-4ceb-49fb-a53c-48de9b08aaae
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/SCTE/providers/Microsoft.Compute/D
                  isks/SCTETest_OsDisk_1_38a767e44ceb49fba53c48de9b08aaae

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="24cf0-116">Usa il `Count` parametro per recuperare un numero specifico di dischi.</span><span class="sxs-lookup"><span data-stu-id="24cf0-116">Use the `Count` parameter to retrieve a specific number of disks.</span></span>

### <span data-ttu-id="24cf0-117">Esempio 4: ottenere tutti i dischi in una posizione specifica</span><span class="sxs-lookup"><span data-stu-id="24cf0-117">Example 4: Get all disks in specific location</span></span>
```powershell
PS C:\> Get-AzsDisk -Status All -ScaleUnit s-cluster -VolumeLabel Objstore_4

ActualSizeGb    : 2
DiskId          : e4732f76-0753-40ec-80f5-8effdd0b437d
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/e4732f76-0753-40ec-80f5-8effdd0b437d
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/e4732f76-0753-40ec-80f5-8effdd0b437d
ProvisionSizeGb : 30
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/test1_OsDisk_1_e4732f76075340ec80f58effdd0b437d

ActualSizeGb    : 1
DiskId          : 0485cbc9-1efa-43bd-86c2-0e201d79c528
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/0485cbc9-1efa-43bd-86c2-0e201d79c528
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/0485cbc9-1efa-43bd-86c2-0e201d79c528
ProvisionSizeGb : 64
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/TESTRG1/providers/Microsoft.Compute/Disks/gpsdisk

ActualSizeGb    : 1
DiskId          : 137893db-e7ce-4907-a488-b35c5e928614
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/137893db-e7ce-4907-a488-b35c5e928614
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/137893db-e7ce-4907-a488-b35c5e928614
ProvisionSizeGb : 55
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/testdd
```

<span data-ttu-id="24cf0-118">Usare il `ScaleUnit` `VolumeLabel` parametro or per elencare tutti i dischi in una posizione specifica</span><span class="sxs-lookup"><span data-stu-id="24cf0-118">Use the `ScaleUnit` or `VolumeLabel` parameter to list all disks in specific location</span></span>

## <span data-ttu-id="24cf0-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24cf0-119">PARAMETERS</span></span>

### <span data-ttu-id="24cf0-120">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="24cf0-120">-Count</span></span>
<span data-ttu-id="24cf0-121">Numero massimo di dischi da restituire.</span><span class="sxs-lookup"><span data-stu-id="24cf0-121">The maximum number of disks to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24cf0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cf0-122">-DefaultProfile</span></span>
<span data-ttu-id="24cf0-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24cf0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24cf0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24cf0-124">-InputObject</span></span>
<span data-ttu-id="24cf0-125">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="24cf0-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="24cf0-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="24cf0-126">-Location</span></span>
<span data-ttu-id="24cf0-127">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="24cf0-127">Location of the resource.</span></span>

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

### <span data-ttu-id="24cf0-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="24cf0-128">-Name</span></span>
<span data-ttu-id="24cf0-129">GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="24cf0-129">The disk guid as identity.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24cf0-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="24cf0-130">-ScaleUnit</span></span>
<span data-ttu-id="24cf0-131">Unità di scala a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="24cf0-131">The scale unit which the resource belongs to.</span></span>

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

### <span data-ttu-id="24cf0-132">-SharePath</span><span class="sxs-lookup"><span data-stu-id="24cf0-132">-SharePath</span></span>
<span data-ttu-id="24cf0-133">La condivisione a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="24cf0-133">The share which the resource belongs to.</span></span>

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

### <span data-ttu-id="24cf0-134">-Inizio</span><span class="sxs-lookup"><span data-stu-id="24cf0-134">-Start</span></span>
<span data-ttu-id="24cf0-135">Indice Start dei dischi in query.</span><span class="sxs-lookup"><span data-stu-id="24cf0-135">The start index of disks in query.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24cf0-136">-Stato</span><span class="sxs-lookup"><span data-stu-id="24cf0-136">-Status</span></span>
<span data-ttu-id="24cf0-137">I parametri dello stato del disco.</span><span class="sxs-lookup"><span data-stu-id="24cf0-137">The parameters of disk state.</span></span>

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

### <span data-ttu-id="24cf0-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24cf0-138">-SubscriptionId</span></span>
<span data-ttu-id="24cf0-139">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="24cf0-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="24cf0-140">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="24cf0-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="24cf0-141">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24cf0-141">-UserSubscriptionId</span></span>
<span data-ttu-id="24cf0-142">ID abbonamento utente a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="24cf0-142">User Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="24cf0-143">-VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="24cf0-143">-VolumeLabel</span></span>
<span data-ttu-id="24cf0-144">Etichetta di volume del volume a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="24cf0-144">The volume label of the volume which the resource belongs to.</span></span>

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

### <span data-ttu-id="24cf0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cf0-145">CommonParameters</span></span>
<span data-ttu-id="24cf0-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24cf0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cf0-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24cf0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cf0-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24cf0-148">INPUTS</span></span>

### <span data-ttu-id="24cf0-149">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="24cf0-149">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="24cf0-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24cf0-150">OUTPUTS</span></span>

### <span data-ttu-id="24cf0-151">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180730Preview. IDisk</span><span class="sxs-lookup"><span data-stu-id="24cf0-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk</span></span>



## <span data-ttu-id="24cf0-152">Note</span><span class="sxs-lookup"><span data-stu-id="24cf0-152">NOTES</span></span>

<span data-ttu-id="24cf0-153">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="24cf0-153">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24cf0-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="24cf0-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="24cf0-155">INPUTOBJECT <IComputeAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="24cf0-155">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="24cf0-156">`[DiskId <String>]`: GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="24cf0-156">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="24cf0-157">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="24cf0-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="24cf0-158">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="24cf0-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="24cf0-159">`[MigrationId <String>]`: Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="24cf0-159">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="24cf0-160">`[Offer <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="24cf0-160">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="24cf0-161">`[Publisher <String>]`: Nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="24cf0-161">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="24cf0-162">`[QuotaName <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="24cf0-162">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="24cf0-163">`[Sku <String>]`: Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="24cf0-163">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="24cf0-164">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="24cf0-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="24cf0-165">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="24cf0-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="24cf0-166">`[Type <String>]`: Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="24cf0-166">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="24cf0-167">`[Version <String>]`: La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="24cf0-167">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="24cf0-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24cf0-168">RELATED LINKS</span></span>

