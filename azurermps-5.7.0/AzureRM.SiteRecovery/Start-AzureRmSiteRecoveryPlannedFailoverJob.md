---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: f5bf4372c1140402cb56ca875b5532387dd06704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687417"
---
# <span data-ttu-id="4fc20-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="4fc20-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="4fc20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fc20-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc20-103">Avvia un'operazione di failover pianificata per il ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="4fc20-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fc20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fc20-104">SYNTAX</span></span>

### <span data-ttu-id="4fc20-105">ByPEObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4fc20-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc20-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="4fc20-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc20-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="4fc20-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fc20-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fc20-108">DESCRIPTION</span></span>
<span data-ttu-id="4fc20-109">Il cmdlet **Start-AzureRmSiteRecoveryPlannedFailoverJob** avvia un failover pianificato per un'entità di protezione o un piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4fc20-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="4fc20-110">Puoi verificare se il processo viene eseguito correttamente usando il cmdlet Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="4fc20-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="4fc20-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fc20-111">EXAMPLES</span></span>

## <span data-ttu-id="4fc20-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fc20-112">PARAMETERS</span></span>

### <span data-ttu-id="4fc20-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="4fc20-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="4fc20-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4fc20-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fc20-115">Sì</span><span class="sxs-lookup"><span data-stu-id="4fc20-115">Yes</span></span>
- <span data-ttu-id="4fc20-116">Non</span><span class="sxs-lookup"><span data-stu-id="4fc20-116">No</span></span>

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

### <span data-ttu-id="4fc20-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="4fc20-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="4fc20-118">Specifica il file di certificato principale.</span><span class="sxs-lookup"><span data-stu-id="4fc20-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="4fc20-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="4fc20-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="4fc20-120">Specifica il file di certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="4fc20-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="4fc20-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc20-121">-DefaultProfile</span></span>
<span data-ttu-id="4fc20-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc20-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fc20-123">-Direzione</span><span class="sxs-lookup"><span data-stu-id="4fc20-123">-Direction</span></span>
<span data-ttu-id="4fc20-124">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="4fc20-124">Specifies the direction of the failover.</span></span>
<span data-ttu-id="4fc20-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4fc20-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fc20-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="4fc20-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="4fc20-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="4fc20-127">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="4fc20-128">-Optimize</span><span class="sxs-lookup"><span data-stu-id="4fc20-128">-Optimize</span></span>
<span data-ttu-id="4fc20-129">Specifica il tipo di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="4fc20-129">Specifies what to optimize for.</span></span>
<span data-ttu-id="4fc20-130">Questo parametro si applica quando il failover viene eseguito da un sito di Azure a un sito locale che richiede una sostanziale sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4fc20-130">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="4fc20-131">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="4fc20-131">Valid values are:</span></span>

- <span data-ttu-id="4fc20-132">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="4fc20-132">ForDowntime</span></span>
- <span data-ttu-id="4fc20-133">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="4fc20-133">ForSynchronization</span></span>

<span data-ttu-id="4fc20-134">Quando **ForDowntime** è specificato, indica che i dati vengono sincronizzati prima del failover per ridurre al minimo i tempi di inattività.</span><span class="sxs-lookup"><span data-stu-id="4fc20-134">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="4fc20-135">La sincronizzazione viene eseguita senza arrestare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4fc20-135">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="4fc20-136">Al termine della sincronizzazione, il processo viene sospeso.</span><span class="sxs-lookup"><span data-stu-id="4fc20-136">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="4fc20-137">Riprendere il processo per eseguire un'operazione di sincronizzazione aggiuntiva che arresta la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4fc20-137">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="4fc20-138">Quando **ForSynchronization** viene specificato, indica che i dati vengono sincronizzati durante il failover solo in modo che la sincronizzazione dei dati venga ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="4fc20-138">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="4fc20-139">Con questa impostazione abilitata, la macchina virtuale viene arrestata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="4fc20-139">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="4fc20-140">La sincronizzazione viene avviata dopo l'arresto per completare l'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="4fc20-140">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="4fc20-141">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="4fc20-141">-ProtectionEntity</span></span>
<span data-ttu-id="4fc20-142">Specifica l'oggetto entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="4fc20-142">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="4fc20-143">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fc20-143">-RecoveryPlan</span></span>
<span data-ttu-id="4fc20-144">Specifica un oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4fc20-144">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="4fc20-145">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4fc20-145">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="4fc20-146">-Server</span><span class="sxs-lookup"><span data-stu-id="4fc20-146">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc20-147">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4fc20-147">-ServicesProvider</span></span>
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

### <span data-ttu-id="4fc20-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc20-148">CommonParameters</span></span>
<span data-ttu-id="4fc20-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc20-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc20-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc20-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc20-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fc20-151">INPUTS</span></span>

### <span data-ttu-id="4fc20-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="4fc20-152">ASRProtectionEntity</span></span>
<span data-ttu-id="4fc20-153">Il parametro ' ProtectionEntity ' accetta il valore di tipo ' ASRProtectionEntity ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4fc20-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="4fc20-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fc20-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="4fc20-155">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4fc20-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="4fc20-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4fc20-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="4fc20-157">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4fc20-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="4fc20-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fc20-158">OUTPUTS</span></span>

### <span data-ttu-id="4fc20-159">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4fc20-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4fc20-160">Note</span><span class="sxs-lookup"><span data-stu-id="4fc20-160">NOTES</span></span>

## <span data-ttu-id="4fc20-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fc20-161">RELATED LINKS</span></span>

