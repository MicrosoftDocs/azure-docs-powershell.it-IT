---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: e723aacbfbd1b782a91fdc6aa589bfe15df42cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515984"
---
# <span data-ttu-id="b68d4-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="b68d4-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="b68d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b68d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b68d4-103">Avvia un'operazione di failover pianificata per il ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="b68d4-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b68d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b68d4-104">SYNTAX</span></span>

### <span data-ttu-id="b68d4-105">ByPEObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b68d4-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b68d4-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="b68d4-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b68d4-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="b68d4-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b68d4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b68d4-108">DESCRIPTION</span></span>
<span data-ttu-id="b68d4-109">Il cmdlet **Start-AzureRmSiteRecoveryPlannedFailoverJob** avvia un failover pianificato per un'entità di protezione o un piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b68d4-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="b68d4-110">Puoi verificare se il processo viene eseguito correttamente usando il cmdlet Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="b68d4-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="b68d4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b68d4-111">EXAMPLES</span></span>

## <span data-ttu-id="b68d4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b68d4-112">PARAMETERS</span></span>

### <span data-ttu-id="b68d4-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="b68d4-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="b68d4-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b68d4-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b68d4-115">Sì</span><span class="sxs-lookup"><span data-stu-id="b68d4-115">Yes</span></span>
- <span data-ttu-id="b68d4-116">Non</span><span class="sxs-lookup"><span data-stu-id="b68d4-116">No</span></span>

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

### <span data-ttu-id="b68d4-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b68d4-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="b68d4-118">Specifica il file di certificato principale.</span><span class="sxs-lookup"><span data-stu-id="b68d4-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="b68d4-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b68d4-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="b68d4-120">Specifica il file di certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="b68d4-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="b68d4-121">-Direzione</span><span class="sxs-lookup"><span data-stu-id="b68d4-121">-Direction</span></span>
<span data-ttu-id="b68d4-122">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="b68d4-122">Specifies the direction of the failover.</span></span>
<span data-ttu-id="b68d4-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b68d4-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b68d4-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="b68d4-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="b68d4-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="b68d4-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="b68d4-126">-Optimize</span><span class="sxs-lookup"><span data-stu-id="b68d4-126">-Optimize</span></span>
<span data-ttu-id="b68d4-127">Specifica il tipo di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="b68d4-127">Specifies what to optimize for.</span></span>
<span data-ttu-id="b68d4-128">Questo parametro si applica quando il failover viene eseguito da un sito di Azure a un sito locale che richiede una sostanziale sincronizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="b68d4-128">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="b68d4-129">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b68d4-129">Valid values are:</span></span>

- <span data-ttu-id="b68d4-130">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="b68d4-130">ForDowntime</span></span>
- <span data-ttu-id="b68d4-131">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="b68d4-131">ForSynchronization</span></span>

<span data-ttu-id="b68d4-132">Quando **ForDowntime** è specificato, indica che i dati vengono sincronizzati prima del failover per ridurre al minimo i tempi di inattività.</span><span class="sxs-lookup"><span data-stu-id="b68d4-132">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="b68d4-133">La sincronizzazione viene eseguita senza arrestare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b68d4-133">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="b68d4-134">Al termine della sincronizzazione, il processo viene sospeso.</span><span class="sxs-lookup"><span data-stu-id="b68d4-134">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="b68d4-135">Riprendere il processo per eseguire un'operazione di sincronizzazione aggiuntiva che arresta la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b68d4-135">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="b68d4-136">Quando **ForSynchronization** viene specificato, indica che i dati vengono sincronizzati durante il failover solo in modo che la sincronizzazione dei dati venga ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="b68d4-136">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="b68d4-137">Con questa impostazione abilitata, la macchina virtuale viene arrestata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b68d4-137">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="b68d4-138">La sincronizzazione viene avviata dopo l'arresto per completare l'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="b68d4-138">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="b68d4-139">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b68d4-139">-ProtectionEntity</span></span>
<span data-ttu-id="b68d4-140">Specifica l'oggetto entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="b68d4-140">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b68d4-141">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b68d4-141">-RecoveryPlan</span></span>
<span data-ttu-id="b68d4-142">Specifica un oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b68d4-142">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b68d4-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b68d4-143">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b68d4-144">-Server</span><span class="sxs-lookup"><span data-stu-id="b68d4-144">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b68d4-145">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b68d4-145">-ServicesProvider</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b68d4-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68d4-146">-DefaultProfile</span></span>
<span data-ttu-id="b68d4-147">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b68d4-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b68d4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68d4-148">CommonParameters</span></span>
<span data-ttu-id="b68d4-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b68d4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68d4-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b68d4-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68d4-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b68d4-151">INPUTS</span></span>

### <span data-ttu-id="b68d4-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b68d4-152">ASRProtectionEntity</span></span>
<span data-ttu-id="b68d4-153">Il parametro ' ProtectionEntity ' accetta il valore di tipo ' ASRProtectionEntity ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b68d4-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="b68d4-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b68d4-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="b68d4-155">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b68d4-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="b68d4-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b68d4-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="b68d4-157">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b68d4-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="b68d4-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b68d4-158">OUTPUTS</span></span>

### <span data-ttu-id="b68d4-159">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b68d4-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b68d4-160">Note</span><span class="sxs-lookup"><span data-stu-id="b68d4-160">NOTES</span></span>

## <span data-ttu-id="b68d4-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b68d4-161">RELATED LINKS</span></span>

