---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: 6103e9a820a80df7e89130f269296cd073283947
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512867"
---
# <span data-ttu-id="0a27d-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="0a27d-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="0a27d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a27d-102">SYNOPSIS</span></span>
<span data-ttu-id="0a27d-103">Aggiorna il server di origine e di destinazione per la protezione di un oggetto di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="0a27d-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a27d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a27d-104">SYNTAX</span></span>

### <span data-ttu-id="0a27d-105">ByPEObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a27d-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a27d-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0a27d-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a27d-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="0a27d-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a27d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a27d-108">DESCRIPTION</span></span>
<span data-ttu-id="0a27d-109">Il cmdlet **Update-AzureRmSiteRecoveryProtectionDirection** aggiorna il server di origine e di destinazione per la protezione di un oggetto di ripristino di un sito di Azure dopo il completamento di un'operazione di failover di commit.</span><span class="sxs-lookup"><span data-stu-id="0a27d-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="0a27d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a27d-110">EXAMPLES</span></span>

## <span data-ttu-id="0a27d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a27d-111">PARAMETERS</span></span>

### <span data-ttu-id="0a27d-112">-Direzione</span><span class="sxs-lookup"><span data-stu-id="0a27d-112">-Direction</span></span>
<span data-ttu-id="0a27d-113">Specifica la direzione del commit.</span><span class="sxs-lookup"><span data-stu-id="0a27d-113">Specifies the direction of the commit.</span></span>
<span data-ttu-id="0a27d-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a27d-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a27d-115">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0a27d-115">PrimaryToRecovery</span></span>
- <span data-ttu-id="0a27d-116">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0a27d-116">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a27d-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0a27d-117">-ProtectionEntity</span></span>
<span data-ttu-id="0a27d-118">Specifica l'oggetto entità di protezione.</span><span class="sxs-lookup"><span data-stu-id="0a27d-118">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a27d-119">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0a27d-119">-RecoveryPlan</span></span>
<span data-ttu-id="0a27d-120">Specifica un oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0a27d-120">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a27d-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0a27d-121">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a27d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a27d-122">-DefaultProfile</span></span>
<span data-ttu-id="0a27d-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a27d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a27d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a27d-124">CommonParameters</span></span>
<span data-ttu-id="0a27d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a27d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a27d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a27d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a27d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a27d-127">INPUTS</span></span>

### <span data-ttu-id="0a27d-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0a27d-128">ASRProtectionEntity</span></span>
<span data-ttu-id="0a27d-129">Il parametro ' ProtectionEntity ' accetta il valore di tipo ' ASRProtectionEntity ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0a27d-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="0a27d-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0a27d-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="0a27d-131">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0a27d-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="0a27d-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0a27d-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="0a27d-133">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0a27d-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="0a27d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a27d-134">OUTPUTS</span></span>

### <span data-ttu-id="0a27d-135">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0a27d-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0a27d-136">Note</span><span class="sxs-lookup"><span data-stu-id="0a27d-136">NOTES</span></span>

## <span data-ttu-id="0a27d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a27d-137">RELATED LINKS</span></span>

