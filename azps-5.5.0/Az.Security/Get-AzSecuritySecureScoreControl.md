---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 6f3b932ae4d8aad746eb1586525326ba9453af9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189158"
---
# <span data-ttu-id="248c6-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="248c6-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="248c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="248c6-102">SYNOPSIS</span></span>
<span data-ttu-id="248c6-103">Ottiene i controlli del punteggio di sicurezza e i relativi risultati in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="248c6-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="248c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="248c6-104">SYNTAX</span></span>

### <span data-ttu-id="248c6-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="248c6-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="248c6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="248c6-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="248c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="248c6-107">EXAMPLES</span></span>

### <span data-ttu-id="248c6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="248c6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="248c6-109">Ottiene tutti i punteggi di sicurezza di un abbonamento</span><span class="sxs-lookup"><span data-stu-id="248c6-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="248c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="248c6-110">PARAMETERS</span></span>

### <span data-ttu-id="248c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="248c6-111">-DefaultProfile</span></span>
<span data-ttu-id="248c6-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="248c6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="248c6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="248c6-113">-Name</span></span>
<span data-ttu-id="248c6-114">Nome del punteggio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="248c6-114">Secure score name.</span></span>

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

### <span data-ttu-id="248c6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="248c6-115">CommonParameters</span></span>
<span data-ttu-id="248c6-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="248c6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="248c6-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="248c6-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="248c6-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="248c6-118">INPUTS</span></span>

### <span data-ttu-id="248c6-119">System.String</span><span class="sxs-lookup"><span data-stu-id="248c6-119">System.String</span></span>

## <span data-ttu-id="248c6-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="248c6-120">OUTPUTS</span></span>

### <span data-ttu-id="248c6-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="248c6-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="248c6-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="248c6-122">NOTES</span></span>

## <span data-ttu-id="248c6-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="248c6-123">RELATED LINKS</span></span>
