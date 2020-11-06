---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fbd2f518d3bdcf64599e32b55cdb9f416c29be21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521556"
---
# <span data-ttu-id="02d0e-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02d0e-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="02d0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="02d0e-103">Ottiene le proprietà di un elemento protetto della replica del ripristino dei siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="02d0e-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02d0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02d0e-104">SYNTAX</span></span>

### <span data-ttu-id="02d0e-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="02d0e-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="02d0e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="02d0e-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="02d0e-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="02d0e-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="02d0e-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="02d0e-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [<CommonParameters>]
```

## <span data-ttu-id="02d0e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02d0e-109">DESCRIPTION</span></span>
<span data-ttu-id="02d0e-110">Il cmdlet **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** ottiene le proprietà di tutti gli elementi o dell'elemento protetto della replica ASR specificata dal contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="02d0e-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="02d0e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02d0e-111">EXAMPLES</span></span>

### <span data-ttu-id="02d0e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02d0e-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="02d0e-113">Elenca tutti gli elementi protetti da replica nel contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="02d0e-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="02d0e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02d0e-114">PARAMETERS</span></span>

### <span data-ttu-id="02d0e-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="02d0e-115">-FriendlyName</span></span>
<span data-ttu-id="02d0e-116">Specifica il nome descrittivo dell'elemento protetto dalla replica da ottenere.</span><span class="sxs-lookup"><span data-stu-id="02d0e-116">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02d0e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="02d0e-117">-Name</span></span>
<span data-ttu-id="02d0e-118">Specifica il nome dell'elemento protetto per la replica da ottenere.</span><span class="sxs-lookup"><span data-stu-id="02d0e-118">Specifies the name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02d0e-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="02d0e-119">-ProtectableItem</span></span>
<span data-ttu-id="02d0e-120">Specifica un oggetto elemento protetto da ASR.</span><span class="sxs-lookup"><span data-stu-id="02d0e-120">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="02d0e-121">Il cmdlet ottiene l'elemento protetto dalla replica ASR che corrisponde all'elemento protettivo ASR specificato se l'elemento è protetto.</span><span class="sxs-lookup"><span data-stu-id="02d0e-121">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02d0e-122">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="02d0e-122">-ProtectionContainer</span></span>
<span data-ttu-id="02d0e-123">Specifica l'oggetto contenitore di protezione ASR del contenitore di protezione ASR corrispondente all'elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="02d0e-123">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02d0e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d0e-124">CommonParameters</span></span>
<span data-ttu-id="02d0e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d0e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d0e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d0e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d0e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02d0e-127">INPUTS</span></span>

### <span data-ttu-id="02d0e-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="02d0e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="02d0e-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="02d0e-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="02d0e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02d0e-130">OUTPUTS</span></span>

### <span data-ttu-id="02d0e-131">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="02d0e-131">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="02d0e-132">Note</span><span class="sxs-lookup"><span data-stu-id="02d0e-132">NOTES</span></span>

## <span data-ttu-id="02d0e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02d0e-133">RELATED LINKS</span></span>

[<span data-ttu-id="02d0e-134">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02d0e-134">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="02d0e-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02d0e-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="02d0e-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="02d0e-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
