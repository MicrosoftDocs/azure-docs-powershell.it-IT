---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: c3fd190fb033a685bcb0d5087c544298681e47c5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023328"
---
# <span data-ttu-id="cc0e6-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="cc0e6-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="cc0e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cc0e6-102">SYNOPSIS</span></span>


## <span data-ttu-id="cc0e6-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc0e6-103">SYNTAX</span></span>

### <span data-ttu-id="cc0e6-104">Volume (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cc0e6-104">Volume (Default)</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetScaleUnit <String> -TargetVolumeLabel <String> -Disks <IDisk[]>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cc0e6-105">Condividi</span><span class="sxs-lookup"><span data-stu-id="cc0e6-105">Share</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetShare <String> -Disks <IDisk[]> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc0e6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc0e6-106">DESCRIPTION</span></span>


## <span data-ttu-id="cc0e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc0e6-107">EXAMPLES</span></span>

### <span data-ttu-id="cc0e6-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="cc0e6-108">Example 1:</span></span>
```powershell
PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

CreationTime : 2/26/2020 10:56:32 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestJob1
Location     : redmond
MigrationId  : TestJob1
Name         : redmond/TestJob1
StartTime    : 
Status       : Pending
Subtask      : {53ee3665-00e4-4c69-a067-524058905ead, d551734f-0370-4851-9704-c7cec80b34c5}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_2
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="cc0e6-109">Creare un processo di migrazione disco per eseguire la migrazione dei dischi all'unità e al volume della scala di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-109">Create a disk migration job to migrate disks to the target scale unit and volume.</span></span>

### <span data-ttu-id="cc0e6-110">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="cc0e6-110">Example 2:</span></span> 
```powershell
PS C:\> PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob2 -TargetShare \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3 -Disks $disks
WARNING: TargetShare parameter will be deprecated in a future release, please use Volume instead.

CreationTime : 2/26/2020 11:02:48 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob2
Location     : redmond
MigrationId  : TestJob2
Name         : redmond/TestJob2
StartTime    : 
Status       : Pending
Subtask      : {0cfd8d29-1ca4-42db-a490-9198814abc50, 89c9b15e-47c6-4321-a390-611fc190cfad}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

```

<span data-ttu-id="cc0e6-111">Creare un processo di migrazione disco per eseguire la migrazione dei dischi alla condivisione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-111">Create a disk migration job to migrate disks to the target share.</span></span>

## <span data-ttu-id="cc0e6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc0e6-112">PARAMETERS</span></span>

### <span data-ttu-id="cc0e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc0e6-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="cc0e6-114">-Dischi</span><span class="sxs-lookup"><span data-stu-id="cc0e6-114">-Disks</span></span>
<span data-ttu-id="cc0e6-115">Per costruire, vedere la sezione Note per le proprietà dei dischi e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-115">To construct, see NOTES section for DISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cc0e6-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cc0e6-116">-Location</span></span>


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

### <span data-ttu-id="cc0e6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc0e6-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc0e6-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc0e6-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="cc0e6-119">-TargetScaleUnit</span><span class="sxs-lookup"><span data-stu-id="cc0e6-119">-TargetScaleUnit</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc0e6-120">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="cc0e6-120">-TargetShare</span></span>


```yaml
Type: System.String
Parameter Sets: Share
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc0e6-121">-TargetVolumeLabel</span><span class="sxs-lookup"><span data-stu-id="cc0e6-121">-TargetVolumeLabel</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc0e6-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cc0e6-122">-Confirm</span></span>
<span data-ttu-id="cc0e6-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc0e6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc0e6-124">-WhatIf</span></span>
<span data-ttu-id="cc0e6-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc0e6-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc0e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc0e6-127">CommonParameters</span></span>
<span data-ttu-id="cc0e6-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc0e6-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc0e6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc0e6-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cc0e6-130">INPUTS</span></span>

### <span data-ttu-id="cc0e6-131">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180730Preview. IDisk []</span><span class="sxs-lookup"><span data-stu-id="cc0e6-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]</span></span>

## <span data-ttu-id="cc0e6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc0e6-132">OUTPUTS</span></span>

### <span data-ttu-id="cc0e6-133">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="cc0e6-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



### <span data-ttu-id="cc0e6-134">Start-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="cc0e6-134">Start-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="cc0e6-135">Note</span><span class="sxs-lookup"><span data-stu-id="cc0e6-135">NOTES</span></span>

<span data-ttu-id="cc0e6-136">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc0e6-137">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cc0e6-138">DISCHI <IDisk [] >:</span><span class="sxs-lookup"><span data-stu-id="cc0e6-138">DISKS <IDisk[]>:</span></span> 
  - <span data-ttu-id="cc0e6-139">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-139">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cc0e6-140">`[DiskId <String>]`: ID disco.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-140">`[DiskId <String>]`: The disk id.</span></span>
  - <span data-ttu-id="cc0e6-141">`[SharePath <String>]`: Percorso condivisione disco.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-141">`[SharePath <String>]`: The disk share path.</span></span>
  - <span data-ttu-id="cc0e6-142">`[Status <DiskState?>]`: Lo stato del disco.</span><span class="sxs-lookup"><span data-stu-id="cc0e6-142">`[Status <DiskState?>]`: The disk status.</span></span>

## <span data-ttu-id="cc0e6-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc0e6-143">RELATED LINKS</span></span>

