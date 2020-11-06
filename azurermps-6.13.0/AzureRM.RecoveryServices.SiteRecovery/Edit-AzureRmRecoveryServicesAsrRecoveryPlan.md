---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: f60da52bffcc78e563863c79971beea8d45e398e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518604"
---
# <span data-ttu-id="8adcf-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8adcf-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="8adcf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8adcf-102">SYNOPSIS</span></span>
<span data-ttu-id="8adcf-103">Modifica un piano di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="8adcf-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8adcf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8adcf-104">SYNTAX</span></span>

### <span data-ttu-id="8adcf-105">AppendGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8adcf-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8adcf-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="8adcf-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8adcf-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="8adcf-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8adcf-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="8adcf-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8adcf-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8adcf-109">DESCRIPTION</span></span>
<span data-ttu-id="8adcf-110">Il cmdlet **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** modifica un piano di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="8adcf-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="8adcf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8adcf-111">EXAMPLES</span></span>

### <span data-ttu-id="8adcf-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8adcf-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="8adcf-113">Aggiunge un gruppo a un piano di ripristino del sito di Azure esistente e restituisce il piano di ripristino aggiornato in memoria.</span><span class="sxs-lookup"><span data-stu-id="8adcf-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="8adcf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8adcf-114">PARAMETERS</span></span>

### <span data-ttu-id="8adcf-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8adcf-115">-AddProtectedItem</span></span>
<span data-ttu-id="8adcf-116">Elenco di elementi protetti per la replica ASR da aggiungere al gruppo piano di ripristino nell'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8adcf-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="8adcf-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="8adcf-117">-AppendGroup</span></span>
<span data-ttu-id="8adcf-118">Parametro switch per aggiungere un gruppo piano di ripristino all'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8adcf-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="8adcf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8adcf-119">-DefaultProfile</span></span>
<span data-ttu-id="8adcf-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8adcf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8adcf-121">-Gruppo</span><span class="sxs-lookup"><span data-stu-id="8adcf-121">-Group</span></span>
<span data-ttu-id="8adcf-122">Specifica un gruppo piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8adcf-122">Specifies a recovery plan group.</span></span>

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

### <span data-ttu-id="8adcf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8adcf-123">-InputObject</span></span>
<span data-ttu-id="8adcf-124">Oggetto piano di ripristino ASR da modificare (in operazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="8adcf-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="8adcf-125">Per aggiornare il piano di ripristino, eseguire Update-AzureRmASRRecoveryPlan con l'oggetto piano di ripristino modificato.</span><span class="sxs-lookup"><span data-stu-id="8adcf-125">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

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

### <span data-ttu-id="8adcf-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="8adcf-126">-RemoveGroup</span></span>
<span data-ttu-id="8adcf-127">Rimuove il gruppo specificato dall'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8adcf-127">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="8adcf-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8adcf-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="8adcf-129">Elenco di elementi protetti per la replica ASR da rimuovere dal gruppo piano di ripristino nell'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8adcf-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="8adcf-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8adcf-130">-Confirm</span></span>
<span data-ttu-id="8adcf-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8adcf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8adcf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8adcf-132">-WhatIf</span></span>
<span data-ttu-id="8adcf-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8adcf-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8adcf-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8adcf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8adcf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8adcf-135">CommonParameters</span></span>
<span data-ttu-id="8adcf-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8adcf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8adcf-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8adcf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8adcf-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8adcf-138">INPUTS</span></span>

### <span data-ttu-id="8adcf-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8adcf-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="8adcf-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8adcf-140">OUTPUTS</span></span>

### <span data-ttu-id="8adcf-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="8adcf-141">System.Object</span></span>

## <span data-ttu-id="8adcf-142">Note</span><span class="sxs-lookup"><span data-stu-id="8adcf-142">NOTES</span></span>

## <span data-ttu-id="8adcf-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8adcf-143">RELATED LINKS</span></span>

[<span data-ttu-id="8adcf-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8adcf-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="8adcf-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8adcf-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
