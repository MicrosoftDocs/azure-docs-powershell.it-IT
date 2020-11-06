---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: f7d8efcde5f60ed9cf6eb3aff7f86c9ea3171ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507924"
---
# <span data-ttu-id="c8782-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="c8782-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="c8782-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8782-102">SYNOPSIS</span></span>
<span data-ttu-id="c8782-103">Aggiorna il server di origine e di destinazione per la protezione di un oggetto di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="c8782-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8782-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8782-104">SYNTAX</span></span>

### <span data-ttu-id="c8782-105">ByPEObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8782-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8782-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c8782-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8782-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="c8782-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8782-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8782-108">DESCRIPTION</span></span>
<span data-ttu-id="c8782-109">Il cmdlet **Update-AzureRmSiteRecoveryProtectionDirection** aggiorna il server di origine e di destinazione per la protezione di un oggetto di ripristino di un sito di Azure dopo il completamento di un'operazione di failover di commit.</span><span class="sxs-lookup"><span data-stu-id="c8782-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="c8782-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8782-110">EXAMPLES</span></span>

## <span data-ttu-id="c8782-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8782-111">PARAMETERS</span></span>

### <span data-ttu-id="c8782-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8782-112">-DefaultProfile</span></span>
<span data-ttu-id="c8782-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8782-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8782-114">-Direzione</span><span class="sxs-lookup"><span data-stu-id="c8782-114">-Direction</span></span>
<span data-ttu-id="c8782-115">Specifica la direzione del commit.</span><span class="sxs-lookup"><span data-stu-id="c8782-115">Specifies the direction of the commit.</span></span>
<span data-ttu-id="c8782-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c8782-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8782-117">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="c8782-117">PrimaryToRecovery</span></span>
- <span data-ttu-id="c8782-118">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="c8782-118">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8782-119">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c8782-119">-ProtectionEntity</span></span>
<span data-ttu-id="c8782-120">Specifica l'oggetto entità di protezione.</span><span class="sxs-lookup"><span data-stu-id="c8782-120">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8782-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c8782-121">-RecoveryPlan</span></span>
<span data-ttu-id="c8782-122">Specifica un oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c8782-122">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8782-123">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c8782-123">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8782-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8782-124">CommonParameters</span></span>
<span data-ttu-id="c8782-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8782-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8782-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8782-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8782-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8782-127">INPUTS</span></span>

### <span data-ttu-id="c8782-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c8782-128">ASRProtectionEntity</span></span>
<span data-ttu-id="c8782-129">Il parametro ' ProtectionEntity ' accetta il valore di tipo ' ASRProtectionEntity ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c8782-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="c8782-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c8782-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="c8782-131">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c8782-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="c8782-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c8782-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="c8782-133">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c8782-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="c8782-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8782-134">OUTPUTS</span></span>

### <span data-ttu-id="c8782-135">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c8782-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c8782-136">Note</span><span class="sxs-lookup"><span data-stu-id="c8782-136">NOTES</span></span>

## <span data-ttu-id="c8782-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8782-137">RELATED LINKS</span></span>

