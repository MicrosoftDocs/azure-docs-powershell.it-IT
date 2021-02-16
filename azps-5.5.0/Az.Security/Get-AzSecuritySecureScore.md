---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189174"
---
# <span data-ttu-id="1811e-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="1811e-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="1811e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1811e-102">SYNOPSIS</span></span>
<span data-ttu-id="1811e-103">Ottiene i punteggi per la sicurezza e i relativi risultati in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="1811e-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="1811e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1811e-104">SYNTAX</span></span>

### <span data-ttu-id="1811e-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1811e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1811e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="1811e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1811e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1811e-107">EXAMPLES</span></span>

### <span data-ttu-id="1811e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1811e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="1811e-109">Ottiene tutti i punteggi di sicurezza di un abbonamento</span><span class="sxs-lookup"><span data-stu-id="1811e-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="1811e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1811e-110">PARAMETERS</span></span>

### <span data-ttu-id="1811e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1811e-111">-DefaultProfile</span></span>
<span data-ttu-id="1811e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1811e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1811e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1811e-113">-Name</span></span>
<span data-ttu-id="1811e-114">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1811e-114">Resource name.</span></span>

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

### <span data-ttu-id="1811e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1811e-115">CommonParameters</span></span>
<span data-ttu-id="1811e-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1811e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1811e-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1811e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1811e-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="1811e-118">INPUTS</span></span>

### <span data-ttu-id="1811e-119">System.String</span><span class="sxs-lookup"><span data-stu-id="1811e-119">System.String</span></span>

## <span data-ttu-id="1811e-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1811e-120">OUTPUTS</span></span>

### <span data-ttu-id="1811e-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="1811e-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="1811e-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="1811e-122">NOTES</span></span>

## <span data-ttu-id="1811e-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1811e-123">RELATED LINKS</span></span>
