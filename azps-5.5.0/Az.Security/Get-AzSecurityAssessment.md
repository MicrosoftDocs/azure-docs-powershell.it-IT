---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208331"
---
# <span data-ttu-id="0626d-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="0626d-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="0626d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0626d-102">SYNOPSIS</span></span>
<span data-ttu-id="0626d-103">Ottiene le valutazioni della sicurezza e i relativi risultati in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="0626d-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="0626d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0626d-104">SYNTAX</span></span>

### <span data-ttu-id="0626d-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0626d-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0626d-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="0626d-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0626d-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="0626d-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0626d-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0626d-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0626d-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0626d-109">DESCRIPTION</span></span>
<span data-ttu-id="0626d-110">Ottiene la valutazione della sicurezza e i relativi risultati sull'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0626d-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="0626d-111">Le valutazioni della sicurezza consentono di sapere quali procedure consigliate sono consigliate di nuovo dal Centro sicurezza di Azure per essere attenuate per la sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0626d-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="0626d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0626d-112">EXAMPLES</span></span>

### <span data-ttu-id="0626d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0626d-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="0626d-114">Ottiene tutta la valutazione della sicurezza in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="0626d-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="0626d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0626d-115">PARAMETERS</span></span>

### <span data-ttu-id="0626d-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="0626d-116">-AssessedResourceId</span></span>
<span data-ttu-id="0626d-117">ID risorsa completo della risorsa su cui viene calcolata la valutazione.</span><span class="sxs-lookup"><span data-stu-id="0626d-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="0626d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0626d-118">-DefaultProfile</span></span>
<span data-ttu-id="0626d-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0626d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0626d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0626d-120">-Name</span></span>
<span data-ttu-id="0626d-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0626d-121">Resource name.</span></span>

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

### <span data-ttu-id="0626d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0626d-122">-ResourceId</span></span>
<span data-ttu-id="0626d-123">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="0626d-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="0626d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0626d-124">CommonParameters</span></span>
<span data-ttu-id="0626d-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0626d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0626d-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0626d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0626d-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="0626d-127">INPUTS</span></span>

### <span data-ttu-id="0626d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0626d-128">System.String</span></span>

## <span data-ttu-id="0626d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0626d-129">OUTPUTS</span></span>

### <span data-ttu-id="0626d-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="0626d-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="0626d-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="0626d-131">NOTES</span></span>

## <span data-ttu-id="0626d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0626d-132">RELATED LINKS</span></span>
