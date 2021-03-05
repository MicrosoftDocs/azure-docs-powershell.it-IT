---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 677c67ecc2418a4940b4cbe79e2ac7145eada0c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984157"
---
# <span data-ttu-id="4549f-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4549f-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="4549f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4549f-102">SYNOPSIS</span></span>
<span data-ttu-id="4549f-103">Creare una nuova configurazione di consigli per una soluzione di sicurezza iot</span><span class="sxs-lookup"><span data-stu-id="4549f-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="4549f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4549f-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4549f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4549f-105">DESCRIPTION</span></span>
<span data-ttu-id="4549f-106">AzIotSecuritySolutionRecommendationConfigurationObject crea un nuovo oggetto di configurazione di consiglio per la soluzione di sicurezza iot.</span><span class="sxs-lookup"><span data-stu-id="4549f-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="4549f-107">In questo modo viene configurato lo stato di un suggerimento, indipendentemente dal fatto che sia abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4549f-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="4549f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4549f-108">EXAMPLES</span></span>

### <span data-ttu-id="4549f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4549f-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="4549f-110">Creare una nuova configurazione di consiglio per il tipo di suggerimento "IoT_ACRAuthentication" con lo stato impostato su disable</span><span class="sxs-lookup"><span data-stu-id="4549f-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="4549f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4549f-111">PARAMETERS</span></span>

### <span data-ttu-id="4549f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4549f-112">-DefaultProfile</span></span>
<span data-ttu-id="4549f-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4549f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4549f-114">-Enabled</span><span class="sxs-lookup"><span data-stu-id="4549f-114">-Enabled</span></span>
<span data-ttu-id="4549f-115">Stato.</span><span class="sxs-lookup"><span data-stu-id="4549f-115">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4549f-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="4549f-116">-RecommendationType</span></span>
<span data-ttu-id="4549f-117">Tipo di suggerimento.</span><span class="sxs-lookup"><span data-stu-id="4549f-117">Recommendation type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4549f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4549f-118">CommonParameters</span></span>
<span data-ttu-id="4549f-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4549f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4549f-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4549f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4549f-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="4549f-121">INPUTS</span></span>

### <span data-ttu-id="4549f-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4549f-122">None</span></span>

## <span data-ttu-id="4549f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4549f-123">OUTPUTS</span></span>

### <span data-ttu-id="4549f-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="4549f-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="4549f-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="4549f-125">NOTES</span></span>

## <span data-ttu-id="4549f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4549f-126">RELATED LINKS</span></span>
