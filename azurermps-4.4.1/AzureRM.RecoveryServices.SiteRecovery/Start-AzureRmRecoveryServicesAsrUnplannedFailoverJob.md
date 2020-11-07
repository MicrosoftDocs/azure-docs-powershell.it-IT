---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 0d619084f62f4cad9b5bd7a9295987681994e53e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687114"
---
# <span data-ttu-id="df4ef-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="df4ef-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="df4ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df4ef-102">SYNOPSIS</span></span>
<span data-ttu-id="df4ef-103">Avvia un'operazione di failover non pianificata.</span><span class="sxs-lookup"><span data-stu-id="df4ef-103">Starts an unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df4ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df4ef-104">SYNTAX</span></span>

### <span data-ttu-id="df4ef-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="df4ef-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4ef-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="df4ef-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df4ef-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df4ef-107">DESCRIPTION</span></span>
<span data-ttu-id="df4ef-108">Il cmdlet **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** avvia il failover non pianificato di un elemento protetto o di un piano di ripristino di un sito di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="df4ef-108">The **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="df4ef-109">Puoi verificare se il processo viene eseguito correttamente usando il cmdlet Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="df4ef-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="df4ef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df4ef-110">EXAMPLES</span></span>

### <span data-ttu-id="df4ef-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="df4ef-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="df4ef-112">Avvia l'operazione di failover non pianificata per il piano di ripristino specificato usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="df4ef-112">Starts the unplanned failover operation for the specified recovery plan using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="df4ef-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df4ef-113">PARAMETERS</span></span>

### <span data-ttu-id="df4ef-114">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="df4ef-114">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="df4ef-115">Specifica il file di certificato principale.</span><span class="sxs-lookup"><span data-stu-id="df4ef-115">Specifies the primary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4ef-116">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="df4ef-116">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="df4ef-117">Specifica il file di certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="df4ef-117">Specifies the secondary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4ef-118">-Direzione</span><span class="sxs-lookup"><span data-stu-id="df4ef-118">-Direction</span></span>
<span data-ttu-id="df4ef-119">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="df4ef-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="df4ef-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="df4ef-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="df4ef-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="df4ef-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="df4ef-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="df4ef-122">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4ef-123">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="df4ef-123">-PerformSourceSideAction</span></span>
<span data-ttu-id="df4ef-124">Indica che tutte le operazioni del sito di origine specificate nel piano di ripristino devono essere eseguite come parte del failover.</span><span class="sxs-lookup"><span data-stu-id="df4ef-124">Indicates that any source site operations specified in the recovery plan must be attempted to be performed as part of the fail over.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4ef-125">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="df4ef-125">-RecoveryPlan</span></span>
<span data-ttu-id="df4ef-126">Specifica un oggetto piano di ripristino ASR che corrisponde al piano di ripristino in cui deve essere eseguita l'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="df4ef-126">Specifies an ASR recovery plan object corresponding to the recovery plan on which the failover operation is to be performed.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4ef-127">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="df4ef-127">-ReplicationProtectedItem</span></span>
<span data-ttu-id="df4ef-128">Specifica l'oggetto elemento protetto della replica ASR che corrisponde all'elemento protetto da replica in cui deve essere eseguita l'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="df4ef-128">Specifies the ASR replication protected item object corresponding to the replication protected item on which the failover operation is to be performed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4ef-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="df4ef-129">-Confirm</span></span>
<span data-ttu-id="df4ef-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df4ef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df4ef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df4ef-131">-WhatIf</span></span>
<span data-ttu-id="df4ef-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df4ef-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df4ef-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df4ef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df4ef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4ef-134">CommonParameters</span></span>
<span data-ttu-id="df4ef-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df4ef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4ef-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df4ef-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4ef-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df4ef-137">INPUTS</span></span>

### <span data-ttu-id="df4ef-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="df4ef-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="df4ef-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="df4ef-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="df4ef-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df4ef-140">OUTPUTS</span></span>

### <span data-ttu-id="df4ef-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="df4ef-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="df4ef-142">Note</span><span class="sxs-lookup"><span data-stu-id="df4ef-142">NOTES</span></span>

## <span data-ttu-id="df4ef-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df4ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="df4ef-144">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="df4ef-144">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)


