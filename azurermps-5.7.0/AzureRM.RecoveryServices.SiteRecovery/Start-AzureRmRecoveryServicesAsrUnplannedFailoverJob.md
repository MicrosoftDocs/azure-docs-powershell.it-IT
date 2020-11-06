---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: ba31be7094da4c4c17fa8c674728b8c32bfa2b8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508039"
---
# <span data-ttu-id="e40dc-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e40dc-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="e40dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e40dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e40dc-103">Avvia un'operazione di failover non pianificata.</span><span class="sxs-lookup"><span data-stu-id="e40dc-103">Starts a unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e40dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e40dc-104">SYNTAX</span></span>

### <span data-ttu-id="e40dc-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e40dc-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e40dc-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e40dc-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e40dc-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="e40dc-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e40dc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e40dc-108">DESCRIPTION</span></span>
<span data-ttu-id="e40dc-109">Il cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** avvia il failover del test di un elemento protetto o un piano di ripristino di un sito di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="e40dc-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="e40dc-110">Puoi verificare se il processo è riuscito usando il cmdlet Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="e40dc-110">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="e40dc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e40dc-111">EXAMPLES</span></span>

### <span data-ttu-id="e40dc-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e40dc-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="e40dc-113">Avvia l'operazione di failover del test per il piano di ripristino con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e40dc-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e40dc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e40dc-114">PARAMETERS</span></span>

### <span data-ttu-id="e40dc-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e40dc-115">-Confirm</span></span>
<span data-ttu-id="e40dc-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e40dc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e40dc-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e40dc-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="e40dc-118">Specifica il percorso del file del certificato primario di crittografia dei dati per il failover dell'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="e40dc-118">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="e40dc-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e40dc-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="e40dc-120">Specifica il percorso del file del certificato secondario per la crittografia dei dati per il failover dell'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="e40dc-120">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="e40dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e40dc-121">-DefaultProfile</span></span>
<span data-ttu-id="e40dc-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e40dc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="e40dc-123">-Direzione</span><span class="sxs-lookup"><span data-stu-id="e40dc-123">-Direction</span></span>
<span data-ttu-id="e40dc-124">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="e40dc-124">Specifies the failover direction.</span></span>
<span data-ttu-id="e40dc-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e40dc-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e40dc-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e40dc-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="e40dc-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e40dc-127">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="e40dc-128">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="e40dc-128">-PerformSourceSideAction</span></span>
<span data-ttu-id="e40dc-129">Eseguire l'operazione nel lato origine prima di avviare il failover non pianificato.</span><span class="sxs-lookup"><span data-stu-id="e40dc-129">Perform operation in source side before starting unplanned failover.</span></span>

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

### <span data-ttu-id="e40dc-130">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e40dc-130">-RecoveryPlan</span></span>
<span data-ttu-id="e40dc-131">Specifica un oggetto piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="e40dc-131">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="e40dc-132">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e40dc-132">-RecoveryPoint</span></span>
<span data-ttu-id="e40dc-133">Specifica un punto di ripristino personalizzato a cui eseguire il failover del computer protetto.</span><span class="sxs-lookup"><span data-stu-id="e40dc-133">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e40dc-134">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="e40dc-134">-RecoveryTag</span></span>
<span data-ttu-id="e40dc-135">Specifica il tag di recupero a cui eseguire il failover.</span><span class="sxs-lookup"><span data-stu-id="e40dc-135">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e40dc-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e40dc-136">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e40dc-137">Specifica un elemento protetto della replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="e40dc-137">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e40dc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e40dc-138">-WhatIf</span></span>
<span data-ttu-id="e40dc-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e40dc-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e40dc-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e40dc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e40dc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e40dc-141">CommonParameters</span></span>
<span data-ttu-id="e40dc-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e40dc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e40dc-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e40dc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e40dc-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e40dc-144">INPUTS</span></span>

### <span data-ttu-id="e40dc-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e40dc-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="e40dc-146">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e40dc-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e40dc-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e40dc-147">OUTPUTS</span></span>

### <span data-ttu-id="e40dc-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e40dc-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e40dc-149">Note</span><span class="sxs-lookup"><span data-stu-id="e40dc-149">NOTES</span></span>

## <span data-ttu-id="e40dc-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e40dc-150">RELATED LINKS</span></span>

[<span data-ttu-id="e40dc-151">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e40dc-151">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
