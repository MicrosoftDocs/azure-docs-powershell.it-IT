---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 96a30621bc545b635262fd7937e0e55739d0be7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521557"
---
# <span data-ttu-id="fd4e5-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="fd4e5-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="fd4e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd4e5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4e5-103">Ottiene i punti di ripristino disponibili per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd4e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd4e5-104">SYNTAX</span></span>

### <span data-ttu-id="fd4e5-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd4e5-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [<CommonParameters>]
```

### <span data-ttu-id="fd4e5-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="fd4e5-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [<CommonParameters>]
```

## <span data-ttu-id="fd4e5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd4e5-107">DESCRIPTION</span></span>
<span data-ttu-id="fd4e5-108">Il cmdlet **Get-AzureRmRecoveryServicesAsrRecoveryPoint** Ottiene l'elenco dei punti di ripristino disponibili per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="fd4e5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd4e5-109">EXAMPLES</span></span>

### <span data-ttu-id="fd4e5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd4e5-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="fd4e5-111">Ottiene i punti di ripristino per l'elemento protetto della replica ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="fd4e5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd4e5-112">PARAMETERS</span></span>

### <span data-ttu-id="fd4e5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd4e5-113">-Name</span></span>
<span data-ttu-id="fd4e5-114">Specifica il nome del punto di recupero da ottenere.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-114">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="fd4e5-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fd4e5-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fd4e5-116">Specifica l'oggetto elemento protetto della replica del ripristino di Azure site per cui ottenere l'elenco dei punti di ripristino disponibili.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-116">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4e5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4e5-117">CommonParameters</span></span>
<span data-ttu-id="fd4e5-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4e5-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd4e5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4e5-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd4e5-120">INPUTS</span></span>

### <span data-ttu-id="fd4e5-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fd4e5-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="fd4e5-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd4e5-122">OUTPUTS</span></span>

### <span data-ttu-id="fd4e5-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fd4e5-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fd4e5-124">Note</span><span class="sxs-lookup"><span data-stu-id="fd4e5-124">NOTES</span></span>

## <span data-ttu-id="fd4e5-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd4e5-125">RELATED LINKS</span></span>

[<span data-ttu-id="fd4e5-126">Modifica-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fd4e5-126">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="fd4e5-127">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fd4e5-127">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="fd4e5-128">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fd4e5-128">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="fd4e5-129">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fd4e5-129">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="fd4e5-130">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fd4e5-130">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
