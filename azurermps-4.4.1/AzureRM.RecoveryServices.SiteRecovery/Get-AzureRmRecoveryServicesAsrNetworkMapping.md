---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 510e38e201c84ad6158c959d4d56fe9872ad83df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688259"
---
# <span data-ttu-id="0d2ad-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0d2ad-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="0d2ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2ad-103">Ottiene informazioni sui mapping di rete di ripristino del sito per il Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="0d2ad-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d2ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d2ad-104">SYNTAX</span></span>

### <span data-ttu-id="0d2ad-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0d2ad-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Network <ASRNetwork> [<CommonParameters>]
```

### <span data-ttu-id="0d2ad-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="0d2ad-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -Network <ASRNetwork> [<CommonParameters>]
```

## <span data-ttu-id="0d2ad-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d2ad-107">DESCRIPTION</span></span>
<span data-ttu-id="0d2ad-108">Il cmdlet **Get-AzureRmRecoveryServicesAsrNetworkMapping** ottiene le informazioni sui mapping di rete di ripristino dei siti di Azure per il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0d2ad-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="0d2ad-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d2ad-109">EXAMPLES</span></span>

### <span data-ttu-id="0d2ad-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d2ad-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="0d2ad-111">Ottiene tutti i mapping delle reti per la rete passata.</span><span class="sxs-lookup"><span data-stu-id="0d2ad-111">Gets all networks mappings for the passed Network.</span></span>

## <span data-ttu-id="0d2ad-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d2ad-112">PARAMETERS</span></span>

### <span data-ttu-id="0d2ad-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d2ad-113">-Name</span></span>
<span data-ttu-id="0d2ad-114">Nome dell'oggetto mapping di rete ASR da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0d2ad-114">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="0d2ad-115">-Rete</span><span class="sxs-lookup"><span data-stu-id="0d2ad-115">-Network</span></span>
<span data-ttu-id="0d2ad-116">Ottenere i mapping di rete ASR corrispondenti all'oggetto ASR di rete specificato.</span><span class="sxs-lookup"><span data-stu-id="0d2ad-116">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d2ad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2ad-117">CommonParameters</span></span>
<span data-ttu-id="0d2ad-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2ad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2ad-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d2ad-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2ad-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d2ad-120">INPUTS</span></span>

### <span data-ttu-id="0d2ad-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="0d2ad-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="0d2ad-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d2ad-122">OUTPUTS</span></span>

### <span data-ttu-id="0d2ad-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0d2ad-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0d2ad-124">Note</span><span class="sxs-lookup"><span data-stu-id="0d2ad-124">NOTES</span></span>

## <span data-ttu-id="0d2ad-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d2ad-125">RELATED LINKS</span></span>

[<span data-ttu-id="0d2ad-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0d2ad-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="0d2ad-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0d2ad-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
