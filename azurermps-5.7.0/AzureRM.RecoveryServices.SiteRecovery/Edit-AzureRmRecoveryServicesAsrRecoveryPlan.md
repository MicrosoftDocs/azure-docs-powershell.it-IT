---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 289804771010a586b73621ec5df81805ed30ae55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519390"
---
# <span data-ttu-id="e6a72-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e6a72-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="e6a72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6a72-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a72-103">Modifica un piano di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="e6a72-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6a72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6a72-104">SYNTAX</span></span>

### <span data-ttu-id="e6a72-105">AppendGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6a72-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6a72-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="e6a72-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6a72-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e6a72-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6a72-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e6a72-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6a72-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6a72-109">DESCRIPTION</span></span>
<span data-ttu-id="e6a72-110">Il cmdlet **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** modifica un piano di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a72-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="e6a72-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6a72-111">EXAMPLES</span></span>

### <span data-ttu-id="e6a72-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6a72-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="e6a72-113">Aggiunge un gruppo a un piano di ripristino del sito di Azure esistente e restituisce il piano di ripristino aggiornato in memoria.</span><span class="sxs-lookup"><span data-stu-id="e6a72-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="e6a72-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6a72-114">PARAMETERS</span></span>

### <span data-ttu-id="e6a72-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e6a72-115">-AddProtectedItem</span></span>
<span data-ttu-id="e6a72-116">Elenco di elementi protetti per la replica ASR da aggiungere al gruppo piano di ripristino nell'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e6a72-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="e6a72-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="e6a72-117">-AppendGroup</span></span>
<span data-ttu-id="e6a72-118">Parametro switch per aggiungere un gruppo piano di ripristino all'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e6a72-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="e6a72-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6a72-119">-Confirm</span></span>
<span data-ttu-id="e6a72-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6a72-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a72-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a72-121">-DefaultProfile</span></span>
<span data-ttu-id="e6a72-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a72-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a72-123">-Gruppo</span><span class="sxs-lookup"><span data-stu-id="e6a72-123">-Group</span></span>
<span data-ttu-id="e6a72-124">Specifica un gruppo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e6a72-124">Specifies a recovery plan group.</span></span>

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

### <span data-ttu-id="e6a72-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6a72-125">-InputObject</span></span>
<span data-ttu-id="e6a72-126">Oggetto piano di ripristino ASR da modificare (in operazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="e6a72-126">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="e6a72-127">Per aggiornare il piano di ripristino, eseguire Update-AzureRmASRRecoveryPlan con l'oggetto piano di ripristino modificato.</span><span class="sxs-lookup"><span data-stu-id="e6a72-127">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

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

### <span data-ttu-id="e6a72-128">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="e6a72-128">-RemoveGroup</span></span>
<span data-ttu-id="e6a72-129">Rimuove il gruppo specificato dall'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e6a72-129">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="e6a72-130">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e6a72-130">-RemoveProtectedItem</span></span>
<span data-ttu-id="e6a72-131">Elenco di elementi protetti per la replica ASR da rimuovere dal gruppo piano di ripristino nell'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e6a72-131">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="e6a72-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a72-132">-WhatIf</span></span>
<span data-ttu-id="e6a72-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6a72-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6a72-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6a72-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a72-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a72-135">CommonParameters</span></span>
<span data-ttu-id="e6a72-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a72-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a72-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a72-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a72-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6a72-138">INPUTS</span></span>

### <span data-ttu-id="e6a72-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e6a72-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="e6a72-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6a72-140">OUTPUTS</span></span>

### <span data-ttu-id="e6a72-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="e6a72-141">System.Object</span></span>

## <span data-ttu-id="e6a72-142">Note</span><span class="sxs-lookup"><span data-stu-id="e6a72-142">NOTES</span></span>

## <span data-ttu-id="e6a72-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6a72-143">RELATED LINKS</span></span>

[<span data-ttu-id="e6a72-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e6a72-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e6a72-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e6a72-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
