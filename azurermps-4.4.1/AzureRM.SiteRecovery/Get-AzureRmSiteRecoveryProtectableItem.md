---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 0b2fe8f500e17bc21407870a712ad4b9f00fd544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685862"
---
# <span data-ttu-id="78bfb-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="78bfb-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="78bfb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="78bfb-103">Ottenere gli elementi protettivi in un contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="78bfb-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78bfb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78bfb-104">SYNTAX</span></span>

### <span data-ttu-id="78bfb-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78bfb-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78bfb-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="78bfb-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78bfb-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="78bfb-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78bfb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78bfb-108">DESCRIPTION</span></span>
<span data-ttu-id="78bfb-109">Il cmdlet **Get-AzureRmSiteRecoveryProtectableItem** ottiene gli elementi protettivi in un contenitore di protezione per il ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="78bfb-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="78bfb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78bfb-110">EXAMPLES</span></span>

## <span data-ttu-id="78bfb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78bfb-111">PARAMETERS</span></span>

### <span data-ttu-id="78bfb-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="78bfb-112">-FriendlyName</span></span>
<span data-ttu-id="78bfb-113">Specifica il nome descrittivo dell'elemento protetto per il ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="78bfb-113">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="78bfb-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="78bfb-114">-Name</span></span>
<span data-ttu-id="78bfb-115">Specifica il nome dell'elemento protetto per il ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="78bfb-115">Specifies the name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="78bfb-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="78bfb-116">-ProtectionContainer</span></span>
<span data-ttu-id="78bfb-117">Specifica l'oggetto contenitore di protezione per il ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="78bfb-117">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78bfb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78bfb-118">-DefaultProfile</span></span>
<span data-ttu-id="78bfb-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78bfb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78bfb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78bfb-120">CommonParameters</span></span>
<span data-ttu-id="78bfb-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78bfb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78bfb-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78bfb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78bfb-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78bfb-123">INPUTS</span></span>

### <span data-ttu-id="78bfb-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="78bfb-124">ASRProtectionContainer</span></span>
<span data-ttu-id="78bfb-125">Il parametro ' ProtectionContainer ' accetta il valore di tipo ' ASRProtectionContainer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="78bfb-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="78bfb-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78bfb-126">OUTPUTS</span></span>

### <span data-ttu-id="78bfb-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="78bfb-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="78bfb-128">Note</span><span class="sxs-lookup"><span data-stu-id="78bfb-128">NOTES</span></span>

## <span data-ttu-id="78bfb-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78bfb-129">RELATED LINKS</span></span>

[<span data-ttu-id="78bfb-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="78bfb-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="78bfb-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="78bfb-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
