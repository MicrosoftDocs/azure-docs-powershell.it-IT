---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 1d6199042cec106d81ba91ccb7ccb854741d319d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687122"
---
# <span data-ttu-id="3e804-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3e804-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="3e804-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e804-102">SYNOPSIS</span></span>
<span data-ttu-id="3e804-103">Ottiene i dettagli dei provider di servizi di ripristino ASR registrati nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3e804-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e804-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e804-104">SYNTAX</span></span>

### <span data-ttu-id="3e804-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e804-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="3e804-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3e804-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="3e804-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3e804-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric> [<CommonParameters>]
```

## <span data-ttu-id="3e804-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e804-108">DESCRIPTION</span></span>
<span data-ttu-id="3e804-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrServicesProvider** ottiene le informazioni sui provider di ripristino del sito di Azure nel Vault.</span><span class="sxs-lookup"><span data-stu-id="3e804-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="3e804-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e804-110">EXAMPLES</span></span>

### <span data-ttu-id="3e804-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e804-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="3e804-112">Elenca tutti i provider di servizi di replica ASR registrati nel Vault di servizi di ripristino che corrispondono al tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="3e804-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="3e804-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e804-113">PARAMETERS</span></span>

### <span data-ttu-id="3e804-114">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="3e804-114">-Fabric</span></span>
<span data-ttu-id="3e804-115">Specifica l'oggetto del tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="3e804-115">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="3e804-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3e804-116">-FriendlyName</span></span>
<span data-ttu-id="3e804-117">Specifica il nome descrittivo del provider di servizi di ripristino ASR per ottenere informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="3e804-117">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="3e804-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e804-118">-Name</span></span>
<span data-ttu-id="3e804-119">Specifica il nome del provider di servizi di ripristino ASR per cui ottenere i dettagli.</span><span class="sxs-lookup"><span data-stu-id="3e804-119">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="3e804-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e804-120">CommonParameters</span></span>
<span data-ttu-id="3e804-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e804-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e804-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e804-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e804-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e804-123">INPUTS</span></span>

### <span data-ttu-id="3e804-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="3e804-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="3e804-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e804-125">OUTPUTS</span></span>

### <span data-ttu-id="3e804-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3e804-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3e804-127">Note</span><span class="sxs-lookup"><span data-stu-id="3e804-127">NOTES</span></span>

## <span data-ttu-id="3e804-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e804-128">RELATED LINKS</span></span>

[<span data-ttu-id="3e804-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3e804-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="3e804-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3e804-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
