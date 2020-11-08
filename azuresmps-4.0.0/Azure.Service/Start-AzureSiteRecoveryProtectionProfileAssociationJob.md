---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB5E1419-C4C7-4524-ACCC-13C9D9CCA621
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4955bfa121d6742903dd2ca99721186c7c860004
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023806"
---
# <span data-ttu-id="c2e95-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="c2e95-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>

## <span data-ttu-id="c2e95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2e95-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e95-103">Avvia un processo di associazione dei criteri di replica del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="c2e95-103">Starts a Site Recovery replication policy association job.</span></span>

## <span data-ttu-id="c2e95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2e95-104">SYNTAX</span></span>

### <span data-ttu-id="c2e95-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2e95-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c2e95-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c2e95-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c2e95-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2e95-107">DESCRIPTION</span></span>
<span data-ttu-id="c2e95-108">Il cmdlet **Start-AzureSiteRecoveryProtectionProfileAssociationJob** avvia un processo di associazione per associare un criterio di replica con un contenitore di protezione per il ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="c2e95-108">The **Start-AzureSiteRecoveryProtectionProfileAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="c2e95-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2e95-109">EXAMPLES</span></span>

### <span data-ttu-id="c2e95-110">Esempio 1: associare un profilo di protezione</span><span class="sxs-lookup"><span data-stu-id="c2e95-110">Example 1: Associate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionProfile = New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileAssociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionProfile -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-27 22:55:55Z-P
State            : InProgress
StateDescription : InProgress
StartTime        : 1/27/2015 10:56:01 PM
EndTime          : 
AllowedActions   : 
Tasks            : {Adding the protection group, Configuring Windows Server 2012 R2 Hyper-V hosts for Azure}
Errors           : {}
```

<span data-ttu-id="c2e95-111">Il primo comando ottiene un contenitore di protezione usando il cmdlet **Get-AzureSiteRecoveryProtectionContainer** e quindi archivia tale contenitore nella variabile $ProtectionContainer 01.</span><span class="sxs-lookup"><span data-stu-id="c2e95-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="c2e95-112">Il secondo comando crea un profilo di protezione usando il cmdlet **New-AzureSiteRecoveryProtectionProfileObject** e archivia il profilo di protezione nella variabile $ProtectionProfile.</span><span class="sxs-lookup"><span data-stu-id="c2e95-112">The second command creates a protection profile by using the **New-AzureSiteRecoveryProtectionProfileObject** cmdlet, and stores that protection profile in the $ProtectionProfile variable.</span></span>

<span data-ttu-id="c2e95-113">Il terzo comando ottiene un contenitore di protezione e lo archivia nella variabile $ProtectionContainer 02.</span><span class="sxs-lookup"><span data-stu-id="c2e95-113">The third command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="c2e95-114">Il comando finale associa il profilo di protezione archiviato in $ProtectionProfile al contenitore archiviato in $ProtectionContainer 01 come contenitore di protezione principale.</span><span class="sxs-lookup"><span data-stu-id="c2e95-114">The final command associates the protection profile stored in $ProtectionProfile to the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="c2e95-115">Il comando associa il contenitore archiviato in $ProtectionContainer 02 come contenitore di protezione del ripristino.</span><span class="sxs-lookup"><span data-stu-id="c2e95-115">The command associates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="c2e95-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2e95-116">PARAMETERS</span></span>

### <span data-ttu-id="c2e95-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c2e95-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="c2e95-118">Specifica il contenitore di protezione principale in cui applicare le impostazioni del profilo di protezione.</span><span class="sxs-lookup"><span data-stu-id="c2e95-118">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e95-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="c2e95-119">-Profile</span></span>
<span data-ttu-id="c2e95-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e95-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c2e95-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c2e95-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c2e95-122">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="c2e95-122">-ProtectionProfile</span></span>
<span data-ttu-id="c2e95-123">Specifica le impostazioni del profilo di protezione da applicare ai contenitori di protezione.</span><span class="sxs-lookup"><span data-stu-id="c2e95-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="c2e95-124">Per ottenere un oggetto **ASRProtectionProfile** , usa il cmdlet New-AzureSiteRecoveryProtectionProfileObject.</span><span class="sxs-lookup"><span data-stu-id="c2e95-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e95-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c2e95-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="c2e95-126">Specifica il contenitore di protezione per il recupero in cui applicare le impostazioni del profilo di protezione.</span><span class="sxs-lookup"><span data-stu-id="c2e95-126">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e95-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e95-127">CommonParameters</span></span>
<span data-ttu-id="c2e95-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2e95-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e95-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2e95-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e95-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2e95-130">INPUTS</span></span>

## <span data-ttu-id="c2e95-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2e95-131">OUTPUTS</span></span>

## <span data-ttu-id="c2e95-132">Note</span><span class="sxs-lookup"><span data-stu-id="c2e95-132">NOTES</span></span>

## <span data-ttu-id="c2e95-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2e95-133">RELATED LINKS</span></span>

[<span data-ttu-id="c2e95-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c2e95-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="c2e95-135">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="c2e95-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="c2e95-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="c2e95-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileDissociationJob.md)


