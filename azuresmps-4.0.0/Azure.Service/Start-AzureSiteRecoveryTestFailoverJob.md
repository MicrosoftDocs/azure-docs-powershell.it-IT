---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 9AE41884-C39F-4AEB-8030-96167F98C8DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b46cc27b2e5380f3cb533a4355a94170e941cd8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029490"
---
# <span data-ttu-id="49913-101">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="49913-101">Start-AzureSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="49913-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49913-102">SYNOPSIS</span></span>
<span data-ttu-id="49913-103">Avvia un failover di test per un'entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="49913-103">Starts a test failover for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="49913-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49913-104">SYNTAX</span></span>

### <span data-ttu-id="49913-105">ByPEId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49913-105">ByPEId (Default)</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="49913-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="49913-106">ByRPId</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49913-107">ByRPIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="49913-107">ByRPIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="49913-108">ByRPIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="49913-108">ByRPIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="49913-109">ByRPIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="49913-109">ByRPIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> -Network <ASRNetwork> [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49913-110">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="49913-110">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49913-111">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="49913-111">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="49913-112">ByPEIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="49913-112">ByPEIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="49913-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="49913-113">ByRPObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="49913-114">ByRPObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="49913-114">ByRPObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49913-115">ByRPObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="49913-115">ByRPObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49913-116">ByPEIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="49913-116">ByPEIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49913-117">ByPEIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="49913-117">ByPEIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49913-118">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="49913-118">ByPEObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49913-119">ByPEObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="49913-119">ByPEObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49913-120">ByPEObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="49913-120">ByPEObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="49913-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49913-121">DESCRIPTION</span></span>
<span data-ttu-id="49913-122">Il cmdlet **Start-AzureSiteRecoveryTestFailoverJob** avvia il failover dei test di un'entità o un piano di ripristino di un sito di Azure Protection.</span><span class="sxs-lookup"><span data-stu-id="49913-122">The **Start-AzureSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="49913-123">Puoi verificare se il processo è riuscito usando il cmdlet **Get-AzureRMSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="49913-123">You can check whether the job succeeded by using the **Get-AzureRMSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="49913-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49913-124">EXAMPLES</span></span>

### <span data-ttu-id="49913-125">Esempio 1: avviare un failover di test</span><span class="sxs-lookup"><span data-stu-id="49913-125">Example 1: Start a test failover</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer
PS C:\> Start-AzureSiteRecoveryTestFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="49913-126">Il primo comando usa il cmdlet **Get-AzureSiteRecoveryProtectionContainer** per ottenere un contenitore protetto e lo archivia nella variabile $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="49913-126">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="49913-127">Il secondo comando ottiene le entità protette che appartengono al contenitore protetto archiviato in $ProtectionContainer usando il cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="49913-127">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="49913-128">Il comando Archivia i risultati nella variabile $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="49913-128">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="49913-129">Il comando finale avvia l'operazione di failover del test per le entità protette archiviate in $ProtectionEntity e specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="49913-129">The final command starts the test failover operation for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

### <span data-ttu-id="49913-130">Esempio 2: avviare un failover di test con un piano di ripristino</span><span class="sxs-lookup"><span data-stu-id="49913-130">Example 2: Start a test failover using a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan -Name "RecoveryPlan01"
Start-AzureSiteRecoveryTestFailoverJob -Direction PrimaryToRecovery -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="49913-131">Questo comando ottiene il piano di ripristino denominato RecoveryPlan01 per il Vault di ripristino del sito di Azure corrente usando il cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="49913-131">This command gets the recovery plan named RecoveryPlan01 for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>
<span data-ttu-id="49913-132">Il comando Archivia il piano nella variabile $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="49913-132">The command stores the plan in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="49913-133">Il secondo comando avvia l'operazione di failover del test per il piano di ripristino archiviato in $RecoveryPlan e specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="49913-133">The second command starts the test failover operation for the recovery plan stored in $RecoveryPlan and specifies the direction of the failover.</span></span>

## <span data-ttu-id="49913-134">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49913-134">PARAMETERS</span></span>

