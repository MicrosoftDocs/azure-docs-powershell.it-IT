---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: af4dbdbb2741850cdb01eb88e321f80a4844919a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677680"
---
# <span data-ttu-id="89089-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="89089-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="89089-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89089-102">SYNOPSIS</span></span>
<span data-ttu-id="89089-103">Ottiene le proprietà di un elemento protetto della replica del ripristino dei siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="89089-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="89089-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89089-104">SYNTAX</span></span>

### <span data-ttu-id="89089-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89089-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89089-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="89089-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89089-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="89089-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89089-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="89089-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89089-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89089-109">DESCRIPTION</span></span>
<span data-ttu-id="89089-110">Il cmdlet **Get-AzRecoveryServicesAsrReplicationProtectedItem** ottiene le proprietà di tutti gli elementi o dell'elemento protetto della replica ASR specificata dal contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="89089-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="89089-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89089-111">EXAMPLES</span></span>

### <span data-ttu-id="89089-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="89089-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="89089-113">Elenca tutti gli elementi protetti da replica nel contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="89089-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="89089-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89089-114">PARAMETERS</span></span>

### <span data-ttu-id="89089-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89089-115">-DefaultProfile</span></span>
<span data-ttu-id="89089-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89089-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="89089-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="89089-117">-FriendlyName</span></span>
<span data-ttu-id="89089-118">Specifica il nome descrittivo dell'elemento protetto dalla replica da ottenere.</span><span class="sxs-lookup"><span data-stu-id="89089-118">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89089-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="89089-119">-Name</span></span>
<span data-ttu-id="89089-120">Specifica il nome dell'elemento protetto per la replica da ottenere.</span><span class="sxs-lookup"><span data-stu-id="89089-120">Specifies the name of the replication protected item to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89089-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="89089-121">-ProtectableItem</span></span>
<span data-ttu-id="89089-122">Specifica un oggetto elemento protetto da ASR.</span><span class="sxs-lookup"><span data-stu-id="89089-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="89089-123">Il cmdlet ottiene l'elemento protetto dalla replica ASR che corrisponde all'elemento protettivo ASR specificato se l'elemento è protetto.</span><span class="sxs-lookup"><span data-stu-id="89089-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89089-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="89089-124">-ProtectionContainer</span></span>
<span data-ttu-id="89089-125">Specifica l'oggetto contenitore di protezione ASR del contenitore di protezione ASR corrispondente all'elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="89089-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89089-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89089-126">CommonParameters</span></span>
<span data-ttu-id="89089-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89089-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89089-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89089-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89089-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89089-129">INPUTS</span></span>

### <span data-ttu-id="89089-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="89089-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="89089-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="89089-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="89089-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89089-132">OUTPUTS</span></span>

### <span data-ttu-id="89089-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="89089-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="89089-134">Note</span><span class="sxs-lookup"><span data-stu-id="89089-134">NOTES</span></span>

## <span data-ttu-id="89089-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89089-135">RELATED LINKS</span></span>

[<span data-ttu-id="89089-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="89089-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="89089-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="89089-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="89089-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="89089-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
