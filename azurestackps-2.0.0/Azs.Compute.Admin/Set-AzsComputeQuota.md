---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93864002"
---
# <span data-ttu-id="ab8a1-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="ab8a1-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="ab8a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab8a1-102">SYNOPSIS</span></span>


## <span data-ttu-id="ab8a1-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab8a1-103">SYNTAX</span></span>

### <span data-ttu-id="ab8a1-104">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab8a1-104">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ab8a1-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab8a1-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ab8a1-106">UpdateExpanded</span><span class="sxs-lookup"><span data-stu-id="ab8a1-106">UpdateExpanded</span></span>
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## <span data-ttu-id="ab8a1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab8a1-107">DESCRIPTION</span></span>
<span data-ttu-id="ab8a1-108">Aggiornare una quota di calcolo</span><span class="sxs-lookup"><span data-stu-id="ab8a1-108">Update a Compute Quota</span></span>

## <span data-ttu-id="ab8a1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab8a1-109">EXAMPLES</span></span>

### <span data-ttu-id="ab8a1-110">Esempio 1: impostare le proprietà in una quota di calcolo esistente</span><span class="sxs-lookup"><span data-stu-id="ab8a1-110">Example 1: Set Properties on an Existing Compute Quota</span></span>
```powershell
PS C:\> $myComputeQuota = Get-AzsComputeQuota -Name MyComputeQuota

PS C:\> $myComputeQuota.CoresLimit = 99; 

PS C:\> Set-AzsComputeQuota -NewQuota $myComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 99
Id                                 : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/northwest/quotas/MyComputeQuota
Location                           : northwest
Name                               : MyComputeQuota
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="ab8a1-111">Impostare i parametri specificati nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-111">Set the parameters specified on the command line.</span></span>
<span data-ttu-id="ab8a1-112">Tutti i parametri non impostati saranno predefiniti per 0</span><span class="sxs-lookup"><span data-stu-id="ab8a1-112">Any parameters not set will default to 0</span></span>

## <span data-ttu-id="ab8a1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab8a1-113">PARAMETERS</span></span>

### <span data-ttu-id="ab8a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8a1-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="ab8a1-115">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="ab8a1-115">-NewQuota</span></span>
<span data-ttu-id="ab8a1-116">Per costruire, vedere la sezione Note per le proprietà di NEWQUOTA e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-116">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ab8a1-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab8a1-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="ab8a1-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab8a1-118">-Confirm</span></span>
<span data-ttu-id="ab8a1-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab8a1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab8a1-120">-WhatIf</span></span>
<span data-ttu-id="ab8a1-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab8a1-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab8a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8a1-123">CommonParameters</span></span>
<span data-ttu-id="ab8a1-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8a1-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab8a1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8a1-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab8a1-126">INPUTS</span></span>

### <span data-ttu-id="ab8a1-127">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="ab8a1-127">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="ab8a1-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab8a1-128">OUTPUTS</span></span>

### <span data-ttu-id="ab8a1-129">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="ab8a1-129">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="ab8a1-130">Note</span><span class="sxs-lookup"><span data-stu-id="ab8a1-130">NOTES</span></span>

<span data-ttu-id="ab8a1-131">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab8a1-132">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ab8a1-133">NEWQUOTA <IQuota> :</span><span class="sxs-lookup"><span data-stu-id="ab8a1-133">NEWQUOTA <IQuota>:</span></span> 
  - <span data-ttu-id="ab8a1-134">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-134">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="ab8a1-135">`[AvailabilitySetCount <Int32?>]`: Numero massimo di set di disponibilità consentiti.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-135">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="ab8a1-136">`[CoresLimit <Int32?>]`: Numero massimo di core consentiti.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-136">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="ab8a1-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Numero massimo di dischi gestiti ed istantanee di tipo Premium consentiti.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="ab8a1-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Numero massimo di dischi gestiti ed istantanee di tipo standard consentiti.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="ab8a1-139">`[VMScaleSetCount <Int32?>]`: Numero massimo di set di proporzioni consentiti.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-139">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="ab8a1-140">`[VirtualMachineCount <Int32?>]`: Numero massimo di macchine virtuali consentite.</span><span class="sxs-lookup"><span data-stu-id="ab8a1-140">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="ab8a1-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab8a1-141">RELATED LINKS</span></span>

