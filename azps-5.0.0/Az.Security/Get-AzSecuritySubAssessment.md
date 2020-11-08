---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201634"
---
# <span data-ttu-id="48af3-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="48af3-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="48af3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48af3-102">SYNOPSIS</span></span>
<span data-ttu-id="48af3-103">Ottiene i risultati delle valutazioni secondarie in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="48af3-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="48af3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48af3-104">SYNTAX</span></span>

### <span data-ttu-id="48af3-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48af3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48af3-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="48af3-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48af3-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="48af3-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48af3-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="48af3-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48af3-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="48af3-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48af3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48af3-110">DESCRIPTION</span></span>
<span data-ttu-id="48af3-111">Ottiene i risultati delle valutazioni secondarie in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="48af3-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="48af3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48af3-112">EXAMPLES</span></span>

### <span data-ttu-id="48af3-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48af3-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="48af3-114">Ottiene tutti i risultati delle valutazioni secondarie in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="48af3-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="48af3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48af3-115">PARAMETERS</span></span>

### <span data-ttu-id="48af3-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="48af3-116">-AssessedResourceId</span></span>
<span data-ttu-id="48af3-117">ID risorsa completa della risorsa a cui viene calcolata la valutazione.</span><span class="sxs-lookup"><span data-stu-id="48af3-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="48af3-118">-Assessmentname</span><span class="sxs-lookup"><span data-stu-id="48af3-118">-AssessmentName</span></span>
<span data-ttu-id="48af3-119">Nome della risorsa di valutazione.</span><span class="sxs-lookup"><span data-stu-id="48af3-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="48af3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48af3-120">-DefaultProfile</span></span>
<span data-ttu-id="48af3-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48af3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48af3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="48af3-122">-Name</span></span>
<span data-ttu-id="48af3-123">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="48af3-123">Resource name.</span></span>

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

### <span data-ttu-id="48af3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48af3-124">-ResourceId</span></span>
<span data-ttu-id="48af3-125">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="48af3-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="48af3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48af3-126">CommonParameters</span></span>
<span data-ttu-id="48af3-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48af3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48af3-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48af3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48af3-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48af3-129">INPUTS</span></span>

### <span data-ttu-id="48af3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="48af3-130">System.String</span></span>

## <span data-ttu-id="48af3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48af3-131">OUTPUTS</span></span>

### <span data-ttu-id="48af3-132">Microsoft. Azure. Commands. Security. Models. subassessments. PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="48af3-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="48af3-133">Note</span><span class="sxs-lookup"><span data-stu-id="48af3-133">NOTES</span></span>

## <span data-ttu-id="48af3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48af3-134">RELATED LINKS</span></span>
