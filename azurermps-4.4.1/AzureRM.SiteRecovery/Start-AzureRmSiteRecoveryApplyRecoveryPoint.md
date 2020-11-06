---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: d77ed7723ef9875413c551912563b4ee2f4ae306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512888"
---
# <span data-ttu-id="158b9-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="158b9-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="158b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="158b9-102">SYNOPSIS</span></span>
<span data-ttu-id="158b9-103">Cambia un punto di recupero per un elemento non superato protetto prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="158b9-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="158b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="158b9-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="158b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="158b9-105">DESCRIPTION</span></span>
<span data-ttu-id="158b9-106">**Start-AzureRmSiteRecoveryApplyRecoveryPoint** modifica un punto di recupero per un elemento non riuscito tramite protezione prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="158b9-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="158b9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="158b9-107">EXAMPLES</span></span>

## <span data-ttu-id="158b9-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="158b9-108">PARAMETERS</span></span>

### <span data-ttu-id="158b9-109">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="158b9-109">-DataEncryptionPrimaryCertFile</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158b9-110">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="158b9-110">-DataEncryptionSecondaryCertFile</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158b9-111">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="158b9-111">-RecoveryPoint</span></span>
<span data-ttu-id="158b9-112">Specifica l'oggetto punto di ripristino modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="158b9-112">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158b9-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="158b9-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="158b9-114">Specifica l'oggetto elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="158b9-114">Specifies the Replication Protected Item object.</span></span>

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

### <span data-ttu-id="158b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158b9-115">-DefaultProfile</span></span>
<span data-ttu-id="158b9-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="158b9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="158b9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158b9-117">CommonParameters</span></span>
<span data-ttu-id="158b9-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="158b9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158b9-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="158b9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158b9-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="158b9-120">INPUTS</span></span>

### <span data-ttu-id="158b9-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="158b9-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="158b9-122">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="158b9-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="158b9-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="158b9-123">OUTPUTS</span></span>

### <span data-ttu-id="158b9-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="158b9-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="158b9-125">Note</span><span class="sxs-lookup"><span data-stu-id="158b9-125">NOTES</span></span>

## <span data-ttu-id="158b9-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="158b9-126">RELATED LINKS</span></span>

[<span data-ttu-id="158b9-127">Cmdlet di ripristino del sito di Azure</span><span class="sxs-lookup"><span data-stu-id="158b9-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
