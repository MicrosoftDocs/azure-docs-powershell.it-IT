---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 21a01ae07c383484a6ec8e17d9b09a93671bfbe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511559"
---
# <span data-ttu-id="e36b6-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e36b6-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="e36b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e36b6-102">SYNOPSIS</span></span>
<span data-ttu-id="e36b6-103">Ottiene i punti di ripristino disponibili per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="e36b6-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e36b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e36b6-104">SYNTAX</span></span>

### <span data-ttu-id="e36b6-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e36b6-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e36b6-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e36b6-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e36b6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e36b6-107">DESCRIPTION</span></span>
<span data-ttu-id="e36b6-108">Il cmdlet **Get-AzureRmRecoveryServicesAsrRecoveryPoint** Ottiene l'elenco dei punti di ripristino disponibili per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="e36b6-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="e36b6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e36b6-109">EXAMPLES</span></span>

### <span data-ttu-id="e36b6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e36b6-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="e36b6-111">Ottiene i punti di ripristino per l'elemento protetto della replica ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="e36b6-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="e36b6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e36b6-112">PARAMETERS</span></span>

### <span data-ttu-id="e36b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36b6-113">-DefaultProfile</span></span>
<span data-ttu-id="e36b6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e36b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e36b6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e36b6-115">-Name</span></span>
<span data-ttu-id="e36b6-116">Specifica il nome del punto di recupero da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e36b6-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="e36b6-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e36b6-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e36b6-118">Specifica l'oggetto elemento protetto della replica del ripristino di Azure site per cui ottenere l'elenco dei punti di ripristino disponibili.</span><span class="sxs-lookup"><span data-stu-id="e36b6-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e36b6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36b6-119">CommonParameters</span></span>
<span data-ttu-id="e36b6-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36b6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36b6-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e36b6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36b6-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e36b6-122">INPUTS</span></span>

### <span data-ttu-id="e36b6-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e36b6-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e36b6-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e36b6-124">OUTPUTS</span></span>

### <span data-ttu-id="e36b6-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e36b6-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e36b6-126">Note</span><span class="sxs-lookup"><span data-stu-id="e36b6-126">NOTES</span></span>

## <span data-ttu-id="e36b6-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e36b6-127">RELATED LINKS</span></span>

[<span data-ttu-id="e36b6-128">Modifica-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e36b6-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e36b6-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e36b6-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e36b6-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e36b6-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e36b6-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e36b6-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e36b6-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e36b6-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
