---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: ee39fdfcb40c394bfbd7f1d804d8d9785a63f7c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677558"
---
# <span data-ttu-id="01dbd-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="01dbd-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="01dbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="01dbd-103">Avvia un'operazione di failover pianificata.</span><span class="sxs-lookup"><span data-stu-id="01dbd-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="01dbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01dbd-104">SYNTAX</span></span>

### <span data-ttu-id="01dbd-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01dbd-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01dbd-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="01dbd-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01dbd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01dbd-107">DESCRIPTION</span></span>
<span data-ttu-id="01dbd-108">Il cmdlet **Start-AzRecoveryServicesAsrPlannedFailoverJob** avvia un failover pianificato per un elemento protetto o un piano di ripristino di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="01dbd-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="01dbd-109">Puoi verificare se il processo viene eseguito correttamente usando il cmdlet Get-AzRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="01dbd-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="01dbd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01dbd-110">EXAMPLES</span></span>

### <span data-ttu-id="01dbd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="01dbd-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="01dbd-112">Avvia il failover pianificato per il piano di ripristino ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="01dbd-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="01dbd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01dbd-113">PARAMETERS</span></span>

### <span data-ttu-id="01dbd-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="01dbd-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="01dbd-115">Creare la macchina virtuale se non viene trovata durante il ripristino dell'area principale (usata in recupero di posizione alternativo). I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="01dbd-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01dbd-116">Sì</span><span class="sxs-lookup"><span data-stu-id="01dbd-116">Yes</span></span>
- <span data-ttu-id="01dbd-117">Non</span><span class="sxs-lookup"><span data-stu-id="01dbd-117">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01dbd-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="01dbd-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="01dbd-119">Specifica il file di certificato principale.</span><span class="sxs-lookup"><span data-stu-id="01dbd-119">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01dbd-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="01dbd-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="01dbd-121">Specifica il file di certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="01dbd-121">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01dbd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01dbd-122">-DefaultProfile</span></span>
<span data-ttu-id="01dbd-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01dbd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="01dbd-124">-Direzione</span><span class="sxs-lookup"><span data-stu-id="01dbd-124">-Direction</span></span>
<span data-ttu-id="01dbd-125">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="01dbd-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="01dbd-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="01dbd-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01dbd-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="01dbd-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="01dbd-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="01dbd-128">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01dbd-129">-Optimize</span><span class="sxs-lookup"><span data-stu-id="01dbd-129">-Optimize</span></span>
<span data-ttu-id="01dbd-130">Specifica il tipo di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="01dbd-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="01dbd-131">Questo parametro si applica quando il failover viene eseguito da un sito di Azure a un sito locale che richiede una sostanziale sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="01dbd-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="01dbd-132">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="01dbd-132">Valid values are:</span></span>

- <span data-ttu-id="01dbd-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="01dbd-133">ForDowntime</span></span>
- <span data-ttu-id="01dbd-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="01dbd-134">ForSynchronization</span></span>

<span data-ttu-id="01dbd-135">Quando **ForDowntime** è specificato, indica che i dati vengono sincronizzati prima del failover per ridurre al minimo i tempi di inattività.</span><span class="sxs-lookup"><span data-stu-id="01dbd-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="01dbd-136">La sincronizzazione viene eseguita senza arrestare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="01dbd-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="01dbd-137">Al termine della sincronizzazione, il processo viene sospeso.</span><span class="sxs-lookup"><span data-stu-id="01dbd-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="01dbd-138">Riprendere il processo per eseguire un'operazione di sincronizzazione aggiuntiva che arresta la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="01dbd-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="01dbd-139">Quando **ForSynchronization** viene specificato, indica che i dati vengono sincronizzati durante il failover solo in modo che la sincronizzazione dei dati venga ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="01dbd-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="01dbd-140">Con questa impostazione abilitata, la macchina virtuale viene arrestata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="01dbd-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="01dbd-141">La sincronizzazione viene avviata dopo l'arresto per completare l'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="01dbd-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01dbd-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="01dbd-142">-RecoveryPlan</span></span>
<span data-ttu-id="01dbd-143">Specifica l'oggetto piano di ripristino ASR che corrisponde al piano di ripristino per il quale non è possibile eseguire il failover.</span><span class="sxs-lookup"><span data-stu-id="01dbd-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01dbd-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="01dbd-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="01dbd-145">Specifica l'oggetto elemento protetto della replica ASR che corrisponde all'elemento protetto dalla replica per il quale non è possibile eseguire il failover.</span><span class="sxs-lookup"><span data-stu-id="01dbd-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01dbd-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="01dbd-146">-ServicesProvider</span></span>
<span data-ttu-id="01dbd-147">Identifica l'host su cui creare la macchina virtuale durante il failback in una posizione alternativa specificando l'oggetto provider di servizi ASR che corrisponde al provider di servizi ASR in esecuzione nell'host.</span><span class="sxs-lookup"><span data-stu-id="01dbd-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01dbd-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="01dbd-148">-Confirm</span></span>
<span data-ttu-id="01dbd-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01dbd-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01dbd-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01dbd-150">-WhatIf</span></span>
<span data-ttu-id="01dbd-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01dbd-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01dbd-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01dbd-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01dbd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01dbd-153">CommonParameters</span></span>
<span data-ttu-id="01dbd-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01dbd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01dbd-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01dbd-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01dbd-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01dbd-156">INPUTS</span></span>

### <span data-ttu-id="01dbd-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="01dbd-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="01dbd-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="01dbd-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="01dbd-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01dbd-159">OUTPUTS</span></span>

### <span data-ttu-id="01dbd-160">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="01dbd-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="01dbd-161">Note</span><span class="sxs-lookup"><span data-stu-id="01dbd-161">NOTES</span></span>

## <span data-ttu-id="01dbd-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01dbd-162">RELATED LINKS</span></span>
