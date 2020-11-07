---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d497938a8a68d3efc6cafd1640de8d0be738b113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688229"
---
# <span data-ttu-id="37762-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="37762-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="37762-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37762-102">SYNOPSIS</span></span>
<span data-ttu-id="37762-103">Aggiorna un piano di ripristino nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="37762-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37762-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37762-104">SYNTAX</span></span>

### <span data-ttu-id="37762-105">ByRPObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37762-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37762-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="37762-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37762-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37762-107">DESCRIPTION</span></span>
<span data-ttu-id="37762-108">Il cmdlet **Update-AzureRmSiteRecoveryRecoveryPlan** aggiorna un piano di ripristino in Azure Site Recovery e lo pubblica.</span><span class="sxs-lookup"><span data-stu-id="37762-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="37762-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37762-109">EXAMPLES</span></span>

### <span data-ttu-id="37762-110">Esempio 1: aggiornare un piano di ripristino</span><span class="sxs-lookup"><span data-stu-id="37762-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="37762-111">Questo comando Aggiorna il piano di ripristino specificato e lo pubblica.</span><span class="sxs-lookup"><span data-stu-id="37762-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="37762-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37762-112">PARAMETERS</span></span>

### <span data-ttu-id="37762-113">-Path</span><span class="sxs-lookup"><span data-stu-id="37762-113">-Path</span></span>
<span data-ttu-id="37762-114">Specifica il percorso del file del piano di ripristino del piano di ripristino che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="37762-114">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37762-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="37762-115">-RecoveryPlan</span></span>
<span data-ttu-id="37762-116">Specifica un piano di ripristino che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="37762-116">Specifies a recovery plan that this cmdlet updates.</span></span>

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

### <span data-ttu-id="37762-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37762-117">-DefaultProfile</span></span>
<span data-ttu-id="37762-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37762-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37762-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37762-119">CommonParameters</span></span>
<span data-ttu-id="37762-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37762-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37762-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37762-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37762-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37762-122">INPUTS</span></span>

### <span data-ttu-id="37762-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="37762-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="37762-124">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="37762-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="37762-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37762-125">OUTPUTS</span></span>

## <span data-ttu-id="37762-126">Note</span><span class="sxs-lookup"><span data-stu-id="37762-126">NOTES</span></span>

## <span data-ttu-id="37762-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37762-127">RELATED LINKS</span></span>

[<span data-ttu-id="37762-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="37762-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="37762-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="37762-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="37762-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="37762-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


