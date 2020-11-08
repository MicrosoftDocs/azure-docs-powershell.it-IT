---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 870EE77E-57D9-4B52-9F80-CB24D642E6E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f94d95b40fb89f0c1df89ad0c8a9b78eb283184
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029862"
---
# <span data-ttu-id="874a6-101">Update-AzureSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="874a6-101">Update-AzureSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="874a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="874a6-102">SYNOPSIS</span></span>
<span data-ttu-id="874a6-103">Aggiorna il server di origine e di destinazione per la protezione di un oggetto di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="874a6-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

## <span data-ttu-id="874a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="874a6-104">SYNTAX</span></span>

### <span data-ttu-id="874a6-105">ByRPObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="874a6-105">ByRPObject (Default)</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="874a6-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="874a6-106">ByRPId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="874a6-107">ByPEId</span><span class="sxs-lookup"><span data-stu-id="874a6-107">ByPEId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="874a6-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="874a6-108">ByPEObject</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="874a6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="874a6-109">DESCRIPTION</span></span>
<span data-ttu-id="874a6-110">Il cmdlet **Update-AzureSiteRecoveryProtectionDirection** aggiorna il server di origine e di destinazione per la protezione di un oggetto di ripristino di un sito di Azure dopo il completamento di un'operazione di failover del commit.</span><span class="sxs-lookup"><span data-stu-id="874a6-110">The **Update-AzureSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after a commit failover operation finishes.</span></span>

## <span data-ttu-id="874a6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="874a6-111">EXAMPLES</span></span>

### <span data-ttu-id="874a6-112">Esempio 1: modificare la direzione di un oggetto protetto in un contenitore</span><span class="sxs-lookup"><span data-stu-id="874a6-112">Example 1: Modify the direction for a protected object in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container  
PS C:\> Update-AzureSiteRecoveryProtectionDirection -Direction RecoveryToPrimary -ProtectionEntity $Protected 
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

<span data-ttu-id="874a6-113">Il primo comando consente di ottenere i contenitori protetti nel Vault di ripristino del sito di Azure corrente usando il cmdlet **Get-AzureSiteRecoveryProtectionContainer** e quindi di archiviarlo nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="874a6-113">The first command gets the protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="874a6-114">Il secondo comando ottiene le macchine virtuali che appartengono al contenitore archiviato in $Container usando il cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="874a6-114">The second command gets the virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="874a6-115">Il comando Archivia i risultati nella variabile $Protected.</span><span class="sxs-lookup"><span data-stu-id="874a6-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="874a6-116">Il comando Final imposta la direzione su RecoverToPrimary per gli oggetti archiviati in $Protected.</span><span class="sxs-lookup"><span data-stu-id="874a6-116">The final command sets the direction to RecoverToPrimary for the objects stored in $Protected.</span></span>

## <span data-ttu-id="874a6-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="874a6-117">PARAMETERS</span></span>

### <span data-ttu-id="874a6-118">-Direzione</span><span class="sxs-lookup"><span data-stu-id="874a6-118">-Direction</span></span>
<span data-ttu-id="874a6-119">Specifica la direzione del commit.</span><span class="sxs-lookup"><span data-stu-id="874a6-119">Specifies the direction of the commit.</span></span>
<span data-ttu-id="874a6-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="874a6-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="874a6-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="874a6-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="874a6-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="874a6-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="874a6-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="874a6-123">-Profile</span></span>
<span data-ttu-id="874a6-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="874a6-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="874a6-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="874a6-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="874a6-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="874a6-126">-ProtectionContainerId</span></span>
<span data-ttu-id="874a6-127">Specifica l'ID di un contenitore protetto.</span><span class="sxs-lookup"><span data-stu-id="874a6-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="874a6-128">Questo cmdlet modifica la direzione per una macchina virtuale protetta che appartiene al contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="874a6-128">This cmdlet modifies the direction for a protected virtual machine that belongs to the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="874a6-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="874a6-129">-ProtectionEntity</span></span>
<span data-ttu-id="874a6-130">Specifica l'oggetto entità di protezione.</span><span class="sxs-lookup"><span data-stu-id="874a6-130">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="874a6-131">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="874a6-131">-ProtectionEntityId</span></span>
<span data-ttu-id="874a6-132">Specifica l'ID di una macchina virtuale protetta.</span><span class="sxs-lookup"><span data-stu-id="874a6-132">Specifies the ID of a protected virtual machine.</span></span>
<span data-ttu-id="874a6-133">Questo cmdlet modifica la direzione per la macchina virtuale protetta specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="874a6-133">This cmdlet modifies the direction for the protected virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="874a6-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="874a6-134">-RecoveryPlan</span></span>
<span data-ttu-id="874a6-135">Specifica un oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="874a6-135">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="874a6-136">-RPId</span><span class="sxs-lookup"><span data-stu-id="874a6-136">-RPId</span></span>
<span data-ttu-id="874a6-137">Specifica l'ID di un piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="874a6-137">Specifies the ID of a recovery plan.</span></span>
<span data-ttu-id="874a6-138">Questo cmdlet modifica la direzione per il piano di ripristino specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="874a6-138">This cmdlet modifies the direction for the recovery plan that this parameter specifies.</span></span>

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

### <span data-ttu-id="874a6-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="874a6-139">-WaitForCompletion</span></span>
<span data-ttu-id="874a6-140">Indica che il cmdlet attende il completamento dell'operazione prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="874a6-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="874a6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="874a6-141">CommonParameters</span></span>
<span data-ttu-id="874a6-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="874a6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="874a6-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="874a6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="874a6-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="874a6-144">INPUTS</span></span>

## <span data-ttu-id="874a6-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="874a6-145">OUTPUTS</span></span>

## <span data-ttu-id="874a6-146">Note</span><span class="sxs-lookup"><span data-stu-id="874a6-146">NOTES</span></span>

## <span data-ttu-id="874a6-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="874a6-147">RELATED LINKS</span></span>

[<span data-ttu-id="874a6-148">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="874a6-148">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="874a6-149">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="874a6-149">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


