---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183590"
---
# <span data-ttu-id="e98b9-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="e98b9-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="e98b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e98b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e98b9-103">Ottiene i risultati delle valutazioni secondarie in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e98b9-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e98b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e98b9-104">SYNTAX</span></span>

### <span data-ttu-id="e98b9-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e98b9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e98b9-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e98b9-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e98b9-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="e98b9-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e98b9-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="e98b9-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e98b9-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e98b9-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e98b9-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e98b9-110">DESCRIPTION</span></span>
<span data-ttu-id="e98b9-111">Ottiene i risultati delle valutazioni secondarie in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e98b9-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e98b9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e98b9-112">EXAMPLES</span></span>

### <span data-ttu-id="e98b9-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e98b9-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="e98b9-114">Ottiene tutti i risultati delle valutazioni secondarie in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e98b9-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e98b9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e98b9-115">PARAMETERS</span></span>

### <span data-ttu-id="e98b9-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="e98b9-116">-AssessedResourceId</span></span>
<span data-ttu-id="e98b9-117">ID risorsa completo della risorsa su cui viene calcolata la valutazione.</span><span class="sxs-lookup"><span data-stu-id="e98b9-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionScope, SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98b9-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="e98b9-118">-AssessmentName</span></span>
<span data-ttu-id="e98b9-119">Nome della risorsa di valutazione.</span><span class="sxs-lookup"><span data-stu-id="e98b9-119">Name of the assessment resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98b9-120">-DefaultProfile</span></span>
<span data-ttu-id="e98b9-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e98b9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e98b9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e98b9-122">-Name</span></span>
<span data-ttu-id="e98b9-123">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e98b9-123">Resource name.</span></span>

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
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98b9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e98b9-124">-ResourceId</span></span>
<span data-ttu-id="e98b9-125">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="e98b9-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e98b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98b9-126">CommonParameters</span></span>
<span data-ttu-id="e98b9-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e98b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98b9-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e98b9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98b9-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="e98b9-129">INPUTS</span></span>

### <span data-ttu-id="e98b9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e98b9-130">System.String</span></span>

## <span data-ttu-id="e98b9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e98b9-131">OUTPUTS</span></span>

### <span data-ttu-id="e98b9-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="e98b9-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="e98b9-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="e98b9-133">NOTES</span></span>

## <span data-ttu-id="e98b9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e98b9-134">RELATED LINKS</span></span>
