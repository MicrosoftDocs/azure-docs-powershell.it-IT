---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 6f3b932ae4d8aad746eb1586525326ba9453af9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377842"
---
# <span data-ttu-id="7366f-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="7366f-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="7366f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7366f-102">SYNOPSIS</span></span>
<span data-ttu-id="7366f-103">Ottiene i controlli di Punteggio sicuro per la sicurezza e i relativi risultati in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="7366f-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="7366f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7366f-104">SYNTAX</span></span>

### <span data-ttu-id="7366f-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7366f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7366f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="7366f-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7366f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7366f-107">EXAMPLES</span></span>

### <span data-ttu-id="7366f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7366f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="7366f-109">Ottiene tutti i punteggi sicuri per la sicurezza in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="7366f-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="7366f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7366f-110">PARAMETERS</span></span>

### <span data-ttu-id="7366f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7366f-111">-DefaultProfile</span></span>
<span data-ttu-id="7366f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7366f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7366f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7366f-113">-Name</span></span>
<span data-ttu-id="7366f-114">Nome del Punteggio sicuro.</span><span class="sxs-lookup"><span data-stu-id="7366f-114">Secure score name.</span></span>

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

### <span data-ttu-id="7366f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7366f-115">CommonParameters</span></span>
<span data-ttu-id="7366f-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7366f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7366f-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7366f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7366f-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7366f-118">INPUTS</span></span>

### <span data-ttu-id="7366f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="7366f-119">System.String</span></span>

## <span data-ttu-id="7366f-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7366f-120">OUTPUTS</span></span>

### <span data-ttu-id="7366f-121">Microsoft. Azure. Commands. Security. Models. assessments. PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="7366f-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="7366f-122">Note</span><span class="sxs-lookup"><span data-stu-id="7366f-122">NOTES</span></span>

## <span data-ttu-id="7366f-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7366f-123">RELATED LINKS</span></span>
