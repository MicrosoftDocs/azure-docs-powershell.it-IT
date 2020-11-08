---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB1A36E9-75BE-43CF-9092-9713DFEB96F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5329d50f87b92254136c222f406bb49586d6d7a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023546"
---
# <span data-ttu-id="20a07-101">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="20a07-101">Get-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="20a07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20a07-102">SYNOPSIS</span></span>
<span data-ttu-id="20a07-103">Ottiene entità protettive o protette in un Vault di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="20a07-103">Gets protectable or protected entities in a Site Recovery vault.</span></span>

## <span data-ttu-id="20a07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20a07-104">SYNTAX</span></span>

### <span data-ttu-id="20a07-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20a07-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="20a07-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="20a07-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="20a07-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="20a07-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="20a07-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="20a07-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="20a07-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="20a07-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainerId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="20a07-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="20a07-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="20a07-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20a07-111">DESCRIPTION</span></span>
<span data-ttu-id="20a07-112">Il cmdlet **Get-AzureSiteRecoveryProtectionEntity** consente di ottenere le entità protetti o protette, ad esempio le macchine virtuali, nell'archivio di ripristino del sito di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="20a07-112">The **Get-AzureSiteRecoveryProtectionEntity** cmdlet gets the protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="20a07-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20a07-113">EXAMPLES</span></span>

### <span data-ttu-id="20a07-114">Esempio 1: visualizzare una macchina virtuale protetta in un contenitore</span><span class="sxs-lookup"><span data-stu-id="20a07-114">Example 1: Display a protected virtual machine in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
ID                           : 43aaab46-1cb0-4c39-8077-9a091c3b05ce
ServerId                     : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId        : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                         : testvm
Type                         : VirtualMachine
FabricObjectId               : 506B3CAC-5758-49E2-98C4-E5B0512E4D8E
Protected                    : False
CanCommit                    : False
CanFailover                  : False
CanReverseReplicate          : False
ActiveLocation               : Primary
ProtectionStateDescription   : Enabling protection
ReplicationHealth            : 
TestFailoverStateDescription : Nonev
ReplicationProvider          : HyperVReplica
```

<span data-ttu-id="20a07-115">Il primo comando ottiene un contenitore protetto usando il cmdlet **Get-AzureSiteRecoveryProtectionContainer** e quindi archivia tale oggetto nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="20a07-115">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="20a07-116">Il secondo comando consente di ottenere la macchina virtuale protetta che appartiene al contenitore in $Container e quindi di visualizzarla.</span><span class="sxs-lookup"><span data-stu-id="20a07-116">The second command gets the protected virtual machine that belongs to the container in $Container, and then displays it.</span></span>

## <span data-ttu-id="20a07-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20a07-117">PARAMETERS</span></span>

### <span data-ttu-id="20a07-118">-ID</span><span class="sxs-lookup"><span data-stu-id="20a07-118">-Id</span></span>
<span data-ttu-id="20a07-119">Specifica l'ID di un'entità di protezione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="20a07-119">Specifies the ID of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithId, ByIDsWithId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a07-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="20a07-120">-Name</span></span>
<span data-ttu-id="20a07-121">Specifica il nome di un'entità di protezione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="20a07-121">Specifies the name of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByIDsWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a07-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="20a07-122">-Profile</span></span>
<span data-ttu-id="20a07-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20a07-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20a07-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="20a07-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20a07-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="20a07-125">-ProtectionContainer</span></span>
<span data-ttu-id="20a07-126">Specifica un contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="20a07-126">Specifies a protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithId, ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20a07-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="20a07-127">-ProtectionContainerId</span></span>
<span data-ttu-id="20a07-128">Specifica l'ID di un contenitore protetto.</span><span class="sxs-lookup"><span data-stu-id="20a07-128">Specifies the ID of a protected container.</span></span>

```yaml
Type: String
Parameter Sets: ByIDsWithId, ByIDsWithName, ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a07-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a07-129">CommonParameters</span></span>
<span data-ttu-id="20a07-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a07-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a07-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a07-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a07-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20a07-132">INPUTS</span></span>

## <span data-ttu-id="20a07-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20a07-133">OUTPUTS</span></span>

## <span data-ttu-id="20a07-134">Note</span><span class="sxs-lookup"><span data-stu-id="20a07-134">NOTES</span></span>

## <span data-ttu-id="20a07-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20a07-135">RELATED LINKS</span></span>

[<span data-ttu-id="20a07-136">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="20a07-136">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="20a07-137">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="20a07-137">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="20a07-138">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="20a07-138">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


