---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032377"
---
# <span data-ttu-id="d3158-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d3158-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="d3158-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3158-102">SYNOPSIS</span></span>
<span data-ttu-id="d3158-103">Aggiunge una condizione a RewriteRule per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d3158-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="d3158-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3158-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3158-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3158-105">DESCRIPTION</span></span>
<span data-ttu-id="d3158-106">**Il cmdlet AzApplicationGatewayRewriteRuleCondition** crea una condizione di riscrittura della regola per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="d3158-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="d3158-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3158-107">EXAMPLES</span></span>

### <span data-ttu-id="d3158-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3158-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="d3158-109">Questo comando crea una condizione in una regola di riscrittura e archivia il risultato nella variabile denominata $condition.</span><span class="sxs-lookup"><span data-stu-id="d3158-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="d3158-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3158-110">PARAMETERS</span></span>

### <span data-ttu-id="d3158-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3158-111">-DefaultProfile</span></span>
<span data-ttu-id="d3158-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3158-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3158-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="d3158-113">-IgnoreCase</span></span>
<span data-ttu-id="d3158-114">Impostare questo contrassegno su Ignora maiuscole/minuscole nello schema</span><span class="sxs-lookup"><span data-stu-id="d3158-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3158-115">-Negazione</span><span class="sxs-lookup"><span data-stu-id="d3158-115">-Negate</span></span>
<span data-ttu-id="d3158-116">Impostare questo contrassegno per annullare la convalida della condizione</span><span class="sxs-lookup"><span data-stu-id="d3158-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3158-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="d3158-117">-Pattern</span></span>
<span data-ttu-id="d3158-118">Modello da cercare nell'intestazione della variabile</span><span class="sxs-lookup"><span data-stu-id="d3158-118">Pattern to look for in the Variable Header</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3158-119">-Variabile</span><span class="sxs-lookup"><span data-stu-id="d3158-119">-Variable</span></span>
<span data-ttu-id="d3158-120">Nome dell'intestazione in cui impostare la condizione</span><span class="sxs-lookup"><span data-stu-id="d3158-120">Name of the Header to set condition on it</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3158-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3158-121">CommonParameters</span></span>
<span data-ttu-id="d3158-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3158-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d3158-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3158-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3158-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3158-124">INPUTS</span></span>

### <span data-ttu-id="d3158-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d3158-125">None</span></span>

## <span data-ttu-id="d3158-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3158-126">OUTPUTS</span></span>

### <span data-ttu-id="d3158-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d3158-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="d3158-128">Note</span><span class="sxs-lookup"><span data-stu-id="d3158-128">NOTES</span></span>

## <span data-ttu-id="d3158-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3158-129">RELATED LINKS</span></span>
[<span data-ttu-id="d3158-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3158-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3158-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3158-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3158-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3158-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3158-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3158-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3158-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3158-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3158-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d3158-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d3158-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d3158-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
