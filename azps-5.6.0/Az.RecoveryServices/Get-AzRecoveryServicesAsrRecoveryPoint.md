---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 27f1f0f03da7a4ad912be28a2de85bf6e7cf58f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014941"
---
# <span data-ttu-id="96669-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="96669-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="96669-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96669-102">SYNOPSIS</span></span>
<span data-ttu-id="96669-103">Recupera i punti di ripristino disponibili per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="96669-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="96669-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96669-104">SYNTAX</span></span>

### <span data-ttu-id="96669-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="96669-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96669-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="96669-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96669-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="96669-107">DESCRIPTION</span></span>
<span data-ttu-id="96669-108">Il cmdlet **Get-AzRecoveryServicesAsrRecoveryPoint** ottiene l'elenco dei punti di ripristino disponibili per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="96669-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="96669-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96669-109">EXAMPLES</span></span>

### <span data-ttu-id="96669-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="96669-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="96669-111">Recupera i punti di ripristino per l'elemento protetto da replica ASR specificata.</span><span class="sxs-lookup"><span data-stu-id="96669-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="96669-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96669-112">PARAMETERS</span></span>

### <span data-ttu-id="96669-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96669-113">-DefaultProfile</span></span>
<span data-ttu-id="96669-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96669-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96669-115">-Name</span><span class="sxs-lookup"><span data-stu-id="96669-115">-Name</span></span>
<span data-ttu-id="96669-116">Specifica il nome del punto di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="96669-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="96669-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="96669-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="96669-118">Specifica l'oggetto elemento protetto da replica di Azure Site Recovery per cui ottenere l'elenco dei punti di ripristino disponibili.</span><span class="sxs-lookup"><span data-stu-id="96669-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="96669-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96669-119">CommonParameters</span></span>
<span data-ttu-id="96669-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96669-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96669-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="96669-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96669-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="96669-122">INPUTS</span></span>

### <span data-ttu-id="96669-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="96669-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="96669-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96669-124">OUTPUTS</span></span>

### <span data-ttu-id="96669-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="96669-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="96669-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="96669-126">NOTES</span></span>

## <span data-ttu-id="96669-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96669-127">RELATED LINKS</span></span>

[<span data-ttu-id="96669-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96669-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="96669-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96669-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="96669-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96669-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="96669-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96669-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="96669-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96669-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
