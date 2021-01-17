---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486324"
---
# <span data-ttu-id="a8262-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="a8262-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="a8262-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8262-102">SYNOPSIS</span></span>
<span data-ttu-id="a8262-103">Ottiene i punteggi sicuri per la sicurezza e i relativi risultati in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="a8262-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="a8262-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8262-104">SYNTAX</span></span>

### <span data-ttu-id="a8262-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8262-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8262-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a8262-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8262-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8262-107">EXAMPLES</span></span>

### <span data-ttu-id="a8262-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8262-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="a8262-109">Ottiene tutti i punteggi sicuri per la sicurezza in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="a8262-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="a8262-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8262-110">PARAMETERS</span></span>

### <span data-ttu-id="a8262-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8262-111">-DefaultProfile</span></span>
<span data-ttu-id="a8262-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8262-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8262-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8262-113">-Name</span></span>
<span data-ttu-id="a8262-114">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="a8262-114">Resource name.</span></span>

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

### <span data-ttu-id="a8262-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8262-115">CommonParameters</span></span>
<span data-ttu-id="a8262-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8262-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8262-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8262-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8262-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8262-118">INPUTS</span></span>

### <span data-ttu-id="a8262-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a8262-119">System.String</span></span>

## <span data-ttu-id="a8262-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8262-120">OUTPUTS</span></span>

### <span data-ttu-id="a8262-121">Microsoft. Azure. Commands. Security. Models. assessments. PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="a8262-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="a8262-122">Note</span><span class="sxs-lookup"><span data-stu-id="a8262-122">NOTES</span></span>

## <span data-ttu-id="a8262-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8262-123">RELATED LINKS</span></span>
