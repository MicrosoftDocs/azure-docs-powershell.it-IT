---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: df04d3f3dd19c62c37ffbb82cbd57e50c3d73c15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177878"
---
# <span data-ttu-id="0713f-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="0713f-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="0713f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0713f-102">SYNOPSIS</span></span>
<span data-ttu-id="0713f-103">Crea una regola di recapito.</span><span class="sxs-lookup"><span data-stu-id="0713f-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="0713f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0713f-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0713f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0713f-105">DESCRIPTION</span></span>
<span data-ttu-id="0713f-106">Il cmdlet **New-AzCdnDeliveryRule** crea una regola di recapito per la creazione dell'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="0713f-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="0713f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0713f-107">EXAMPLES</span></span>

### <span data-ttu-id="0713f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0713f-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="0713f-109">Creare una regola semplice.</span><span class="sxs-lookup"><span data-stu-id="0713f-109">Create a simple rule.</span></span>

## <span data-ttu-id="0713f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0713f-110">PARAMETERS</span></span>

### <span data-ttu-id="0713f-111">-Action</span><span class="sxs-lookup"><span data-stu-id="0713f-111">-Action</span></span>
<span data-ttu-id="0713f-112">Elenco di azioni che vengono eseguite quando vengono soddisfatte tutte le condizioni di una regola.</span><span class="sxs-lookup"><span data-stu-id="0713f-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0713f-113">-Condizione</span><span class="sxs-lookup"><span data-stu-id="0713f-113">-Condition</span></span>
<span data-ttu-id="0713f-114">Elenco di condizioni per cui deve essere trovata una corrispondenza per l'esecuzione delle azioni.</span><span class="sxs-lookup"><span data-stu-id="0713f-114">A list of conditions that must be matched for the actions to be executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0713f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0713f-115">-DefaultProfile</span></span>
<span data-ttu-id="0713f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0713f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0713f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0713f-117">-Name</span></span>
<span data-ttu-id="0713f-118">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="0713f-118">Name of the rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0713f-119">-Ordine</span><span class="sxs-lookup"><span data-stu-id="0713f-119">-Order</span></span>
<span data-ttu-id="0713f-120">Ordine della regola</span><span class="sxs-lookup"><span data-stu-id="0713f-120">Order of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0713f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0713f-121">CommonParameters</span></span>
<span data-ttu-id="0713f-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0713f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0713f-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0713f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0713f-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="0713f-124">INPUTS</span></span>

### <span data-ttu-id="0713f-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0713f-125">None</span></span>

## <span data-ttu-id="0713f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0713f-126">OUTPUTS</span></span>

### <span data-ttu-id="0713f-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="0713f-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="0713f-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="0713f-128">NOTES</span></span>

## <span data-ttu-id="0713f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0713f-129">RELATED LINKS</span></span>
