---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: e8ec0073eef8b8db95197e19f2bfd61d0bbcdafd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995915"
---
# <span data-ttu-id="4cb0d-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="4cb0d-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="4cb0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cb0d-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb0d-103">Recupera le definizioni di controllo del punteggio di sicurezza in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="4cb0d-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="4cb0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cb0d-104">SYNTAX</span></span>

### <span data-ttu-id="4cb0d-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4cb0d-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cb0d-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4cb0d-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cb0d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cb0d-107">EXAMPLES</span></span>

### <span data-ttu-id="4cb0d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4cb0d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="4cb0d-109">Ottiene tutte le definizioni di controllo di Sicurezza sicura in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="4cb0d-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="4cb0d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cb0d-110">PARAMETERS</span></span>

### <span data-ttu-id="4cb0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb0d-111">-DefaultProfile</span></span>
<span data-ttu-id="4cb0d-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cb0d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cb0d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb0d-113">CommonParameters</span></span>
<span data-ttu-id="4cb0d-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cb0d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb0d-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4cb0d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb0d-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="4cb0d-116">INPUTS</span></span>

### <span data-ttu-id="4cb0d-117">System.String</span><span class="sxs-lookup"><span data-stu-id="4cb0d-117">System.String</span></span>

## <span data-ttu-id="4cb0d-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cb0d-118">OUTPUTS</span></span>

### <span data-ttu-id="4cb0d-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="4cb0d-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="4cb0d-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="4cb0d-120">NOTES</span></span>

## <span data-ttu-id="4cb0d-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cb0d-121">RELATED LINKS</span></span>
