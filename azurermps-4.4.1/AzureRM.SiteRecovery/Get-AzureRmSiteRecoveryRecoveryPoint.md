---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 68e005a4e54277ad1be304911645c3eeda455d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688231"
---
# <span data-ttu-id="80afc-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="80afc-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="80afc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80afc-102">SYNOPSIS</span></span>
<span data-ttu-id="80afc-103">Ottiene i punti di ripristino disponibili per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="80afc-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80afc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80afc-104">SYNTAX</span></span>

### <span data-ttu-id="80afc-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80afc-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80afc-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="80afc-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80afc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80afc-107">DESCRIPTION</span></span>
<span data-ttu-id="80afc-108">Il cmdlet **Get-AzureRmSiteRecoveryRecoveryPoint** Ottiene l'elenco dei punti di ripristino disponibili per un elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="80afc-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="80afc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80afc-109">EXAMPLES</span></span>

## <span data-ttu-id="80afc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80afc-110">PARAMETERS</span></span>

### <span data-ttu-id="80afc-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="80afc-111">-Name</span></span>
<span data-ttu-id="80afc-112">Specifica il nome del punto di recupero ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80afc-112">Specifies the name of the recovery point this cmdlet gets.</span></span>

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

### <span data-ttu-id="80afc-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="80afc-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="80afc-114">Specifica l'oggetto elemento protetto della replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="80afc-114">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80afc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80afc-115">-DefaultProfile</span></span>
<span data-ttu-id="80afc-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80afc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80afc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80afc-117">CommonParameters</span></span>
<span data-ttu-id="80afc-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80afc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80afc-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80afc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80afc-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80afc-120">INPUTS</span></span>

### <span data-ttu-id="80afc-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="80afc-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="80afc-122">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="80afc-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="80afc-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80afc-123">OUTPUTS</span></span>

### <span data-ttu-id="80afc-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="80afc-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="80afc-125">Note</span><span class="sxs-lookup"><span data-stu-id="80afc-125">NOTES</span></span>

## <span data-ttu-id="80afc-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80afc-126">RELATED LINKS</span></span>

[<span data-ttu-id="80afc-127">Modifica-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="80afc-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="80afc-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="80afc-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="80afc-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="80afc-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="80afc-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="80afc-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="80afc-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="80afc-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
