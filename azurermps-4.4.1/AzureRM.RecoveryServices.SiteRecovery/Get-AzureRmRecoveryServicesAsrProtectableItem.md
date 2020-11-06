---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: b209c706a8da88cfc5188b11302166469749c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521158"
---
# <span data-ttu-id="73bb4-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="73bb4-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="73bb4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="73bb4-103">Ottenere gli elementi protettivi in un contenitore di protezione ASR.</span><span class="sxs-lookup"><span data-stu-id="73bb4-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73bb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73bb4-104">SYNTAX</span></span>

### <span data-ttu-id="73bb4-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73bb4-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="73bb4-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="73bb4-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="73bb4-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="73bb4-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="73bb4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73bb4-108">DESCRIPTION</span></span>
<span data-ttu-id="73bb4-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrProtectableItem** ottiene gli elementi protettivi in un contenitore di protezione per il ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="73bb4-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="73bb4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73bb4-110">EXAMPLES</span></span>

### <span data-ttu-id="73bb4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="73bb4-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="73bb4-112">Ottiene tutti gli elementi protettivi nel contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="73bb4-112">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="73bb4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73bb4-113">PARAMETERS</span></span>

### <span data-ttu-id="73bb4-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="73bb4-114">-FriendlyName</span></span>
<span data-ttu-id="73bb4-115">Specifica il nome descrittivo dell'elemento protetto da ASR.</span><span class="sxs-lookup"><span data-stu-id="73bb4-115">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="73bb4-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="73bb4-116">-Name</span></span>
<span data-ttu-id="73bb4-117">Specifica il nome dell'elemento protetto da ASR.</span><span class="sxs-lookup"><span data-stu-id="73bb4-117">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="73bb4-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="73bb4-118">-ProtectionContainer</span></span>
<span data-ttu-id="73bb4-119">Specifica l'oggetto contenitore di protezione per il ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="73bb4-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73bb4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bb4-120">CommonParameters</span></span>
<span data-ttu-id="73bb4-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73bb4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bb4-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73bb4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bb4-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73bb4-123">INPUTS</span></span>

### <span data-ttu-id="73bb4-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="73bb4-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="73bb4-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73bb4-125">OUTPUTS</span></span>

### <span data-ttu-id="73bb4-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="73bb4-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="73bb4-127">Note</span><span class="sxs-lookup"><span data-stu-id="73bb4-127">NOTES</span></span>

## <span data-ttu-id="73bb4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73bb4-128">RELATED LINKS</span></span>

[<span data-ttu-id="73bb4-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="73bb4-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="73bb4-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="73bb4-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
