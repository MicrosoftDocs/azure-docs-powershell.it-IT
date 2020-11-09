---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310092"
---
# <span data-ttu-id="9944e-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="9944e-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="9944e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9944e-102">SYNOPSIS</span></span>
<span data-ttu-id="9944e-103">Avvia un'operazione di failover del test.</span><span class="sxs-lookup"><span data-stu-id="9944e-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="9944e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9944e-104">SYNTAX</span></span>

### <span data-ttu-id="9944e-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9944e-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9944e-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="9944e-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9944e-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="9944e-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9944e-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="9944e-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9944e-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="9944e-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9944e-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="9944e-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9944e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9944e-111">DESCRIPTION</span></span>
<span data-ttu-id="9944e-112">Il cmdlet **Start-AzRecoveryServicesAsrTestFailoverJob** avvia il failover del test di un elemento protetto o un piano di ripristino di un sito di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="9944e-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="9944e-113">Puoi verificare se il processo è riuscito usando il cmdlet Get-AzRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="9944e-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="9944e-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9944e-114">EXAMPLES</span></span>

### <span data-ttu-id="9944e-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9944e-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="9944e-116">Avvia l'operazione di failover del test per il piano di ripristino con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9944e-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="9944e-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9944e-117">Example 2</span></span>

<span data-ttu-id="9944e-118">Avvia un'operazione di failover del test.</span><span class="sxs-lookup"><span data-stu-id="9944e-118">Starts a test failover operation.</span></span> <span data-ttu-id="9944e-119">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="9944e-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="9944e-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9944e-120">PARAMETERS</span></span>

### <span data-ttu-id="9944e-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="9944e-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="9944e-122">Specifica l'ID di rete VM di Azure per ripristino VM dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="9944e-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="9944e-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="9944e-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="9944e-124">Specifica se deve essere creato un nuovo servizio cloud o se il servizio cloud di ripristino configurato per la VM deve essere usato per il failover del test.</span><span class="sxs-lookup"><span data-stu-id="9944e-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="9944e-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="9944e-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="9944e-126">Specifica il file di certificato principale.</span><span class="sxs-lookup"><span data-stu-id="9944e-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="9944e-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="9944e-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="9944e-128">Specifica il file di certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="9944e-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="9944e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9944e-129">-DefaultProfile</span></span>
<span data-ttu-id="9944e-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9944e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9944e-131">-Direzione</span><span class="sxs-lookup"><span data-stu-id="9944e-131">-Direction</span></span>
<span data-ttu-id="9944e-132">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="9944e-132">Specifies the failover direction.</span></span>
<span data-ttu-id="9944e-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9944e-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9944e-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="9944e-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="9944e-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="9944e-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="9944e-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9944e-136">-RecoveryPlan</span></span>
<span data-ttu-id="9944e-137">Specifica un oggetto piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="9944e-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="9944e-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9944e-138">-RecoveryPoint</span></span>
<span data-ttu-id="9944e-139">Specifica un punto di ripristino personalizzato per testare il failover del computer protetto.</span><span class="sxs-lookup"><span data-stu-id="9944e-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="9944e-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="9944e-140">-RecoveryTag</span></span>
<span data-ttu-id="9944e-141">Specifica il tag di recupero per testare il failover in</span><span class="sxs-lookup"><span data-stu-id="9944e-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="9944e-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9944e-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9944e-143">Specifica un elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="9944e-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="9944e-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="9944e-144">-VMNetwork</span></span>
<span data-ttu-id="9944e-145">Specifica la rete della macchina virtuale di ripristino del sito per connettere le macchine virtuali di failover di test a.</span><span class="sxs-lookup"><span data-stu-id="9944e-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="9944e-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9944e-146">-Confirm</span></span>
<span data-ttu-id="9944e-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9944e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9944e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9944e-148">-WhatIf</span></span>
<span data-ttu-id="9944e-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9944e-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9944e-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9944e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9944e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9944e-151">CommonParameters</span></span>
<span data-ttu-id="9944e-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9944e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9944e-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9944e-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9944e-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9944e-154">INPUTS</span></span>

### <span data-ttu-id="9944e-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9944e-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="9944e-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9944e-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9944e-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9944e-157">OUTPUTS</span></span>

### <span data-ttu-id="9944e-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9944e-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9944e-159">Note</span><span class="sxs-lookup"><span data-stu-id="9944e-159">NOTES</span></span>

## <span data-ttu-id="9944e-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9944e-160">RELATED LINKS</span></span>

[<span data-ttu-id="9944e-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9944e-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
