---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 3a28545958e353c5a5523e24baf20ac6bff21ef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687123"
---
# <span data-ttu-id="f3755-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="f3755-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="f3755-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3755-102">SYNOPSIS</span></span>
<span data-ttu-id="f3755-103">Ottiene informazioni sulle reti gestite dal ripristino del sito per il Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="f3755-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3755-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3755-104">SYNTAX</span></span>

### <span data-ttu-id="f3755-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3755-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="f3755-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f3755-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="f3755-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f3755-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="f3755-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3755-108">DESCRIPTION</span></span>
<span data-ttu-id="f3755-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrNetwork** ottiene informazioni sulle reti di ripristino dei siti di Azure per l'attuale archivio di ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="f3755-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f3755-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3755-110">EXAMPLES</span></span>

### <span data-ttu-id="f3755-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f3755-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="f3755-112">Ottiene tutte le reti note nel tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="f3755-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="f3755-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3755-113">PARAMETERS</span></span>

### <span data-ttu-id="f3755-114">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="f3755-114">-Fabric</span></span>
<span data-ttu-id="f3755-115">Oggetto del tessuto ASR</span><span class="sxs-lookup"><span data-stu-id="f3755-115">ASR fabric object</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3755-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f3755-116">-FriendlyName</span></span>
<span data-ttu-id="f3755-117">Nome descrittivo dell'oggetto ASR di rete.</span><span class="sxs-lookup"><span data-stu-id="f3755-117">Friendly name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3755-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3755-118">-Name</span></span>
<span data-ttu-id="f3755-119">Nome dell'oggetto ASR di rete.</span><span class="sxs-lookup"><span data-stu-id="f3755-119">Name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3755-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3755-120">CommonParameters</span></span>
<span data-ttu-id="f3755-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3755-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3755-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3755-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3755-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3755-123">INPUTS</span></span>

### <span data-ttu-id="f3755-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f3755-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f3755-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3755-125">OUTPUTS</span></span>

### <span data-ttu-id="f3755-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f3755-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f3755-127">Note</span><span class="sxs-lookup"><span data-stu-id="f3755-127">NOTES</span></span>

## <span data-ttu-id="f3755-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3755-128">RELATED LINKS</span></span>

