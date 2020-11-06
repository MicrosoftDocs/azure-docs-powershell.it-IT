---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: d547de0af8d4f7b4f98a572d95dcc023d975fc2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519998"
---
# <span data-ttu-id="5c1d1-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="5c1d1-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="5c1d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1d1-103">Avvia un'operazione di failover del test.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c1d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c1d1-104">SYNTAX</span></span>

### <span data-ttu-id="5c1d1-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c1d1-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1d1-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5c1d1-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c1d1-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="5c1d1-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1d1-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="5c1d1-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1d1-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="5c1d1-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1d1-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="5c1d1-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c1d1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c1d1-111">DESCRIPTION</span></span>
<span data-ttu-id="5c1d1-112">Il cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** avvia il failover del test di un elemento protetto o un piano di ripristino di un sito di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="5c1d1-113">Puoi verificare se il processo è riuscito usando il cmdlet Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="5c1d1-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c1d1-114">EXAMPLES</span></span>

### <span data-ttu-id="5c1d1-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5c1d1-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="5c1d1-116">Avvia l'operazione di failover del test per il piano di ripristino con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5c1d1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c1d1-117">PARAMETERS</span></span>

### <span data-ttu-id="5c1d1-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="5c1d1-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="5c1d1-119">Specifica l'ID di rete virtuale di Azure per connettere il failover dei test alle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1d1-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="5c1d1-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="5c1d1-121">Specifica il file di certificato principale.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="5c1d1-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="5c1d1-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="5c1d1-123">Specifica il file di certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="5c1d1-124">-Direzione</span><span class="sxs-lookup"><span data-stu-id="5c1d1-124">-Direction</span></span>
<span data-ttu-id="5c1d1-125">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-125">Specifies the failover direction.</span></span>
<span data-ttu-id="5c1d1-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c1d1-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5c1d1-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="5c1d1-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="5c1d1-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="5c1d1-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="5c1d1-129">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5c1d1-129">-RecoveryPlan</span></span>
<span data-ttu-id="5c1d1-130">Specifica un oggetto piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-130">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1d1-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5c1d1-131">-ReplicationProtectedItem</span></span>
<span data-ttu-id="5c1d1-132">Specifica un elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-132">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1d1-133">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="5c1d1-133">-VMNetwork</span></span>
<span data-ttu-id="5c1d1-134">Specifica la rete della macchina virtuale di ripristino del sito per connettere le macchine virtuali di failover di test a.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-134">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1d1-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5c1d1-135">-Confirm</span></span>
<span data-ttu-id="5c1d1-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c1d1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c1d1-137">-WhatIf</span></span>
<span data-ttu-id="5c1d1-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c1d1-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c1d1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1d1-140">CommonParameters</span></span>
<span data-ttu-id="5c1d1-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c1d1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1d1-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1d1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1d1-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c1d1-143">INPUTS</span></span>

### <span data-ttu-id="5c1d1-144">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5c1d1-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="5c1d1-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5c1d1-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5c1d1-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c1d1-146">OUTPUTS</span></span>

### <span data-ttu-id="5c1d1-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5c1d1-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5c1d1-148">Note</span><span class="sxs-lookup"><span data-stu-id="5c1d1-148">NOTES</span></span>

## <span data-ttu-id="5c1d1-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c1d1-149">RELATED LINKS</span></span>

[<span data-ttu-id="5c1d1-150">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="5c1d1-150">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
