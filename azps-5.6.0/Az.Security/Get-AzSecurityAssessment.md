---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 5a8a09955158c21ff6d52e2327370c48448c12d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008542"
---
# <span data-ttu-id="42ff0-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="42ff0-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="42ff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="42ff0-103">Ottiene le valutazioni della sicurezza e i relativi risultati in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="42ff0-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="42ff0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42ff0-104">SYNTAX</span></span>

### <span data-ttu-id="42ff0-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42ff0-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42ff0-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="42ff0-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42ff0-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="42ff0-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42ff0-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="42ff0-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42ff0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="42ff0-109">DESCRIPTION</span></span>
<span data-ttu-id="42ff0-110">Ottiene la valutazione della sicurezza e i relativi risultati sull'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="42ff0-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="42ff0-111">Le valutazioni della sicurezza consentono di sapere quali procedure consigliate sono consigliate di nuovo dal Centro sicurezza di Azure per essere attenuate per la sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="42ff0-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="42ff0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42ff0-112">EXAMPLES</span></span>

### <span data-ttu-id="42ff0-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="42ff0-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="42ff0-114">Ottiene tutta la valutazione della sicurezza in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="42ff0-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="42ff0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42ff0-115">PARAMETERS</span></span>

### <span data-ttu-id="42ff0-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="42ff0-116">-AssessedResourceId</span></span>
<span data-ttu-id="42ff0-117">ID risorsa completo della risorsa su cui viene calcolata la valutazione.</span><span class="sxs-lookup"><span data-stu-id="42ff0-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42ff0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ff0-118">-DefaultProfile</span></span>
<span data-ttu-id="42ff0-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42ff0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ff0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="42ff0-120">-Name</span></span>
<span data-ttu-id="42ff0-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="42ff0-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ff0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42ff0-122">-ResourceId</span></span>
<span data-ttu-id="42ff0-123">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="42ff0-123">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42ff0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ff0-124">CommonParameters</span></span>
<span data-ttu-id="42ff0-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42ff0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ff0-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42ff0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ff0-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="42ff0-127">INPUTS</span></span>

### <span data-ttu-id="42ff0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="42ff0-128">System.String</span></span>

## <span data-ttu-id="42ff0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42ff0-129">OUTPUTS</span></span>

### <span data-ttu-id="42ff0-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="42ff0-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="42ff0-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="42ff0-131">NOTES</span></span>

## <span data-ttu-id="42ff0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42ff0-132">RELATED LINKS</span></span>
