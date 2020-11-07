---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: 981447b1988dd750534a69529989d5d3480bc006
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675549"
---
# <span data-ttu-id="48cd8-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="48cd8-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="48cd8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="48cd8-103">Crea una regola di recapito.</span><span class="sxs-lookup"><span data-stu-id="48cd8-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="48cd8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48cd8-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48cd8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="48cd8-106">Il cmdlet **New-AzCdnDeliveryRule** crea una regola di recapito per la creazione di endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="48cd8-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="48cd8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48cd8-107">EXAMPLES</span></span>

### <span data-ttu-id="48cd8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48cd8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="48cd8-109">Creare una regola semplice.</span><span class="sxs-lookup"><span data-stu-id="48cd8-109">Create a simple rule.</span></span>

## <span data-ttu-id="48cd8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48cd8-110">PARAMETERS</span></span>

### <span data-ttu-id="48cd8-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="48cd8-111">-Action</span></span>
<span data-ttu-id="48cd8-112">Elenco di azioni che vengono eseguite quando tutte le condizioni di una regola sono soddisfatte.</span><span class="sxs-lookup"><span data-stu-id="48cd8-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

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

### <span data-ttu-id="48cd8-113">-Condition</span><span class="sxs-lookup"><span data-stu-id="48cd8-113">-Condition</span></span>
<span data-ttu-id="48cd8-114">Un elenco di condizioni che devono essere confrontate per le azioni da eseguire.</span><span class="sxs-lookup"><span data-stu-id="48cd8-114">A list of conditions that must be matched for the actions to be executed.</span></span>

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

### <span data-ttu-id="48cd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48cd8-115">-DefaultProfile</span></span>
<span data-ttu-id="48cd8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48cd8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48cd8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="48cd8-117">-Name</span></span>
<span data-ttu-id="48cd8-118">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="48cd8-118">Name of the rule</span></span>

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

### <span data-ttu-id="48cd8-119">-Ordine</span><span class="sxs-lookup"><span data-stu-id="48cd8-119">-Order</span></span>
<span data-ttu-id="48cd8-120">Ordine della regola</span><span class="sxs-lookup"><span data-stu-id="48cd8-120">Order of the rule</span></span>

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

### <span data-ttu-id="48cd8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48cd8-121">CommonParameters</span></span>
<span data-ttu-id="48cd8-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48cd8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48cd8-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48cd8-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48cd8-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48cd8-124">INPUTS</span></span>

### <span data-ttu-id="48cd8-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="48cd8-125">None</span></span>

## <span data-ttu-id="48cd8-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48cd8-126">OUTPUTS</span></span>

### <span data-ttu-id="48cd8-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="48cd8-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="48cd8-128">Note</span><span class="sxs-lookup"><span data-stu-id="48cd8-128">NOTES</span></span>

## <span data-ttu-id="48cd8-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48cd8-129">RELATED LINKS</span></span>
