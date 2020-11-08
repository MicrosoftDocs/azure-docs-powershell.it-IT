---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029872"
---
# <span data-ttu-id="1a54b-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="1a54b-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>

## <span data-ttu-id="1a54b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a54b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a54b-103">Avvia un processo di dissociazione in un criterio di replica associato a un contenitore di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="1a54b-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

## <span data-ttu-id="1a54b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a54b-104">SYNTAX</span></span>

### <span data-ttu-id="1a54b-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a54b-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1a54b-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="1a54b-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1a54b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a54b-107">DESCRIPTION</span></span>
<span data-ttu-id="1a54b-108">Il cmdlet **Start-AzureSiteRecoveryProtectionProfileDissociationJob** avvia un processo di dissociazione sui criteri di replica associati a un contenitore di protezione del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="1a54b-108">The **Start-AzureSiteRecoveryProtectionProfileDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="1a54b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a54b-109">EXAMPLES</span></span>

### <span data-ttu-id="1a54b-110">Esempio 1: dissociare un profilo di protezione</span><span class="sxs-lookup"><span data-stu-id="1a54b-110">Example 1: Dissociate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="1a54b-111">Il primo comando ottiene un contenitore di protezione usando il cmdlet **Get-AzureSiteRecoveryProtectionContainer** e quindi archivia tale contenitore nella variabile $ProtectionContainer 01.</span><span class="sxs-lookup"><span data-stu-id="1a54b-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="1a54b-112">Il secondo comando ottiene un contenitore di protezione e lo archivia nella variabile $ProtectionContainer 02.</span><span class="sxs-lookup"><span data-stu-id="1a54b-112">The second command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="1a54b-113">Il comando finale dissocia il profilo di protezione dal contenitore archiviato in $ProtectionContainer 01 come contenitore di protezione principale.</span><span class="sxs-lookup"><span data-stu-id="1a54b-113">The final command dissociates the protection profile from the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="1a54b-114">Il comando Dissocia il contenitore archiviato in $ProtectionContainer 02 come contenitore di protezione del ripristino.</span><span class="sxs-lookup"><span data-stu-id="1a54b-114">The command dissociates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="1a54b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a54b-115">PARAMETERS</span></span>

### <span data-ttu-id="1a54b-116">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1a54b-116">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="1a54b-117">Specifica un contenitore di protezione principale.</span><span class="sxs-lookup"><span data-stu-id="1a54b-117">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="1a54b-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="1a54b-118">-Profile</span></span>
<span data-ttu-id="1a54b-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a54b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a54b-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1a54b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a54b-121">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="1a54b-121">-ProtectionProfile</span></span>
<span data-ttu-id="1a54b-122">Specifica le impostazioni del profilo di protezione per la dissociazione dai contenitori di protezione.</span><span class="sxs-lookup"><span data-stu-id="1a54b-122">Specifies the protection profile settings to disassociate from the protection containers.</span></span>
<span data-ttu-id="1a54b-123">Specifica le impostazioni del profilo di protezione da applicare ai contenitori di protezione.</span><span class="sxs-lookup"><span data-stu-id="1a54b-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="1a54b-124">Per ottenere un oggetto **ASRProtectionProfile** , usa il cmdlet New-AzureSiteRecoveryProtectionProfileObject.</span><span class="sxs-lookup"><span data-stu-id="1a54b-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

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

### <span data-ttu-id="1a54b-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1a54b-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="1a54b-126">Specifica un contenitore di protezione per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="1a54b-126">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="1a54b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a54b-127">CommonParameters</span></span>
<span data-ttu-id="1a54b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a54b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a54b-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a54b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a54b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a54b-130">INPUTS</span></span>

## <span data-ttu-id="1a54b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a54b-131">OUTPUTS</span></span>

## <span data-ttu-id="1a54b-132">Note</span><span class="sxs-lookup"><span data-stu-id="1a54b-132">NOTES</span></span>

## <span data-ttu-id="1a54b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a54b-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a54b-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1a54b-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="1a54b-135">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="1a54b-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="1a54b-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="1a54b-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


