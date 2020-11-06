---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7ac4db45f9eb0332217c5097802904cd2146aca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521559"
---
# <span data-ttu-id="dc146-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="dc146-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="dc146-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc146-102">SYNOPSIS</span></span>
<span data-ttu-id="dc146-103">Ottiene i criteri di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="dc146-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc146-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc146-104">SYNTAX</span></span>

### <span data-ttu-id="dc146-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc146-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [<CommonParameters>]
```

### <span data-ttu-id="dc146-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dc146-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="dc146-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="dc146-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="dc146-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc146-108">DESCRIPTION</span></span>
<span data-ttu-id="dc146-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrPolicy** Ottiene l'elenco dei criteri di replica del ripristino del sito Azure configurati o di un criterio di replica specifico per nome.</span><span class="sxs-lookup"><span data-stu-id="dc146-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="dc146-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc146-110">EXAMPLES</span></span>

### <span data-ttu-id="dc146-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dc146-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy -Name $PolicyName
```

<span data-ttu-id="dc146-112">Retruns i criteri di replica con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="dc146-112">Retruns the replication policy with the specified name.</span></span>

## <span data-ttu-id="dc146-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc146-113">PARAMETERS</span></span>

### <span data-ttu-id="dc146-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="dc146-114">-FriendlyName</span></span>
<span data-ttu-id="dc146-115">Specifica il nome descrittivo dei criteri di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="dc146-115">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="dc146-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc146-116">-Name</span></span>
<span data-ttu-id="dc146-117">Specifica il nome del criterio di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="dc146-117">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="dc146-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc146-118">CommonParameters</span></span>
<span data-ttu-id="dc146-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc146-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc146-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc146-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc146-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc146-121">INPUTS</span></span>

### <span data-ttu-id="dc146-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dc146-122">None</span></span>

## <span data-ttu-id="dc146-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc146-123">OUTPUTS</span></span>

### <span data-ttu-id="dc146-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dc146-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dc146-125">Note</span><span class="sxs-lookup"><span data-stu-id="dc146-125">NOTES</span></span>

## <span data-ttu-id="dc146-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc146-126">RELATED LINKS</span></span>

[<span data-ttu-id="dc146-127">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="dc146-127">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="dc146-128">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="dc146-128">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
