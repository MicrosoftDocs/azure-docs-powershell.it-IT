---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d6c93a6ca54a67c13fcba54a11d9f30c61377e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687423"
---
# <span data-ttu-id="2ed0b-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ed0b-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="2ed0b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ed0b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed0b-103">Rimuove un piano di ripristino del sito dal ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ed0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ed0b-104">SYNTAX</span></span>

### <span data-ttu-id="2ed0b-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ed0b-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ed0b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2ed0b-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ed0b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ed0b-107">DESCRIPTION</span></span>
<span data-ttu-id="2ed0b-108">Il cmdlet **Remove-AzureRmSiteRecoveryRecoveryPlan** rimuove un piano di ripristino del sito dal ripristino del sito di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="2ed0b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ed0b-109">EXAMPLES</span></span>

### <span data-ttu-id="2ed0b-110">Esempio 1: rimuovere un piano di ripristino</span><span class="sxs-lookup"><span data-stu-id="2ed0b-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="2ed0b-111">Il primo comando usa il cmdlet Get-AzureRmSiteRecoveryRecoveryPlan per ottenere il piano di ripristino del sito e lo archivia nella variabile $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="2ed0b-112">Il secondo comando rimuove il piano di ripristino in $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="2ed0b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ed0b-113">PARAMETERS</span></span>

### <span data-ttu-id="2ed0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed0b-114">-DefaultProfile</span></span>
<span data-ttu-id="2ed0b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ed0b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ed0b-116">-Name</span></span>
<span data-ttu-id="2ed0b-117">Specifica il nome del piano di ripristino rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-117">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed0b-118">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ed0b-118">-RecoveryPlan</span></span>
<span data-ttu-id="2ed0b-119">Specifica il piano di ripristino rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-119">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ed0b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed0b-120">CommonParameters</span></span>
<span data-ttu-id="2ed0b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed0b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed0b-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed0b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed0b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ed0b-123">INPUTS</span></span>

### <span data-ttu-id="2ed0b-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ed0b-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="2ed0b-125">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2ed0b-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="2ed0b-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ed0b-126">OUTPUTS</span></span>

## <span data-ttu-id="2ed0b-127">Note</span><span class="sxs-lookup"><span data-stu-id="2ed0b-127">NOTES</span></span>

## <span data-ttu-id="2ed0b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ed0b-128">RELATED LINKS</span></span>

[<span data-ttu-id="2ed0b-129">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ed0b-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="2ed0b-130">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ed0b-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="2ed0b-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ed0b-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


