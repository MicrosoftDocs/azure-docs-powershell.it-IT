---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189142"
---
# <span data-ttu-id="d30c4-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="d30c4-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="d30c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d30c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d30c4-103">Recupera le definizioni di controllo del punteggio di sicurezza in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="d30c4-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="d30c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d30c4-104">SYNTAX</span></span>

### <span data-ttu-id="d30c4-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d30c4-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d30c4-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d30c4-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d30c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d30c4-107">EXAMPLES</span></span>

### <span data-ttu-id="d30c4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d30c4-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="d30c4-109">Ottiene tutte le definizioni di controllo di Sicurezza sicura in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="d30c4-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="d30c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d30c4-110">PARAMETERS</span></span>

### <span data-ttu-id="d30c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d30c4-111">-DefaultProfile</span></span>
<span data-ttu-id="d30c4-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d30c4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d30c4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d30c4-113">CommonParameters</span></span>
<span data-ttu-id="d30c4-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d30c4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d30c4-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d30c4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d30c4-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="d30c4-116">INPUTS</span></span>

### <span data-ttu-id="d30c4-117">System.String</span><span class="sxs-lookup"><span data-stu-id="d30c4-117">System.String</span></span>

## <span data-ttu-id="d30c4-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d30c4-118">OUTPUTS</span></span>

### <span data-ttu-id="d30c4-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="d30c4-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="d30c4-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="d30c4-120">NOTES</span></span>

## <span data-ttu-id="d30c4-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d30c4-121">RELATED LINKS</span></span>
