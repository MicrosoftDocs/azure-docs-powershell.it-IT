---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192823"
---
# <span data-ttu-id="1d261-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="1d261-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="1d261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d261-102">SYNOPSIS</span></span>
<span data-ttu-id="1d261-103">Avvia un'operazione di failover del test.</span><span class="sxs-lookup"><span data-stu-id="1d261-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="1d261-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d261-104">SYNTAX</span></span>

### <span data-ttu-id="1d261-105">ByRPIObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d261-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d261-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1d261-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d261-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="1d261-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d261-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="1d261-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d261-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="1d261-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d261-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="1d261-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d261-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1d261-111">DESCRIPTION</span></span>
<span data-ttu-id="1d261-112">Il cmdlet **Start-AzRecoveryServicesAsrTestFailoverJob** avvia il failover di test di un elemento o di un piano di ripristino protetto da replica di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1d261-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="1d261-113">È possibile verificare l'esito positivo del processo usando il cmdlet Get-AzRecoveryServicesAsrJob processo.</span><span class="sxs-lookup"><span data-stu-id="1d261-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="1d261-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d261-114">EXAMPLES</span></span>

### <span data-ttu-id="1d261-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d261-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="1d261-116">Avvia l'operazione di failover del test per il piano di ripristino con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1d261-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="1d261-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1d261-117">Example 2</span></span>

<span data-ttu-id="1d261-118">Avvia un'operazione di failover del test.</span><span class="sxs-lookup"><span data-stu-id="1d261-118">Starts a test failover operation.</span></span> <span data-ttu-id="1d261-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="1d261-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="1d261-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d261-120">PARAMETERS</span></span>

### <span data-ttu-id="1d261-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="1d261-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="1d261-122">Specifica l'ID di rete della macchina virtuale di Azure per la macchina virtuale di ripristino dopo il failover.</span><span class="sxs-lookup"><span data-stu-id="1d261-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="1d261-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="1d261-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="1d261-124">Specifica se deve essere creato un nuovo servizio cloud o se il servizio cloud di ripristino configurato per la macchina virtuale deve essere usato per il failover del test.</span><span class="sxs-lookup"><span data-stu-id="1d261-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="1d261-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1d261-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1d261-126">Specifica il file del certificato principale.</span><span class="sxs-lookup"><span data-stu-id="1d261-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="1d261-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1d261-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1d261-128">Specifica il file di certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="1d261-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="1d261-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d261-129">-DefaultProfile</span></span>
<span data-ttu-id="1d261-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d261-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1d261-131">-Direction</span><span class="sxs-lookup"><span data-stu-id="1d261-131">-Direction</span></span>
<span data-ttu-id="1d261-132">Specifica la direzione di failover.</span><span class="sxs-lookup"><span data-stu-id="1d261-132">Specifies the failover direction.</span></span>
<span data-ttu-id="1d261-133">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="1d261-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d261-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1d261-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="1d261-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1d261-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="1d261-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1d261-136">-RecoveryPlan</span></span>
<span data-ttu-id="1d261-137">Specifica un oggetto del piano di ripristino a matrice.</span><span class="sxs-lookup"><span data-stu-id="1d261-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="1d261-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1d261-138">-RecoveryPoint</span></span>
<span data-ttu-id="1d261-139">Specifica un punto di ripristino personalizzato per testare il failover del computer protetto.</span><span class="sxs-lookup"><span data-stu-id="1d261-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="1d261-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="1d261-140">-RecoveryTag</span></span>
<span data-ttu-id="1d261-141">Specifica il tag di ripristino su cui testare il failover</span><span class="sxs-lookup"><span data-stu-id="1d261-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="1d261-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1d261-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1d261-143">Specifica un elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="1d261-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="1d261-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="1d261-144">-VMNetwork</span></span>
<span data-ttu-id="1d261-145">Specifica la rete delle macchine virtuali di Ripristino siti a cui connettere le macchine virtuali di failover di test.</span><span class="sxs-lookup"><span data-stu-id="1d261-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="1d261-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d261-146">-Confirm</span></span>
<span data-ttu-id="1d261-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d261-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d261-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d261-148">-WhatIf</span></span>
<span data-ttu-id="1d261-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d261-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d261-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d261-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d261-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d261-151">CommonParameters</span></span>
<span data-ttu-id="1d261-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d261-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d261-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d261-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d261-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="1d261-154">INPUTS</span></span>

### <span data-ttu-id="1d261-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1d261-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="1d261-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1d261-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1d261-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d261-157">OUTPUTS</span></span>

### <span data-ttu-id="1d261-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="1d261-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1d261-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="1d261-159">NOTES</span></span>

## <span data-ttu-id="1d261-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d261-160">RELATED LINKS</span></span>

[<span data-ttu-id="1d261-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1d261-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
