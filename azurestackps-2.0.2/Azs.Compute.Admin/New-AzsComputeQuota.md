---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030191"
---
# <span data-ttu-id="fec12-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="fec12-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="fec12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fec12-102">SYNOPSIS</span></span>
<span data-ttu-id="fec12-103">Crea o aggiorna una quota di calcolo con i parametri di quota forniti.</span><span class="sxs-lookup"><span data-stu-id="fec12-103">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="fec12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fec12-104">SYNTAX</span></span>

### <span data-ttu-id="fec12-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fec12-105">CreateExpanded (Default)</span></span>
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fec12-106">Creare</span><span class="sxs-lookup"><span data-stu-id="fec12-106">Create</span></span>
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fec12-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fec12-107">DESCRIPTION</span></span>
<span data-ttu-id="fec12-108">Crea o aggiorna una quota di calcolo con i parametri di quota forniti.</span><span class="sxs-lookup"><span data-stu-id="fec12-108">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="fec12-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fec12-109">EXAMPLES</span></span>

### <span data-ttu-id="fec12-110">Esempio 1: creare una quota di calcolo con parametri predefiniti</span><span class="sxs-lookup"><span data-stu-id="fec12-110">Example 1: Create a Compute Quota with Default Parameters</span></span>
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

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

<span data-ttu-id="fec12-111">Tutti i parametri non specificati verranno impostati sul parametro predefinito, mostrato sopra.</span><span class="sxs-lookup"><span data-stu-id="fec12-111">Any parameters that are not specified will be set to their default parameter, shown above.</span></span>

### <span data-ttu-id="fec12-112">Esempio 2: creare una quota di calcolo con parametri personalizzati</span><span class="sxs-lookup"><span data-stu-id="fec12-112">Example 2: Create a Compute Quota with Custom Parameters</span></span>
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

<span data-ttu-id="fec12-113">Personalizzare la quota con parametri.</span><span class="sxs-lookup"><span data-stu-id="fec12-113">Customize Quota with parameters.</span></span> <span data-ttu-id="fec12-114">Tutti i parametri non specificati avranno un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="fec12-114">Any parameters not specified will have default value.</span></span>

## <span data-ttu-id="fec12-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fec12-115">PARAMETERS</span></span>

### <span data-ttu-id="fec12-116">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="fec12-116">-AvailabilitySetCount</span></span>
<span data-ttu-id="fec12-117">Numero massimo di set di disponibilità consentiti.</span><span class="sxs-lookup"><span data-stu-id="fec12-117">Maximum number of availability sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fec12-118">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="fec12-118">-CoresCount</span></span>
<span data-ttu-id="fec12-119">Numero massimo di core consentiti.</span><span class="sxs-lookup"><span data-stu-id="fec12-119">Maximum number of cores allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fec12-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec12-120">-DefaultProfile</span></span>
<span data-ttu-id="fec12-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fec12-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fec12-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fec12-122">-Location</span></span>
<span data-ttu-id="fec12-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fec12-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fec12-124">-Location1</span><span class="sxs-lookup"><span data-stu-id="fec12-124">-Location1</span></span>
<span data-ttu-id="fec12-125">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fec12-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fec12-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="fec12-126">-Name</span></span>
<span data-ttu-id="fec12-127">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="fec12-127">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fec12-128">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="fec12-128">-NewQuota</span></span>
<span data-ttu-id="fec12-129">Contiene le informazioni sulle quote di calcolo usate per controllare l'allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fec12-129">Holds Compute quota information used to control resource allocation.</span></span>
<span data-ttu-id="fec12-130">Per costruire, vedere la sezione Note per le proprietà di NEWQUOTA e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fec12-130">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fec12-131">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="fec12-131">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="fec12-132">Numero massimo di dischi gestiti ed istantanee di tipo Premium consentiti.</span><span class="sxs-lookup"><span data-stu-id="fec12-132">Maximum number of managed disks and snapshots of type premium allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fec12-133">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="fec12-133">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="fec12-134">Numero massimo di dischi gestiti ed istantanee di tipo standard consentiti.</span><span class="sxs-lookup"><span data-stu-id="fec12-134">Maximum number of managed disks and snapshots of type standard allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fec12-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fec12-135">-SubscriptionId</span></span>
<span data-ttu-id="fec12-136">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fec12-136">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fec12-137">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="fec12-137">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fec12-138">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="fec12-138">-VirtualMachineCount</span></span>
<span data-ttu-id="fec12-139">Numero massimo di macchine virtuali consentite.</span><span class="sxs-lookup"><span data-stu-id="fec12-139">Maximum number of virtual machines allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fec12-140">-VMScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="fec12-140">-VMScaleSetCount</span></span>
<span data-ttu-id="fec12-141">Numero massimo di set di scala consentiti.</span><span class="sxs-lookup"><span data-stu-id="fec12-141">Maximum number of scale sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fec12-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fec12-142">-Confirm</span></span>
<span data-ttu-id="fec12-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fec12-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fec12-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fec12-144">-WhatIf</span></span>
<span data-ttu-id="fec12-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fec12-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fec12-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fec12-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fec12-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec12-147">CommonParameters</span></span>
<span data-ttu-id="fec12-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec12-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec12-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fec12-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec12-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fec12-150">INPUTS</span></span>

### <span data-ttu-id="fec12-151">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="fec12-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="fec12-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fec12-152">OUTPUTS</span></span>

### <span data-ttu-id="fec12-153">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="fec12-153">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="fec12-154">Note</span><span class="sxs-lookup"><span data-stu-id="fec12-154">NOTES</span></span>

<span data-ttu-id="fec12-155">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="fec12-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fec12-156">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fec12-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fec12-157">NEWQUOTA <IQuota> : contiene le informazioni sulle quote di calcolo usate per controllare l'allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fec12-157">NEWQUOTA <IQuota>: Holds Compute quota information used to control resource allocation.</span></span>
  - <span data-ttu-id="fec12-158">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fec12-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="fec12-159">`[AvailabilitySetCount <Int32?>]`: Numero massimo di set di disponibilità consentiti.</span><span class="sxs-lookup"><span data-stu-id="fec12-159">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="fec12-160">`[CoresLimit <Int32?>]`: Numero massimo di core consentiti.</span><span class="sxs-lookup"><span data-stu-id="fec12-160">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="fec12-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Numero massimo di dischi gestiti ed istantanee di tipo Premium consentiti.</span><span class="sxs-lookup"><span data-stu-id="fec12-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="fec12-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Numero massimo di dischi gestiti ed istantanee di tipo standard consentiti.</span><span class="sxs-lookup"><span data-stu-id="fec12-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="fec12-163">`[VMScaleSetCount <Int32?>]`: Numero massimo di set di proporzioni consentiti.</span><span class="sxs-lookup"><span data-stu-id="fec12-163">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="fec12-164">`[VirtualMachineCount <Int32?>]`: Numero massimo di macchine virtuali consentite.</span><span class="sxs-lookup"><span data-stu-id="fec12-164">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="fec12-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fec12-165">RELATED LINKS</span></span>

