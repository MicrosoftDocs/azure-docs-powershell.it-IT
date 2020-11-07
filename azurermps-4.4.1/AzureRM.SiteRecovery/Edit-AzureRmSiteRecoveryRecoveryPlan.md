---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d5b7965ed6dea106a40a6be07171e9a3c258f5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685865"
---
# <span data-ttu-id="473c5-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="473c5-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="473c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="473c5-102">SYNOPSIS</span></span>
<span data-ttu-id="473c5-103">Modifica un piano di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="473c5-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="473c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="473c5-104">SYNTAX</span></span>

### <span data-ttu-id="473c5-105">AppendGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="473c5-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="473c5-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="473c5-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="473c5-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="473c5-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="473c5-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="473c5-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="473c5-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="473c5-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="473c5-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="473c5-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="473c5-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="473c5-111">DESCRIPTION</span></span>
<span data-ttu-id="473c5-112">Il cmdlet **Edit-AzureRmSiteRecoveryRecoveryPlan** modifica un piano di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="473c5-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="473c5-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="473c5-113">EXAMPLES</span></span>

## <span data-ttu-id="473c5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="473c5-114">PARAMETERS</span></span>

### <span data-ttu-id="473c5-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="473c5-115">-AddProtectedEntities</span></span>
<span data-ttu-id="473c5-116">Specifica una matrice di entità protette da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="473c5-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473c5-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="473c5-117">-AddProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473c5-118">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="473c5-118">-AppendGroup</span></span>
<span data-ttu-id="473c5-119">Indica che questa operazione aggiunge il gruppo all'oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="473c5-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473c5-120">-Gruppo</span><span class="sxs-lookup"><span data-stu-id="473c5-120">-Group</span></span>
<span data-ttu-id="473c5-121">Specifica un gruppo piano di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="473c5-121">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473c5-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="473c5-122">-RecoveryPlan</span></span>
<span data-ttu-id="473c5-123">Specifica un piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="473c5-123">Specifies a recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="473c5-124">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="473c5-124">-RemoveGroup</span></span>
<span data-ttu-id="473c5-125">Rimuove il gruppo piano di ripristino del ripristino del sito specificato.</span><span class="sxs-lookup"><span data-stu-id="473c5-125">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473c5-126">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="473c5-126">-RemoveProtectedEntities</span></span>
<span data-ttu-id="473c5-127">Specifica una matrice di entità protette.</span><span class="sxs-lookup"><span data-stu-id="473c5-127">Specifies an array of protected entities.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473c5-128">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="473c5-128">-RemoveProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473c5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473c5-129">-DefaultProfile</span></span>
<span data-ttu-id="473c5-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="473c5-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="473c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473c5-131">CommonParameters</span></span>
<span data-ttu-id="473c5-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="473c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473c5-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="473c5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473c5-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="473c5-134">INPUTS</span></span>

### <span data-ttu-id="473c5-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="473c5-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="473c5-136">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="473c5-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="473c5-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="473c5-137">OUTPUTS</span></span>

## <span data-ttu-id="473c5-138">Note</span><span class="sxs-lookup"><span data-stu-id="473c5-138">NOTES</span></span>

## <span data-ttu-id="473c5-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="473c5-139">RELATED LINKS</span></span>

[<span data-ttu-id="473c5-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="473c5-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="473c5-141">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="473c5-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
