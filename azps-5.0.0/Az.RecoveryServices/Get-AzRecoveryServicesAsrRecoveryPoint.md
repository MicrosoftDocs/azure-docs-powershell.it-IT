---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310668"
---
# <span data-ttu-id="aa578-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="aa578-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="aa578-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa578-102">SYNOPSIS</span></span>
<span data-ttu-id="aa578-103">Ottiene i punti di ripristino disponibili per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="aa578-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="aa578-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa578-104">SYNTAX</span></span>

### <span data-ttu-id="aa578-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa578-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa578-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="aa578-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa578-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa578-107">DESCRIPTION</span></span>
<span data-ttu-id="aa578-108">Il cmdlet **Get-AzRecoveryServicesAsrRecoveryPoint** Ottiene l'elenco dei punti di ripristino disponibili per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="aa578-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="aa578-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa578-109">EXAMPLES</span></span>

### <span data-ttu-id="aa578-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aa578-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="aa578-111">Ottiene i punti di ripristino per l'elemento protetto della replica ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="aa578-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="aa578-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa578-112">PARAMETERS</span></span>

### <span data-ttu-id="aa578-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa578-113">-DefaultProfile</span></span>
<span data-ttu-id="aa578-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa578-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="aa578-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa578-115">-Name</span></span>
<span data-ttu-id="aa578-116">Specifica il nome del punto di recupero da ottenere.</span><span class="sxs-lookup"><span data-stu-id="aa578-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="aa578-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="aa578-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="aa578-118">Specifica l'oggetto elemento protetto della replica del ripristino di Azure site per cui ottenere l'elenco dei punti di ripristino disponibili.</span><span class="sxs-lookup"><span data-stu-id="aa578-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="aa578-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa578-119">CommonParameters</span></span>
<span data-ttu-id="aa578-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa578-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa578-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa578-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa578-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa578-122">INPUTS</span></span>

### <span data-ttu-id="aa578-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="aa578-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="aa578-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa578-124">OUTPUTS</span></span>

### <span data-ttu-id="aa578-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="aa578-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="aa578-126">Note</span><span class="sxs-lookup"><span data-stu-id="aa578-126">NOTES</span></span>

## <span data-ttu-id="aa578-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa578-127">RELATED LINKS</span></span>

[<span data-ttu-id="aa578-128">Modifica-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aa578-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="aa578-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aa578-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="aa578-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aa578-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="aa578-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aa578-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="aa578-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aa578-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
