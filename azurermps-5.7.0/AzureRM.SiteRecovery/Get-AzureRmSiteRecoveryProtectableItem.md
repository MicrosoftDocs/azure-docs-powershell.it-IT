---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 2a857c538188c2b9ddf7516ccebda291f3161e1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520367"
---
# <span data-ttu-id="243a1-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="243a1-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="243a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="243a1-102">SYNOPSIS</span></span>
<span data-ttu-id="243a1-103">Ottenere gli elementi protettivi in un contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="243a1-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="243a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="243a1-104">SYNTAX</span></span>

### <span data-ttu-id="243a1-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="243a1-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="243a1-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="243a1-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="243a1-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="243a1-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="243a1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="243a1-108">DESCRIPTION</span></span>
<span data-ttu-id="243a1-109">Il cmdlet **Get-AzureRmSiteRecoveryProtectableItem** ottiene gli elementi protettivi in un contenitore di protezione per il ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="243a1-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="243a1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="243a1-110">EXAMPLES</span></span>

## <span data-ttu-id="243a1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="243a1-111">PARAMETERS</span></span>

### <span data-ttu-id="243a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="243a1-112">-DefaultProfile</span></span>
<span data-ttu-id="243a1-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="243a1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="243a1-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="243a1-114">-FriendlyName</span></span>
<span data-ttu-id="243a1-115">Specifica il nome descrittivo dell'elemento protetto per il ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="243a1-115">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="243a1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="243a1-116">-Name</span></span>
<span data-ttu-id="243a1-117">Specifica il nome dell'elemento protetto per il ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="243a1-117">Specifies the name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="243a1-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="243a1-118">-ProtectionContainer</span></span>
<span data-ttu-id="243a1-119">Specifica l'oggetto contenitore di protezione per il ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="243a1-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="243a1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="243a1-120">CommonParameters</span></span>
<span data-ttu-id="243a1-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="243a1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="243a1-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="243a1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="243a1-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="243a1-123">INPUTS</span></span>

### <span data-ttu-id="243a1-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="243a1-124">ASRProtectionContainer</span></span>
<span data-ttu-id="243a1-125">Il parametro ' ProtectionContainer ' accetta il valore di tipo ' ASRProtectionContainer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="243a1-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="243a1-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="243a1-126">OUTPUTS</span></span>

### <span data-ttu-id="243a1-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="243a1-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="243a1-128">Note</span><span class="sxs-lookup"><span data-stu-id="243a1-128">NOTES</span></span>

## <span data-ttu-id="243a1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="243a1-129">RELATED LINKS</span></span>

[<span data-ttu-id="243a1-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="243a1-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="243a1-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="243a1-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
