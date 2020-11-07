---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/edit-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: cac83004dc56b8d32acacced0339068a1fd932f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855834"
---
# <span data-ttu-id="0dbce-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0dbce-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="0dbce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0dbce-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbce-103">Modifica un piano di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="0dbce-103">Edits a Site Recovery plan.</span></span>

## <span data-ttu-id="0dbce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0dbce-104">SYNTAX</span></span>

### <span data-ttu-id="0dbce-105">AppendGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0dbce-105">AppendGroup (Default)</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dbce-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="0dbce-106">RemoveGroup</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dbce-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="0dbce-107">AddReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dbce-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="0dbce-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dbce-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0dbce-109">DESCRIPTION</span></span>
<span data-ttu-id="0dbce-110">Il cmdlet **Edit-AzRecoveryServicesAsrRecoveryPlan** modifica un piano di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="0dbce-110">The **Edit-AzRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="0dbce-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0dbce-111">EXAMPLES</span></span>

### <span data-ttu-id="0dbce-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0dbce-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="0dbce-113">Aggiunge un gruppo a un piano di ripristino del sito di Azure esistente e restituisce il piano di ripristino aggiornato in memoria.</span><span class="sxs-lookup"><span data-stu-id="0dbce-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="0dbce-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0dbce-114">PARAMETERS</span></span>

### <span data-ttu-id="0dbce-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0dbce-115">-AddProtectedItem</span></span>
<span data-ttu-id="0dbce-116">Elenco di elementi protetti per la replica ASR da aggiungere al gruppo piano di ripristino nell'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0dbce-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbce-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="0dbce-117">-AppendGroup</span></span>
<span data-ttu-id="0dbce-118">Parametro switch per aggiungere un gruppo piano di ripristino all'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0dbce-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dbce-119">-DefaultProfile</span></span>
<span data-ttu-id="0dbce-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0dbce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbce-121">-Gruppo</span><span class="sxs-lookup"><span data-stu-id="0dbce-121">-Group</span></span>
<span data-ttu-id="0dbce-122">Specifica un gruppo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0dbce-122">Specifies a recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbce-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0dbce-123">-InputObject</span></span>
<span data-ttu-id="0dbce-124">Oggetto piano di ripristino ASR da modificare (in operazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="0dbce-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="0dbce-125">Per aggiornare il piano di ripristino, eseguire Update-AzASRRecoveryPlan con l'oggetto piano di ripristino modificato.</span><span class="sxs-lookup"><span data-stu-id="0dbce-125">To update the recovery plan run Update-AzASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dbce-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="0dbce-126">-RemoveGroup</span></span>
<span data-ttu-id="0dbce-127">Rimuove il gruppo specificato dall'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0dbce-127">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbce-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0dbce-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="0dbce-129">Elenco di elementi protetti per la replica ASR da rimuovere dal gruppo piano di ripristino nell'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0dbce-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbce-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0dbce-130">-Confirm</span></span>
<span data-ttu-id="0dbce-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dbce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dbce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dbce-132">-WhatIf</span></span>
<span data-ttu-id="0dbce-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0dbce-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0dbce-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0dbce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dbce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbce-135">CommonParameters</span></span>
<span data-ttu-id="0dbce-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dbce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dbce-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dbce-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbce-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0dbce-138">INPUTS</span></span>

### <span data-ttu-id="0dbce-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0dbce-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="0dbce-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0dbce-140">OUTPUTS</span></span>

### <span data-ttu-id="0dbce-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0dbce-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="0dbce-142">Note</span><span class="sxs-lookup"><span data-stu-id="0dbce-142">NOTES</span></span>

## <span data-ttu-id="0dbce-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0dbce-143">RELATED LINKS</span></span>

[<span data-ttu-id="0dbce-144">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0dbce-144">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="0dbce-145">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0dbce-145">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)
