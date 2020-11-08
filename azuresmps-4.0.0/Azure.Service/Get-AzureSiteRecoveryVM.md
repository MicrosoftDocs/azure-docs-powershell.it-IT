---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CE15E01D-5D86-4960-8E37-7757B35F4464
online version: ''
schema: 2.0.0
ms.openlocfilehash: a87a825249d7d7cda3fc2dc43a93869f8d869705
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030031"
---
# <span data-ttu-id="73e61-101">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="73e61-101">Get-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="73e61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73e61-102">SYNOPSIS</span></span>
<span data-ttu-id="73e61-103">Ottiene informazioni sulle macchine virtuali gestite dal ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="73e61-103">Gets information about Site Recovery-managed virtual machines.</span></span>

## <span data-ttu-id="73e61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73e61-104">SYNTAX</span></span>

### <span data-ttu-id="73e61-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73e61-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="73e61-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="73e61-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="73e61-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="73e61-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="73e61-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="73e61-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="73e61-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="73e61-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="73e61-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="73e61-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainerId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="73e61-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73e61-111">DESCRIPTION</span></span>
<span data-ttu-id="73e61-112">Il cmdlet **Get-AzureSiteRecoveryVM** ottiene informazioni sulle macchine virtuali gestite in Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="73e61-112">The **Get-AzureSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="73e61-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73e61-113">EXAMPLES</span></span>

### <span data-ttu-id="73e61-114">Esempio 1: ottenere informazioni su una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="73e61-114">Example 1: Get information about a virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer
ID                          : a205fd17-3848-4896-bab6-9dbccc3cd8ed
ServerId                    : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId       : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                        : vm1
Type                        : VirtualMachine
FabricObjectId              : 86447b9e-d877-4e9a-8302-adcd6bbf18c0
Protected                   : False
CanCommit                   : False
CanFailover                 : True
CanReverseReplicate         : False
ActiveLocation              : Primary
ProtectionState             : Enabled
ReplicationHealth           : Healthy
TestFailoverState           : None
ReplicationProvider         : HyperVReplica
```

<span data-ttu-id="73e61-115">Il primo comando usa il cmdlet **Get-AzureSiteRecoveryProtectionContainer** per ottenere un contenitore protetto e lo archivia nella variabile $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="73e61-115">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="73e61-116">Il secondo comando recupera le informazioni sulle macchine virtuali in $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="73e61-116">The second command gets information about the virtual machines in $ProtectionContainer.</span></span>

## <span data-ttu-id="73e61-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73e61-117">PARAMETERS</span></span>

### <span data-ttu-id="73e61-118">-ID</span><span class="sxs-lookup"><span data-stu-id="73e61-118">-Id</span></span>
<span data-ttu-id="73e61-119">Specifica l'ID della macchina virtuale che consente di ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="73e61-119">Specifies the ID of the virtual machine about which to get information.</span></span>

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

### <span data-ttu-id="73e61-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="73e61-120">-Name</span></span>
<span data-ttu-id="73e61-121">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="73e61-121">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="73e61-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="73e61-122">-Profile</span></span>
<span data-ttu-id="73e61-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73e61-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73e61-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="73e61-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73e61-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="73e61-125">-ProtectionContainer</span></span>
<span data-ttu-id="73e61-126">Specifica l'oggetto contenitore di protezione per il ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="73e61-126">Specifies the Site Recovery protection container object.</span></span>

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

### <span data-ttu-id="73e61-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="73e61-127">-ProtectionContainerId</span></span>
<span data-ttu-id="73e61-128">Specifica l'ID di un contenitore protetto per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="73e61-128">Specifies the ID of a protected container about which to get information.</span></span>

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

### <span data-ttu-id="73e61-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e61-129">CommonParameters</span></span>
<span data-ttu-id="73e61-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73e61-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e61-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73e61-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e61-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73e61-132">INPUTS</span></span>

## <span data-ttu-id="73e61-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73e61-133">OUTPUTS</span></span>

## <span data-ttu-id="73e61-134">Note</span><span class="sxs-lookup"><span data-stu-id="73e61-134">NOTES</span></span>

## <span data-ttu-id="73e61-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73e61-135">RELATED LINKS</span></span>

[<span data-ttu-id="73e61-136">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="73e61-136">Set-AzureSiteRecoveryVM</span></span>](./Set-AzureSiteRecoveryVM.md)