### <span data-ttu-id="49913-135">-Direzione</span><span class="sxs-lookup"><span data-stu-id="49913-135">-Direction</span></span>
<span data-ttu-id="49913-136">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="49913-136">Specifies the failover direction.</span></span>
<span data-ttu-id="49913-137">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="49913-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49913-138">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="49913-138">PrimaryToRecovery</span></span>
- <span data-ttu-id="49913-139">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="49913-139">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="49913-140">-LogicalNetworkId</span><span class="sxs-lookup"><span data-stu-id="49913-140">-LogicalNetworkId</span></span>
<span data-ttu-id="49913-141">Specifica l'ID della rete logica.</span><span class="sxs-lookup"><span data-stu-id="49913-141">Specifies the ID of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithLogicalNetworkID, ByRPObjectWithLogicalNetworkID, ByPEIdWithLogicalNetworkID, ByPEObjectWithLogicalNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49913-142">-Rete</span><span class="sxs-lookup"><span data-stu-id="49913-142">-Network</span></span>
<span data-ttu-id="49913-143">Specifica l'oggetto Network da usare per il failover dei test.</span><span class="sxs-lookup"><span data-stu-id="49913-143">Specifies the network object to use for test failover.</span></span>
<span data-ttu-id="49913-144">Per ottenere una rete, usare il cmdlet **Get-AzureSiteRecoveryNetwork** .</span><span class="sxs-lookup"><span data-stu-id="49913-144">To obtain a network, use the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByPEId, ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPObject, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID, ByPEObject, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRNetwork
Parameter Sets: ByRPIdWithVMNetwork, ByPEObjectWithVMNetwork, ByRPObjectWithVMNetwork, ByPEIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49913-145">-NetworkType</span><span class="sxs-lookup"><span data-stu-id="49913-145">-NetworkType</span></span>
<span data-ttu-id="49913-146">Specifica il tipo di rete da usare per il failover dei test.</span><span class="sxs-lookup"><span data-stu-id="49913-146">Specifies the network type to use for test failover.</span></span>
<span data-ttu-id="49913-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="49913-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49913-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="49913-148">None</span></span>
- <span data-ttu-id="49913-149">Nuovo</span><span class="sxs-lookup"><span data-stu-id="49913-149">New</span></span>
- <span data-ttu-id="49913-150">Esistente</span><span class="sxs-lookup"><span data-stu-id="49913-150">Existing</span></span>

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

### <span data-ttu-id="49913-151">-Profile</span><span class="sxs-lookup"><span data-stu-id="49913-151">-Profile</span></span>
<span data-ttu-id="49913-152">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49913-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49913-153">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="49913-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49913-154">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="49913-154">-ProtectionContainerId</span></span>
<span data-ttu-id="49913-155">Specifica l'ID di un contenitore protetto.</span><span class="sxs-lookup"><span data-stu-id="49913-155">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="49913-156">Questo cmdlet avvia il processo per una macchina virtuale protetta che appartiene al contenitore specificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49913-156">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49913-157">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="49913-157">-ProtectionEntity</span></span>
<span data-ttu-id="49913-158">Specifica l'oggetto entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="49913-158">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObjectWithVMNetwork, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49913-159">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="49913-159">-ProtectionEntityId</span></span>
<span data-ttu-id="49913-160">Specifica l'ID di una macchina virtuale protetta per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="49913-160">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49913-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49913-161">-RecoveryPlan</span></span>
<span data-ttu-id="49913-162">Specifica un piano di ripristino per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="49913-162">Specifies a recovery plan for which to start the job.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObjectWithVMNetwork, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49913-163">-RpId</span><span class="sxs-lookup"><span data-stu-id="49913-163">-RpId</span></span>
<span data-ttu-id="49913-164">Specifica l'ID di un piano di ripristino per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="49913-164">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49913-165">-VmNetworkId</span><span class="sxs-lookup"><span data-stu-id="49913-165">-VmNetworkId</span></span>
<span data-ttu-id="49913-166">Specifica l'ID della rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="49913-166">Specifies the ID of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithVMNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithVMNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49913-167">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="49913-167">-WaitForCompletion</span></span>
<span data-ttu-id="49913-168">Indica che il cmdlet attende il completamento dell'operazione prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="49913-168">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="49913-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49913-169">CommonParameters</span></span>
<span data-ttu-id="49913-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49913-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49913-171">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49913-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49913-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49913-172">INPUTS</span></span>

## <span data-ttu-id="49913-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49913-173">OUTPUTS</span></span>

## <span data-ttu-id="49913-174">Note</span><span class="sxs-lookup"><span data-stu-id="49913-174">NOTES</span></span>

## <span data-ttu-id="49913-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49913-175">RELATED LINKS</span></span>

[<span data-ttu-id="49913-176">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="49913-176">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="49913-177">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="49913-177">Get-AzureSiteRecoveryNetwork</span></span>](./Get-AzureSiteRecoveryNetwork.md)

[<span data-ttu-id="49913-178">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="49913-178">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="49913-179">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49913-179">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="49913-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="49913-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>](./Start-AzureSiteRecoveryUnplannedFailoverJob.md)


