---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 92858967d460785af151520c504a4e1cbdb4d3d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008525"
---
# <span data-ttu-id="6fdbc-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="6fdbc-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="6fdbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fdbc-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdbc-103">Ottiene i tipi di valutazioni della sicurezza e la metadta in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6fdbc-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="6fdbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fdbc-104">SYNTAX</span></span>

### <span data-ttu-id="6fdbc-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6fdbc-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fdbc-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="6fdbc-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fdbc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fdbc-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6fdbc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6fdbc-108">DESCRIPTION</span></span>
<span data-ttu-id="6fdbc-109">Ottiene i tipi di valutazioni della sicurezza e la metadta in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6fdbc-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="6fdbc-110">I metadati della valutazione della sicurezza Built-In le valutazioni personalizzate e le valutazioni personalizzate che l'utente può definire.</span><span class="sxs-lookup"><span data-stu-id="6fdbc-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="6fdbc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fdbc-111">EXAMPLES</span></span>

### <span data-ttu-id="6fdbc-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6fdbc-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="6fdbc-113">Ottiene tutte le valutazioni incorporate e le valutazioni personalizzate configurate nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="6fdbc-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="6fdbc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fdbc-114">PARAMETERS</span></span>

### <span data-ttu-id="6fdbc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdbc-115">-DefaultProfile</span></span>
<span data-ttu-id="6fdbc-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fdbc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fdbc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6fdbc-117">-Name</span></span>
<span data-ttu-id="6fdbc-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6fdbc-118">Resource name.</span></span>

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

### <span data-ttu-id="6fdbc-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fdbc-119">-ResourceId</span></span>
<span data-ttu-id="6fdbc-120">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="6fdbc-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="6fdbc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdbc-121">CommonParameters</span></span>
<span data-ttu-id="6fdbc-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fdbc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdbc-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6fdbc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdbc-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="6fdbc-124">INPUTS</span></span>

### <span data-ttu-id="6fdbc-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6fdbc-125">System.String</span></span>

## <span data-ttu-id="6fdbc-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fdbc-126">OUTPUTS</span></span>

### <span data-ttu-id="6fdbc-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="6fdbc-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="6fdbc-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="6fdbc-128">NOTES</span></span>

## <span data-ttu-id="6fdbc-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fdbc-129">RELATED LINKS</span></span>
