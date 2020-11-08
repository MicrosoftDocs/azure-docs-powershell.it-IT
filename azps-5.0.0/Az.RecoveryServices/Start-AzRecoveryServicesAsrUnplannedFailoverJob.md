---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 61bb846067127b8e7d0a4deca0dd9a726d9dd1f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193877"
---
# <span data-ttu-id="ad22f-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ad22f-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="ad22f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad22f-102">SYNOPSIS</span></span>
<span data-ttu-id="ad22f-103">Avvia un'operazione di failover non pianificata.</span><span class="sxs-lookup"><span data-stu-id="ad22f-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="ad22f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad22f-104">SYNTAX</span></span>

### <span data-ttu-id="ad22f-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad22f-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad22f-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ad22f-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad22f-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="ad22f-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad22f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad22f-108">DESCRIPTION</span></span>
<span data-ttu-id="ad22f-109">Il cmdlet **Start-AzRecoveryServicesAsrUnplannedFailoverJob** avvia il failover non pianificato di un elemento protetto o di un piano di ripristino di un sito di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="ad22f-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="ad22f-110">Puoi verificare se il processo è riuscito usando il cmdlet Get-AzRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="ad22f-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="ad22f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad22f-111">EXAMPLES</span></span>

### <span data-ttu-id="ad22f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad22f-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="ad22f-113">Avvia l'operazione di failover non pianificata per il piano di ripristino con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ad22f-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ad22f-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ad22f-114">Example 2</span></span>

<span data-ttu-id="ad22f-115">Avvia un'operazione di failover non pianificata.</span><span class="sxs-lookup"><span data-stu-id="ad22f-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="ad22f-116">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="ad22f-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="ad22f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad22f-117">PARAMETERS</span></span>

### <span data-ttu-id="ad22f-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ad22f-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ad22f-119">Specifica il percorso del file del certificato primario di crittografia dei dati per il failover dell'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="ad22f-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="ad22f-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ad22f-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ad22f-121">Specifica il percorso del file del certificato secondario per la crittografia dei dati per il failover dell'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="ad22f-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="ad22f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad22f-122">-DefaultProfile</span></span>
<span data-ttu-id="ad22f-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad22f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ad22f-124">-Direzione</span><span class="sxs-lookup"><span data-stu-id="ad22f-124">-Direction</span></span>
<span data-ttu-id="ad22f-125">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="ad22f-125">Specifies the failover direction.</span></span>
<span data-ttu-id="ad22f-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ad22f-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad22f-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ad22f-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="ad22f-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ad22f-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="ad22f-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="ad22f-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="ad22f-130">Eseguire l'operazione nel lato origine prima di avviare il failover non pianificato.</span><span class="sxs-lookup"><span data-stu-id="ad22f-130">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad22f-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad22f-131">-RecoveryPlan</span></span>
<span data-ttu-id="ad22f-132">Specifica un oggetto piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="ad22f-132">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="ad22f-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ad22f-133">-RecoveryPoint</span></span>
<span data-ttu-id="ad22f-134">Specifica un punto di ripristino personalizzato a cui eseguire il failover del computer protetto.</span><span class="sxs-lookup"><span data-stu-id="ad22f-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad22f-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="ad22f-135">-RecoveryTag</span></span>
<span data-ttu-id="ad22f-136">Specifica il tag di recupero a cui eseguire il failover.</span><span class="sxs-lookup"><span data-stu-id="ad22f-136">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad22f-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ad22f-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ad22f-138">Specifica un elemento protetto della replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="ad22f-138">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad22f-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad22f-139">-Confirm</span></span>
<span data-ttu-id="ad22f-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad22f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad22f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad22f-141">-WhatIf</span></span>
<span data-ttu-id="ad22f-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad22f-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad22f-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad22f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad22f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad22f-144">CommonParameters</span></span>
<span data-ttu-id="ad22f-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad22f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad22f-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad22f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad22f-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad22f-147">INPUTS</span></span>

### <span data-ttu-id="ad22f-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ad22f-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="ad22f-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ad22f-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ad22f-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad22f-150">OUTPUTS</span></span>

### <span data-ttu-id="ad22f-151">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ad22f-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ad22f-152">Note</span><span class="sxs-lookup"><span data-stu-id="ad22f-152">NOTES</span></span>

## <span data-ttu-id="ad22f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad22f-153">RELATED LINKS</span></span>

[<span data-ttu-id="ad22f-154">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ad22f-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)