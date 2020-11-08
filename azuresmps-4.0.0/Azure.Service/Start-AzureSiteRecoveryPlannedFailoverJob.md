---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023709"
---
# <span data-ttu-id="0d848-101">Start-AzureSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0d848-101">Start-AzureSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="0d848-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d848-102">SYNOPSIS</span></span>
<span data-ttu-id="0d848-103">Avvia un'operazione di failover pianificata per il ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="0d848-103">Starts a Site Recovery planned failover operation.</span></span>

## <span data-ttu-id="0d848-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d848-104">SYNTAX</span></span>

### <span data-ttu-id="0d848-105">ByRPId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0d848-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0d848-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="0d848-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0d848-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0d848-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0d848-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="0d848-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0d848-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d848-109">DESCRIPTION</span></span>
<span data-ttu-id="0d848-110">Il cmdlet **Start-AzureSiteRecoveryPlannedFailoverJob** avvia un failover pianificato per un'entità di protezione o un piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0d848-110">The **Start-AzureSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="0d848-111">Puoi verificare se il processo viene eseguito correttamente usando il cmdlet **Get-AzureSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="0d848-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="0d848-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d848-112">EXAMPLES</span></span>

### <span data-ttu-id="0d848-113">Esempio 1: avviare un processo di failover pianificato</span><span class="sxs-lookup"><span data-stu-id="0d848-113">Example 1: Start a planned failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="0d848-114">Tramite il cmdlet **Get-AzureSiteRecoveryProtectionContainer** , il primo comando recupera tutti i contenitori protetti nel Vault di ripristino del sito di Azure corrente e quindi archivia i risultati nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="0d848-114">The first command gets all protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>
<span data-ttu-id="0d848-115">In questo esempio è disponibile un singolo contenitore.</span><span class="sxs-lookup"><span data-stu-id="0d848-115">In this example, there is a single container.</span></span>

<span data-ttu-id="0d848-116">Il secondo comando ottiene le macchine virtuali protette che appartengono al contenitore archiviato in $Container usando il cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="0d848-116">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="0d848-117">Il comando Archivia i risultati nella variabile $Protected.</span><span class="sxs-lookup"><span data-stu-id="0d848-117">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="0d848-118">Il comando finale avvia il processo di failover nella direzione PrimaryToRecovery per le macchine virtuali protette archiviate in $Protected.</span><span class="sxs-lookup"><span data-stu-id="0d848-118">The final command starts the failover job in the direction PrimaryToRecovery for the protected virtual machines stored in $Protected.</span></span>

## <span data-ttu-id="0d848-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d848-119">PARAMETERS</span></span>

### <span data-ttu-id="0d848-120">-Direzione</span><span class="sxs-lookup"><span data-stu-id="0d848-120">-Direction</span></span>
<span data-ttu-id="0d848-121">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="0d848-121">Specifies the direction of the failover.</span></span>
<span data-ttu-id="0d848-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d848-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d848-123">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0d848-123">PrimaryToRecovery</span></span>
- <span data-ttu-id="0d848-124">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0d848-124">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d848-125">-Optimize</span><span class="sxs-lookup"><span data-stu-id="0d848-125">-Optimize</span></span>
<span data-ttu-id="0d848-126">Specifica il tipo di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="0d848-126">Specifies what to optimize for.</span></span>
<span data-ttu-id="0d848-127">Questo parametro viene applicato per il failover da un sito di Azure a un sito locale che richiede una sincronizzazione dei dati significativa.</span><span class="sxs-lookup"><span data-stu-id="0d848-127">This parameter applies for failover from an Azure site to an on-premise site which requires a significant data synchronization.</span></span>
<span data-ttu-id="0d848-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d848-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d848-129">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="0d848-129">ForDowntime</span></span>
- <span data-ttu-id="0d848-130">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="0d848-130">ForSynchronization</span></span>

<span data-ttu-id="0d848-131">Quando **ForDowntime** è specificato, indica che i dati vengono sincronizzati prima del failover per ridurre al minimo i tempi di inattività.</span><span class="sxs-lookup"><span data-stu-id="0d848-131">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="0d848-132">La sincronizzazione viene eseguita senza arrestare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d848-132">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="0d848-133">Al termine della sincronizzazione, il processo viene sospeso.</span><span class="sxs-lookup"><span data-stu-id="0d848-133">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="0d848-134">Riprendere il processo per eseguire un'operazione di sincronizzazione aggiuntiva che arresta la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d848-134">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="0d848-135">Quando **ForSynchronization** viene specificato, indica che i dati vengono sincronizzati durante il failover solo in modo che la sincronizzazione dei dati venga ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="0d848-135">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="0d848-136">Poiché questa impostazione è abilitata, la macchina virtuale viene arrestata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="0d848-136">Because this setting is enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="0d848-137">La sincronizzazione viene avviata dopo l'arresto per completare l'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="0d848-137">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="0d848-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="0d848-138">-Profile</span></span>
<span data-ttu-id="0d848-139">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d848-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0d848-140">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0d848-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d848-141">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="0d848-141">-ProtectionContainerId</span></span>
<span data-ttu-id="0d848-142">Specifica l'ID del contenitore protetto per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="0d848-142">Specifies the ID of the protected container for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d848-143">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0d848-143">-ProtectionEntity</span></span>
<span data-ttu-id="0d848-144">Specifica l'oggetto entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="0d848-144">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d848-145">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="0d848-145">-ProtectionEntityId</span></span>
<span data-ttu-id="0d848-146">Specifica un oggetto **ASRProtectionEntity** per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="0d848-146">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="0d848-147">Per ottenere un oggetto **ASRProtectionEntity** , usa il cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="0d848-147">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d848-148">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0d848-148">-RecoveryPlan</span></span>
<span data-ttu-id="0d848-149">Specifica un oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0d848-149">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="0d848-150">-RPId</span><span class="sxs-lookup"><span data-stu-id="0d848-150">-RPId</span></span>
<span data-ttu-id="0d848-151">Specifica l'ID di un piano di ripristino per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="0d848-151">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d848-152">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="0d848-152">-WaitForCompletion</span></span>
<span data-ttu-id="0d848-153">Indica che il cmdlet attende il completamento dell'operazione prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d848-153">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d848-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d848-154">CommonParameters</span></span>
<span data-ttu-id="0d848-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d848-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d848-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d848-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d848-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d848-157">INPUTS</span></span>

## <span data-ttu-id="0d848-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d848-158">OUTPUTS</span></span>

## <span data-ttu-id="0d848-159">Note</span><span class="sxs-lookup"><span data-stu-id="0d848-159">NOTES</span></span>

## <span data-ttu-id="0d848-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d848-160">RELATED LINKS</span></span>

[<span data-ttu-id="0d848-161">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0d848-161">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="0d848-162">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0d848-162">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


