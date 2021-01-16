---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360706"
---
# <span data-ttu-id="172c9-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="172c9-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="172c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="172c9-102">SYNOPSIS</span></span>
<span data-ttu-id="172c9-103">Ottiene le valutazioni della sicurezza e i relativi risultati in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="172c9-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="172c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="172c9-104">SYNTAX</span></span>

### <span data-ttu-id="172c9-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="172c9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="172c9-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="172c9-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="172c9-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="172c9-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="172c9-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="172c9-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="172c9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="172c9-109">DESCRIPTION</span></span>
<span data-ttu-id="172c9-110">Ottiene la valutazione della sicurezza e i risultati dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="172c9-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="172c9-111">Le valutazioni della sicurezza consentiranno di limitare le procedure consigliate da Azure Security Center per l'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="172c9-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="172c9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="172c9-112">EXAMPLES</span></span>

### <span data-ttu-id="172c9-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="172c9-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="172c9-114">Ottiene tutta la valutazione della sicurezza in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="172c9-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="172c9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="172c9-115">PARAMETERS</span></span>

### <span data-ttu-id="172c9-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="172c9-116">-AssessedResourceId</span></span>
<span data-ttu-id="172c9-117">ID risorsa completa della risorsa a cui viene calcolata la valutazione.</span><span class="sxs-lookup"><span data-stu-id="172c9-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="172c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172c9-118">-DefaultProfile</span></span>
<span data-ttu-id="172c9-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="172c9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="172c9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="172c9-120">-Name</span></span>
<span data-ttu-id="172c9-121">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="172c9-121">Resource name.</span></span>

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

### <span data-ttu-id="172c9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="172c9-122">-ResourceId</span></span>
<span data-ttu-id="172c9-123">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="172c9-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="172c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172c9-124">CommonParameters</span></span>
<span data-ttu-id="172c9-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="172c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172c9-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="172c9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172c9-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="172c9-127">INPUTS</span></span>

### <span data-ttu-id="172c9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="172c9-128">System.String</span></span>

## <span data-ttu-id="172c9-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="172c9-129">OUTPUTS</span></span>

### <span data-ttu-id="172c9-130">Microsoft. Azure. Commands. Security. Models. assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="172c9-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="172c9-131">Note</span><span class="sxs-lookup"><span data-stu-id="172c9-131">NOTES</span></span>

## <span data-ttu-id="172c9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="172c9-132">RELATED LINKS</span></span>
