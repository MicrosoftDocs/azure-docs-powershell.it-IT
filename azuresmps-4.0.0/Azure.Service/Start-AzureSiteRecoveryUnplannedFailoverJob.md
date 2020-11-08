---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AC73119B-BB76-425B-AA44-44502028ECC4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a74a02f219b5bb64957ab919168cb79ccf681869
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023764"
---
# <span data-ttu-id="0048c-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0048c-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="0048c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0048c-102">SYNOPSIS</span></span>
<span data-ttu-id="0048c-103">Avvia il failover non pianificato per un'entità di protezione del ripristino del sito o un piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0048c-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

## <span data-ttu-id="0048c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0048c-104">SYNTAX</span></span>

### <span data-ttu-id="0048c-105">ByRPId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0048c-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RPId <String> -Direction <String> [-PrimaryAction <Boolean>]
 [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0048c-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="0048c-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0048c-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0048c-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PrimaryAction <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0048c-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="0048c-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0048c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0048c-109">DESCRIPTION</span></span>
<span data-ttu-id="0048c-110">Il cmdlet **Start-AzureSiteRecoveryUnplannedFailoverJob** avvia il failover non pianificato di un'entità o un piano di ripristino di un sito di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="0048c-110">The **Start-AzureSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="0048c-111">Puoi verificare se il processo viene eseguito correttamente usando il cmdlet **Get-AzureSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="0048c-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="0048c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0048c-112">EXAMPLES</span></span>

### <span data-ttu-id="0048c-113">Esempio 1: avviare un processo di failover non pianificato</span><span class="sxs-lookup"><span data-stu-id="0048c-113">Example 1: Start an unplanned failover job</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer 
PS C:\> Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="0048c-114">Il primo comando ottiene un contenitore protetto usando il cmdlet **Get-AzureSiteRecoveryProtectionContainer** e lo archivia nella variabile $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="0048c-114">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="0048c-115">Il secondo comando ottiene le entità protette che appartengono al contenitore protetto archiviato in $ProtectionContainer usando il cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="0048c-115">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="0048c-116">Il comando Archivia i risultati nella variabile $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="0048c-116">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="0048c-117">Il comando finale avvia il failover per le entità protette archiviate in $ProtectionEntity e specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="0048c-117">The final command starts the failover for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

## <span data-ttu-id="0048c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0048c-118">PARAMETERS</span></span>

### <span data-ttu-id="0048c-119">-Direzione</span><span class="sxs-lookup"><span data-stu-id="0048c-119">-Direction</span></span>
<span data-ttu-id="0048c-120">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="0048c-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="0048c-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0048c-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0048c-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0048c-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="0048c-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0048c-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="0048c-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="0048c-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="0048c-125">Indica che l'azione può eseguire azioni Side di origine.</span><span class="sxs-lookup"><span data-stu-id="0048c-125">Indicates that the action can perform source side actions.</span></span>

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

### <span data-ttu-id="0048c-126">-PerformSourceSiteOperations</span><span class="sxs-lookup"><span data-stu-id="0048c-126">-PerformSourceSiteOperations</span></span>
<span data-ttu-id="0048c-127">Indica che le operazioni del sito di origine possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="0048c-127">Indicates that source site operations can be performed.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByPEId, ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0048c-128">-PrimaryAction</span><span class="sxs-lookup"><span data-stu-id="0048c-128">-PrimaryAction</span></span>
<span data-ttu-id="0048c-129">Indica che sono necessarie le azioni del sito principale.</span><span class="sxs-lookup"><span data-stu-id="0048c-129">Indicates that  primary site actions are required.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByRPId, ByRPObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0048c-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="0048c-130">-Profile</span></span>
<span data-ttu-id="0048c-131">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0048c-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0048c-132">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0048c-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0048c-133">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="0048c-133">-ProtectionContainerId</span></span>
<span data-ttu-id="0048c-134">Specifica l'ID di un contenitore protetto.</span><span class="sxs-lookup"><span data-stu-id="0048c-134">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="0048c-135">Questo cmdlet avvia il processo per una macchina virtuale protetta che appartiene al contenitore specificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0048c-135">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0048c-136">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0048c-136">-ProtectionEntity</span></span>
<span data-ttu-id="0048c-137">Specifica l'oggetto entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="0048c-137">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="0048c-138">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="0048c-138">-ProtectionEntityId</span></span>
<span data-ttu-id="0048c-139">Specifica l'ID di una macchina virtuale protetta per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="0048c-139">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0048c-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0048c-140">-RecoveryPlan</span></span>
<span data-ttu-id="0048c-141">Specifica un oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0048c-141">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="0048c-142">-RPId</span><span class="sxs-lookup"><span data-stu-id="0048c-142">-RPId</span></span>
<span data-ttu-id="0048c-143">Specifica l'ID di un piano di ripristino per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="0048c-143">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0048c-144">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="0048c-144">-WaitForCompletion</span></span>
<span data-ttu-id="0048c-145">Indica che il cmdlet attende il completamento dell'operazione prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0048c-145">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="0048c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0048c-146">CommonParameters</span></span>
<span data-ttu-id="0048c-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0048c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0048c-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0048c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0048c-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0048c-149">INPUTS</span></span>

## <span data-ttu-id="0048c-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0048c-150">OUTPUTS</span></span>

## <span data-ttu-id="0048c-151">Note</span><span class="sxs-lookup"><span data-stu-id="0048c-151">NOTES</span></span>

## <span data-ttu-id="0048c-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0048c-152">RELATED LINKS</span></span>

[<span data-ttu-id="0048c-153">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0048c-153">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="0048c-154">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0048c-154">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="0048c-155">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0048c-155">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="0048c-156">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0048c-156">Start-AzureSiteRecoveryTestFailoverJob</span></span>](./Start-AzureSiteRecoveryTestFailoverJob.md)


