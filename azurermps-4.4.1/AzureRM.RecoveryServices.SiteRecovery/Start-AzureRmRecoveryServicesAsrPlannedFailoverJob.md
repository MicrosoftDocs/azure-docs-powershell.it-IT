---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e96a57a00d6314015d1d13f4f540d3f763c96c23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513059"
---
# <span data-ttu-id="61ed7-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="61ed7-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="61ed7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="61ed7-103">Avvia un'operazione di failover pianificata.</span><span class="sxs-lookup"><span data-stu-id="61ed7-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61ed7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61ed7-104">SYNTAX</span></span>

### <span data-ttu-id="61ed7-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61ed7-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61ed7-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="61ed7-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61ed7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61ed7-107">DESCRIPTION</span></span>
<span data-ttu-id="61ed7-108">Il cmdlet **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** avvia un failover pianificato per un elemento protetto o un piano di ripristino di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="61ed7-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="61ed7-109">Puoi verificare se il processo viene eseguito correttamente usando il cmdlet Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="61ed7-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="61ed7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61ed7-110">EXAMPLES</span></span>

### <span data-ttu-id="61ed7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61ed7-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="61ed7-112">Avvia il failover pianificato per il piano di ripristino ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="61ed7-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="61ed7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61ed7-113">PARAMETERS</span></span>

### <span data-ttu-id="61ed7-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="61ed7-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="61ed7-115">Creare la macchina virtuale se non viene trovata durante il ripristino dell'area principale (usata in recupero di posizione alternativo). I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="61ed7-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61ed7-116">Sì</span><span class="sxs-lookup"><span data-stu-id="61ed7-116">Yes</span></span>
- <span data-ttu-id="61ed7-117">Non</span><span class="sxs-lookup"><span data-stu-id="61ed7-117">No</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ed7-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="61ed7-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="61ed7-119">Specifica il file di certificato principale.</span><span class="sxs-lookup"><span data-stu-id="61ed7-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="61ed7-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="61ed7-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="61ed7-121">Specifica il file di certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="61ed7-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="61ed7-122">-Direzione</span><span class="sxs-lookup"><span data-stu-id="61ed7-122">-Direction</span></span>
<span data-ttu-id="61ed7-123">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="61ed7-123">Specifies the direction of the failover.</span></span>
<span data-ttu-id="61ed7-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="61ed7-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61ed7-125">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="61ed7-125">PrimaryToRecovery</span></span>
- <span data-ttu-id="61ed7-126">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="61ed7-126">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="61ed7-127">-Optimize</span><span class="sxs-lookup"><span data-stu-id="61ed7-127">-Optimize</span></span>
<span data-ttu-id="61ed7-128">Specifica il tipo di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="61ed7-128">Specifies what to optimize for.</span></span>
<span data-ttu-id="61ed7-129">Questo parametro si applica quando il failover viene eseguito da un sito di Azure a un sito locale che richiede una sostanziale sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="61ed7-129">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="61ed7-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="61ed7-130">Valid values are:</span></span>

- <span data-ttu-id="61ed7-131">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="61ed7-131">ForDowntime</span></span>
- <span data-ttu-id="61ed7-132">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="61ed7-132">ForSynchronization</span></span>

<span data-ttu-id="61ed7-133">Quando **ForDowntime** è specificato, indica che i dati vengono sincronizzati prima del failover per ridurre al minimo i tempi di inattività.</span><span class="sxs-lookup"><span data-stu-id="61ed7-133">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="61ed7-134">La sincronizzazione viene eseguita senza arrestare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61ed7-134">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="61ed7-135">Al termine della sincronizzazione, il processo viene sospeso.</span><span class="sxs-lookup"><span data-stu-id="61ed7-135">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="61ed7-136">Riprendere il processo per eseguire un'operazione di sincronizzazione aggiuntiva che arresta la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61ed7-136">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="61ed7-137">Quando **ForSynchronization** viene specificato, indica che i dati vengono sincronizzati durante il failover solo in modo che la sincronizzazione dei dati venga ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="61ed7-137">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="61ed7-138">Con questa impostazione abilitata, la macchina virtuale viene arrestata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="61ed7-138">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="61ed7-139">La sincronizzazione viene avviata dopo l'arresto per completare l'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="61ed7-139">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ed7-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="61ed7-140">-RecoveryPlan</span></span>
<span data-ttu-id="61ed7-141">Specifica l'oggetto piano di ripristino ASR che corrisponde al piano di ripristino per il quale non è possibile eseguire il failover.</span><span class="sxs-lookup"><span data-stu-id="61ed7-141">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="61ed7-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="61ed7-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="61ed7-143">Specifica l'oggetto elemento protetto della replica ASR che corrisponde all'elemento protetto dalla replica per il quale non è possibile eseguire il failover.</span><span class="sxs-lookup"><span data-stu-id="61ed7-143">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="61ed7-144">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="61ed7-144">-ServicesProvider</span></span>
<span data-ttu-id="61ed7-145">Identifica l'host su cui creare la macchina virtuale durante il failback in una posizione alternativa specificando l'oggetto provider di servizi ASR che corrisponde al provider di servizi ASR in esecuzione nell'host.</span><span class="sxs-lookup"><span data-stu-id="61ed7-145">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span> 

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ed7-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61ed7-146">-Confirm</span></span>
<span data-ttu-id="61ed7-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61ed7-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61ed7-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ed7-148">-WhatIf</span></span>
<span data-ttu-id="61ed7-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61ed7-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61ed7-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61ed7-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61ed7-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ed7-151">CommonParameters</span></span>
<span data-ttu-id="61ed7-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ed7-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ed7-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61ed7-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ed7-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61ed7-154">INPUTS</span></span>

### <span data-ttu-id="61ed7-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="61ed7-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="61ed7-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="61ed7-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="61ed7-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61ed7-157">OUTPUTS</span></span>

### <span data-ttu-id="61ed7-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="61ed7-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="61ed7-159">Note</span><span class="sxs-lookup"><span data-stu-id="61ed7-159">NOTES</span></span>

## <span data-ttu-id="61ed7-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61ed7-160">RELATED LINKS</span></span>

