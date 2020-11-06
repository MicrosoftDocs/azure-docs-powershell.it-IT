---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 90b615edefe860e084de0040a13c1ba5a1ff39ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512404"
---
# <span data-ttu-id="aaf75-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="aaf75-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="aaf75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aaf75-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf75-103">Ottiene le proprietà di un elemento protetto della replica del ripristino dei siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf75-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaf75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaf75-104">SYNTAX</span></span>

### <span data-ttu-id="aaf75-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aaf75-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaf75-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="aaf75-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaf75-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="aaf75-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaf75-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="aaf75-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaf75-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaf75-109">DESCRIPTION</span></span>
<span data-ttu-id="aaf75-110">Il cmdlet **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** ottiene le proprietà di tutti gli elementi o dell'elemento protetto della replica ASR specificata dal contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="aaf75-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="aaf75-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaf75-111">EXAMPLES</span></span>

### <span data-ttu-id="aaf75-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aaf75-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="aaf75-113">Elenca tutti gli elementi protetti da replica nel contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="aaf75-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="aaf75-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aaf75-114">PARAMETERS</span></span>

### <span data-ttu-id="aaf75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf75-115">-DefaultProfile</span></span>
<span data-ttu-id="aaf75-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf75-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf75-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="aaf75-117">-FriendlyName</span></span>
<span data-ttu-id="aaf75-118">Specifica il nome descrittivo dell'elemento protetto dalla replica da ottenere.</span><span class="sxs-lookup"><span data-stu-id="aaf75-118">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="aaf75-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="aaf75-119">-Name</span></span>
<span data-ttu-id="aaf75-120">Specifica il nome dell'elemento protetto per la replica da ottenere.</span><span class="sxs-lookup"><span data-stu-id="aaf75-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="aaf75-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="aaf75-121">-ProtectableItem</span></span>
<span data-ttu-id="aaf75-122">Specifica un oggetto elemento protetto da ASR.</span><span class="sxs-lookup"><span data-stu-id="aaf75-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="aaf75-123">Il cmdlet ottiene l'elemento protetto dalla replica ASR che corrisponde all'elemento protettivo ASR specificato se l'elemento è protetto.</span><span class="sxs-lookup"><span data-stu-id="aaf75-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

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

### <span data-ttu-id="aaf75-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="aaf75-124">-ProtectionContainer</span></span>
<span data-ttu-id="aaf75-125">Specifica l'oggetto contenitore di protezione ASR del contenitore di protezione ASR corrispondente all'elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="aaf75-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

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

### <span data-ttu-id="aaf75-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf75-126">CommonParameters</span></span>
<span data-ttu-id="aaf75-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf75-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf75-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf75-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf75-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aaf75-129">INPUTS</span></span>

### <span data-ttu-id="aaf75-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="aaf75-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="aaf75-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="aaf75-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="aaf75-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaf75-132">OUTPUTS</span></span>

### <span data-ttu-id="aaf75-133">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="aaf75-133">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="aaf75-134">Note</span><span class="sxs-lookup"><span data-stu-id="aaf75-134">NOTES</span></span>

## <span data-ttu-id="aaf75-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaf75-135">RELATED LINKS</span></span>

[<span data-ttu-id="aaf75-136">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="aaf75-136">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="aaf75-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="aaf75-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="aaf75-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="aaf75-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)