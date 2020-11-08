---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199656"
---
# <span data-ttu-id="7c0dd-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="7c0dd-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="7c0dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c0dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0dd-103">Creare una nuova configurazione di raccomandazione per la soluzione di sicurezza degli altri</span><span class="sxs-lookup"><span data-stu-id="7c0dd-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="7c0dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c0dd-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c0dd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c0dd-105">DESCRIPTION</span></span>
<span data-ttu-id="7c0dd-106">AzIotSecuritySolutionRecommendationConfigurationObject crea un nuovo oggetto di configurazione della raccomandazione per la soluzione di sicurezza degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="7c0dd-107">In questo modo viene configurato lo stato di una raccomandazione, se è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="7c0dd-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c0dd-108">EXAMPLES</span></span>

### <span data-ttu-id="7c0dd-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c0dd-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="7c0dd-110">Creare una nuova configurazione di raccomandazione per il tipo di raccomandazione "IoT_ACRAuthentication" con stato impostato su Disabilita</span><span class="sxs-lookup"><span data-stu-id="7c0dd-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="7c0dd-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c0dd-111">PARAMETERS</span></span>

### <span data-ttu-id="7c0dd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c0dd-112">-DefaultProfile</span></span>
<span data-ttu-id="7c0dd-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c0dd-114">-Enabled</span><span class="sxs-lookup"><span data-stu-id="7c0dd-114">-Enabled</span></span>
<span data-ttu-id="7c0dd-115">Stato.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-115">Status .</span></span>

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

### <span data-ttu-id="7c0dd-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="7c0dd-116">-RecommendationType</span></span>
<span data-ttu-id="7c0dd-117">Tipo di raccomandazione.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-117">Recommendation type.</span></span>

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

### <span data-ttu-id="7c0dd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0dd-118">CommonParameters</span></span>
<span data-ttu-id="7c0dd-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0dd-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c0dd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0dd-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c0dd-121">INPUTS</span></span>

### <span data-ttu-id="7c0dd-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7c0dd-122">None</span></span>

## <span data-ttu-id="7c0dd-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c0dd-123">OUTPUTS</span></span>

### <span data-ttu-id="7c0dd-124">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c0dd-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="7c0dd-125">Note</span><span class="sxs-lookup"><span data-stu-id="7c0dd-125">NOTES</span></span>

## <span data-ttu-id="7c0dd-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c0dd-126">RELATED LINKS</span></span>