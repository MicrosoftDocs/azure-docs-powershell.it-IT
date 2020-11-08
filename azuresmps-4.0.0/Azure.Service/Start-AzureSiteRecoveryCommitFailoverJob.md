---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 44A22B6C-5FD4-43B0-9726-71E28AE53E9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: de1b7a24c1af362297319d0297ce356b00ef9d49
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023736"
---
# <span data-ttu-id="c23b4-101">Start-AzureSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="c23b4-101">Start-AzureSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="c23b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c23b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c23b4-103">Avvia l'azione di failover commit per un oggetto di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="c23b4-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="c23b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c23b4-104">SYNTAX</span></span>

### <span data-ttu-id="c23b4-105">ByRPId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c23b4-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RPId <String> [-Direction <String>] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c23b4-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="c23b4-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 [-Direction <String>] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c23b4-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c23b4-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c23b4-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="c23b4-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c23b4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c23b4-109">DESCRIPTION</span></span>
<span data-ttu-id="c23b4-110">Il cmdlet **Start-AzureSiteRecoveryCommitFailoverJob** avvia il processo di failover di commit per un oggetto di ripristino del sito di Azure dopo un'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="c23b4-110">The **Start-AzureSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="c23b4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c23b4-111">EXAMPLES</span></span>

### <span data-ttu-id="c23b4-112">Esempio 1: avviare un processo di failover del commit</span><span class="sxs-lookup"><span data-stu-id="c23b4-112">Example 1: Start a commit failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity $Protected
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

<span data-ttu-id="c23b4-113">Il primo comando recupera tutti i contenitori protetti per il Vault di ripristino di Azure corrente usando il cmdlet **Get-AzureSiteRecoveryProtectionContainer** e quindi archivia i risultati nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="c23b4-113">The first command gets all protected containers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>

<span data-ttu-id="c23b4-114">Il secondo comando ottiene le macchine virtuali protette che appartengono al contenitore archiviato in $Container usando il cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="c23b4-114">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="c23b4-115">Il comando Archivia i risultati nella variabile $Protected.</span><span class="sxs-lookup"><span data-stu-id="c23b4-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="c23b4-116">Il comando finale avvia il processo di failover per gli oggetti protetti archiviati in $Protected.</span><span class="sxs-lookup"><span data-stu-id="c23b4-116">The final command starts the failover job for the protected objects stored in $Protected.</span></span>

## <span data-ttu-id="c23b4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c23b4-117">PARAMETERS</span></span>

### <span data-ttu-id="c23b4-118">-Direzione</span><span class="sxs-lookup"><span data-stu-id="c23b4-118">-Direction</span></span>
<span data-ttu-id="c23b4-119">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="c23b4-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="c23b4-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c23b4-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c23b4-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="c23b4-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="c23b4-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="c23b4-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="c23b4-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="c23b4-123">-Profile</span></span>
<span data-ttu-id="c23b4-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c23b4-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c23b4-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c23b4-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c23b4-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="c23b4-126">-ProtectionContainerId</span></span>
<span data-ttu-id="c23b4-127">Specifica l'ID di un contenitore protetto.</span><span class="sxs-lookup"><span data-stu-id="c23b4-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="c23b4-128">Questo cmdlet avvia il processo per una macchina virtuale protetta che appartiene al contenitore specificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c23b4-128">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="c23b4-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c23b4-129">-ProtectionEntity</span></span>
<span data-ttu-id="c23b4-130">Specifica un oggetto **ASRProtectionEntity** per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="c23b4-130">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="c23b4-131">Per ottenere un oggetto **ASRProtectionEntity** , usa il cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="c23b4-131">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

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

### <span data-ttu-id="c23b4-132">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="c23b4-132">-ProtectionEntityId</span></span>
<span data-ttu-id="c23b4-133">Specifica l'ID di una macchina virtuale protetta per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="c23b4-133">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="c23b4-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c23b4-134">-RecoveryPlan</span></span>
<span data-ttu-id="c23b4-135">Specifica un oggetto piano di ripristino per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="c23b4-135">Specifies a recovery plan object for which to start the job.</span></span>
<span data-ttu-id="c23b4-136">Per ottenere un oggetto **ASRRecoveryPlan** , usa il cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="c23b4-136">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="c23b4-137">-RPId</span><span class="sxs-lookup"><span data-stu-id="c23b4-137">-RPId</span></span>
<span data-ttu-id="c23b4-138">Specifica l'ID di un piano di ripristino per cui avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="c23b4-138">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="c23b4-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="c23b4-139">-WaitForCompletion</span></span>
<span data-ttu-id="c23b4-140">Indica che il cmdlet attende il completamento dell'operazione prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c23b4-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="c23b4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c23b4-141">CommonParameters</span></span>
<span data-ttu-id="c23b4-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c23b4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c23b4-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c23b4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c23b4-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c23b4-144">INPUTS</span></span>

## <span data-ttu-id="c23b4-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c23b4-145">OUTPUTS</span></span>

## <span data-ttu-id="c23b4-146">Note</span><span class="sxs-lookup"><span data-stu-id="c23b4-146">NOTES</span></span>

## <span data-ttu-id="c23b4-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c23b4-147">RELATED LINKS</span></span>

[<span data-ttu-id="c23b4-148">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c23b4-148">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="c23b4-149">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c23b4-149">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="c23b4-150">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c23b4-150">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


