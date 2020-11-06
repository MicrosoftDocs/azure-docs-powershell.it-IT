---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: f0350cfa9facfe8fc21e6c039c2fa5838bba8875
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514900"
---
# <span data-ttu-id="69a74-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="69a74-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="69a74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69a74-102">SYNOPSIS</span></span>
<span data-ttu-id="69a74-103">Avvia un'operazione di failover del test.</span><span class="sxs-lookup"><span data-stu-id="69a74-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69a74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69a74-104">SYNTAX</span></span>

### <span data-ttu-id="69a74-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="69a74-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a74-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="69a74-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a74-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="69a74-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a74-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="69a74-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a74-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="69a74-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a74-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="69a74-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69a74-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69a74-111">DESCRIPTION</span></span>
<span data-ttu-id="69a74-112">Il cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** avvia il failover del test di un elemento protetto o un piano di ripristino di un sito di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="69a74-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="69a74-113">Puoi verificare se il processo è riuscito usando il cmdlet Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="69a74-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="69a74-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69a74-114">EXAMPLES</span></span>

### <span data-ttu-id="69a74-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="69a74-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="69a74-116">Avvia l'operazione di failover del test per il piano di ripristino con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="69a74-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="69a74-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69a74-117">PARAMETERS</span></span>

### <span data-ttu-id="69a74-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="69a74-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="69a74-119">Specifica l'ID di rete virtuale di Azure per connettere il failover dei test alle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="69a74-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a74-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="69a74-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="69a74-121">Specifica se deve essere creato un nuovo servizio cloud o se il servizio cloud di ripristino configurato per la VM deve essere usato per il failover del test.</span><span class="sxs-lookup"><span data-stu-id="69a74-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a74-122">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="69a74-122">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="69a74-123">Specifica il file di certificato principale.</span><span class="sxs-lookup"><span data-stu-id="69a74-123">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="69a74-124">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="69a74-124">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="69a74-125">Specifica il file di certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="69a74-125">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="69a74-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a74-126">-DefaultProfile</span></span>
<span data-ttu-id="69a74-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69a74-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="69a74-128">-Direzione</span><span class="sxs-lookup"><span data-stu-id="69a74-128">-Direction</span></span>
<span data-ttu-id="69a74-129">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="69a74-129">Specifies the failover direction.</span></span>
<span data-ttu-id="69a74-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="69a74-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69a74-131">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="69a74-131">PrimaryToRecovery</span></span>
- <span data-ttu-id="69a74-132">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="69a74-132">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="69a74-133">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="69a74-133">-RecoveryPlan</span></span>
<span data-ttu-id="69a74-134">Specifica un oggetto piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="69a74-134">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69a74-135">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="69a74-135">-RecoveryPoint</span></span>
<span data-ttu-id="69a74-136">Specifica un punto di ripristino personalizzato per testare il failover del computer protetto.</span><span class="sxs-lookup"><span data-stu-id="69a74-136">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a74-137">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="69a74-137">-RecoveryTag</span></span>
<span data-ttu-id="69a74-138">Specifica il tag di recupero per testare il failover in</span><span class="sxs-lookup"><span data-stu-id="69a74-138">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a74-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="69a74-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="69a74-140">Specifica un elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="69a74-140">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69a74-141">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="69a74-141">-VMNetwork</span></span>
<span data-ttu-id="69a74-142">Specifica la rete della macchina virtuale di ripristino del sito per connettere le macchine virtuali di failover di test a.</span><span class="sxs-lookup"><span data-stu-id="69a74-142">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a74-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="69a74-143">-Confirm</span></span>
<span data-ttu-id="69a74-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69a74-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69a74-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69a74-145">-WhatIf</span></span>
<span data-ttu-id="69a74-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69a74-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69a74-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69a74-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69a74-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a74-148">CommonParameters</span></span>
<span data-ttu-id="69a74-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69a74-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a74-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69a74-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a74-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69a74-151">INPUTS</span></span>

### <span data-ttu-id="69a74-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="69a74-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="69a74-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="69a74-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="69a74-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69a74-154">OUTPUTS</span></span>

### <span data-ttu-id="69a74-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="69a74-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="69a74-156">Note</span><span class="sxs-lookup"><span data-stu-id="69a74-156">NOTES</span></span>

## <span data-ttu-id="69a74-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69a74-157">RELATED LINKS</span></span>

[<span data-ttu-id="69a74-158">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="69a74-158">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
