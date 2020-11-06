---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/edit-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8c078c97a1531863979b6182867e8900550b68b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519853"
---
# <span data-ttu-id="57679-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="57679-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="57679-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57679-102">SYNOPSIS</span></span>
<span data-ttu-id="57679-103">Modifica un piano di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="57679-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57679-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57679-104">SYNTAX</span></span>

### <span data-ttu-id="57679-105">AppendGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57679-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57679-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="57679-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57679-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="57679-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57679-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="57679-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57679-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="57679-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57679-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="57679-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57679-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57679-111">DESCRIPTION</span></span>
<span data-ttu-id="57679-112">Il cmdlet **Edit-AzureRmSiteRecoveryRecoveryPlan** modifica un piano di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="57679-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="57679-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57679-113">EXAMPLES</span></span>

## <span data-ttu-id="57679-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57679-114">PARAMETERS</span></span>

### <span data-ttu-id="57679-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="57679-115">-AddProtectedEntities</span></span>
<span data-ttu-id="57679-116">Specifica una matrice di entità protette da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="57679-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57679-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="57679-117">-AddProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57679-118">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="57679-118">-AppendGroup</span></span>
<span data-ttu-id="57679-119">Indica che questa operazione aggiunge il gruppo all'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="57679-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57679-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57679-120">-DefaultProfile</span></span>
<span data-ttu-id="57679-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57679-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57679-122">-Gruppo</span><span class="sxs-lookup"><span data-stu-id="57679-122">-Group</span></span>
<span data-ttu-id="57679-123">Specifica un gruppo piano di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="57679-123">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57679-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="57679-124">-RecoveryPlan</span></span>
<span data-ttu-id="57679-125">Specifica un piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="57679-125">Specifies a recovery plan.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57679-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="57679-126">-RemoveGroup</span></span>
<span data-ttu-id="57679-127">Rimuove il gruppo piano di ripristino del ripristino del sito specificato.</span><span class="sxs-lookup"><span data-stu-id="57679-127">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57679-128">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="57679-128">-RemoveProtectedEntities</span></span>
<span data-ttu-id="57679-129">Specifica una matrice di entità protette.</span><span class="sxs-lookup"><span data-stu-id="57679-129">Specifies an array of protected entities.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57679-130">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="57679-130">-RemoveProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57679-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57679-131">CommonParameters</span></span>
<span data-ttu-id="57679-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57679-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57679-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57679-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57679-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57679-134">INPUTS</span></span>

### <span data-ttu-id="57679-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="57679-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="57679-136">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="57679-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="57679-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57679-137">OUTPUTS</span></span>

## <span data-ttu-id="57679-138">Note</span><span class="sxs-lookup"><span data-stu-id="57679-138">NOTES</span></span>

## <span data-ttu-id="57679-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57679-139">RELATED LINKS</span></span>

[<span data-ttu-id="57679-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="57679-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="57679-141">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="57679-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
