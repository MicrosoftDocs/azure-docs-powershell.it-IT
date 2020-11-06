---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 68e06f8a4d9c88b57fa88ee8044ca2e5d04d9ce9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520772"
---
# <span data-ttu-id="e3d1d-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e3d1d-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="e3d1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d1d-103">Modifica un piano di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3d1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3d1d-104">SYNTAX</span></span>

### <span data-ttu-id="e3d1d-105">AppendGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3d1d-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3d1d-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="e3d1d-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3d1d-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e3d1d-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3d1d-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e3d1d-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3d1d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3d1d-109">DESCRIPTION</span></span>
<span data-ttu-id="e3d1d-110">Il cmdlet **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** modifica un piano di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="e3d1d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3d1d-111">EXAMPLES</span></span>

### <span data-ttu-id="e3d1d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3d1d-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="e3d1d-113">Aggiunge un gruppo a un piano di ripristino del sito di Azure esistente e restituisce il piano di ripristino aggiornato in memoria.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="e3d1d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3d1d-114">PARAMETERS</span></span>

### <span data-ttu-id="e3d1d-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e3d1d-115">-AddProtectedItem</span></span>
<span data-ttu-id="e3d1d-116">Elenco di elementi protetti per la replica ASR da aggiungere al gruppo piano di ripristino nell'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d1d-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="e3d1d-117">-AppendGroup</span></span>
<span data-ttu-id="e3d1d-118">Parametro switch per aggiungere un gruppo piano di ripristino all'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d1d-119">-Gruppo</span><span class="sxs-lookup"><span data-stu-id="e3d1d-119">-Group</span></span>
<span data-ttu-id="e3d1d-120">Specifica un gruppo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-120">Specifies a recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d1d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3d1d-121">-InputObject</span></span>
<span data-ttu-id="e3d1d-122">Oggetto piano di ripristino ASR da modificare (in operazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-122">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="e3d1d-123">Per aggiornare il piano di ripristino, eseguire Update-AzureRmASRRecoveryPlan con l'oggetto piano di ripristino modificato.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-123">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3d1d-124">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="e3d1d-124">-RemoveGroup</span></span>
<span data-ttu-id="e3d1d-125">Rimuove il gruppo specificato dall'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-125">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d1d-126">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e3d1d-126">-RemoveProtectedItem</span></span>
<span data-ttu-id="e3d1d-127">Elenco di elementi protetti per la replica ASR da rimuovere dal gruppo piano di ripristino nell'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-127">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d1d-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3d1d-128">-Confirm</span></span>
<span data-ttu-id="e3d1d-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d1d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d1d-130">-WhatIf</span></span>
<span data-ttu-id="e3d1d-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3d1d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d1d-133">CommonParameters</span></span>
<span data-ttu-id="e3d1d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d1d-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3d1d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d1d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3d1d-136">INPUTS</span></span>

### <span data-ttu-id="e3d1d-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e3d1d-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="e3d1d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3d1d-138">OUTPUTS</span></span>

### <span data-ttu-id="e3d1d-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="e3d1d-139">System.Object</span></span>

## <span data-ttu-id="e3d1d-140">Note</span><span class="sxs-lookup"><span data-stu-id="e3d1d-140">NOTES</span></span>

## <span data-ttu-id="e3d1d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3d1d-141">RELATED LINKS</span></span>

[<span data-ttu-id="e3d1d-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e3d1d-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e3d1d-143">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e3d1d-143">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
