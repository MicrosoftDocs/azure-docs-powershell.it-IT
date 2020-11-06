---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: a0a6ee7f0430453aef343ba971126cd9aff63f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510299"
---
# <span data-ttu-id="ee6c2-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ee6c2-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="ee6c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee6c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee6c2-103">Avvia il failover non pianificato per un'entità di protezione del ripristino del sito o un piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee6c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee6c2-104">SYNTAX</span></span>

### <span data-ttu-id="ee6c2-105">ByPEObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ee6c2-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee6c2-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ee6c2-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee6c2-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="ee6c2-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee6c2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee6c2-108">DESCRIPTION</span></span>
<span data-ttu-id="ee6c2-109">Il cmdlet **Start-AzureRmSiteRecoveryUnplannedFailoverJob** avvia il failover non pianificato di un'entità o un piano di ripristino di un sito di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="ee6c2-110">Puoi verificare se il processo viene eseguito correttamente usando il cmdlet Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="ee6c2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee6c2-111">EXAMPLES</span></span>

## <span data-ttu-id="ee6c2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee6c2-112">PARAMETERS</span></span>

### <span data-ttu-id="ee6c2-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ee6c2-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ee6c2-114">Specifica il file di certificato principale.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-114">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="ee6c2-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ee6c2-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ee6c2-116">Specifica il file di certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-116">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="ee6c2-117">-Direzione</span><span class="sxs-lookup"><span data-stu-id="ee6c2-117">-Direction</span></span>
<span data-ttu-id="ee6c2-118">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-118">Specifies the direction of the failover.</span></span>
<span data-ttu-id="ee6c2-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee6c2-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ee6c2-120">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ee6c2-120">PrimaryToRecovery</span></span>
- <span data-ttu-id="ee6c2-121">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ee6c2-121">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="ee6c2-122">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="ee6c2-122">-PerformSourceSideActions</span></span>
<span data-ttu-id="ee6c2-123">Indica che l'azione può eseguire operazioni del sito di origine.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-123">Indicates that the action can perform source site operations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee6c2-124">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ee6c2-124">-ProtectionEntity</span></span>
<span data-ttu-id="ee6c2-125">Specifica l'oggetto entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-125">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="ee6c2-126">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ee6c2-126">-RecoveryPlan</span></span>
<span data-ttu-id="ee6c2-127">Specifica un oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-127">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="ee6c2-128">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ee6c2-128">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="ee6c2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee6c2-129">-DefaultProfile</span></span>
<span data-ttu-id="ee6c2-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee6c2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee6c2-131">CommonParameters</span></span>
<span data-ttu-id="ee6c2-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee6c2-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee6c2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee6c2-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee6c2-134">INPUTS</span></span>

### <span data-ttu-id="ee6c2-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ee6c2-135">ASRProtectionEntity</span></span>
<span data-ttu-id="ee6c2-136">Il parametro ' ProtectionEntity ' accetta il valore di tipo ' ASRProtectionEntity ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ee6c2-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="ee6c2-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ee6c2-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="ee6c2-138">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ee6c2-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="ee6c2-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ee6c2-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="ee6c2-140">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ee6c2-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="ee6c2-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee6c2-141">OUTPUTS</span></span>

### <span data-ttu-id="ee6c2-142">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ee6c2-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ee6c2-143">Note</span><span class="sxs-lookup"><span data-stu-id="ee6c2-143">NOTES</span></span>

## <span data-ttu-id="ee6c2-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee6c2-144">RELATED LINKS</span></span>

[<span data-ttu-id="ee6c2-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ee6c2-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

