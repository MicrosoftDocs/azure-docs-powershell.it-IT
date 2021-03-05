---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 9f53ddd628b313a02cf15ce6d80097f0b916c6f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001149"
---
# <span data-ttu-id="bd686-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="bd686-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="bd686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd686-102">SYNOPSIS</span></span>
<span data-ttu-id="bd686-103">Aggiunge una condizione a RewriteRule per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd686-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="bd686-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd686-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd686-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bd686-105">DESCRIPTION</span></span>
<span data-ttu-id="bd686-106">Il cmdlet **AzApplicationGatewayRewriteRuleCondition crea** una condizione della regola di riscrittura per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bd686-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="bd686-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd686-107">EXAMPLES</span></span>

### <span data-ttu-id="bd686-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bd686-108">Example 1</span></span>
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
<span data-ttu-id="bd686-109">Questo comando crea una condizione in una regola di riscrittura e archivia il risultato nella variabile $condition.</span><span class="sxs-lookup"><span data-stu-id="bd686-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="bd686-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd686-110">PARAMETERS</span></span>

### <span data-ttu-id="bd686-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd686-111">-DefaultProfile</span></span>
<span data-ttu-id="bd686-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd686-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd686-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="bd686-113">-IgnoreCase</span></span>
<span data-ttu-id="bd686-114">Impostare questo contrassegno per ignorare la distinzione tra maiuscole e minuscole nei criteri</span><span class="sxs-lookup"><span data-stu-id="bd686-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="bd686-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="bd686-115">-Negate</span></span>
<span data-ttu-id="bd686-116">Impostare questo flag per annullare la convalida della condizione</span><span class="sxs-lookup"><span data-stu-id="bd686-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="bd686-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="bd686-117">-Pattern</span></span>
<span data-ttu-id="bd686-118">Schema da cercare nell'intestazione variabile</span><span class="sxs-lookup"><span data-stu-id="bd686-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="bd686-119">-Variabile</span><span class="sxs-lookup"><span data-stu-id="bd686-119">-Variable</span></span>
<span data-ttu-id="bd686-120">Nome dell'intestazione su cui impostare la condizione</span><span class="sxs-lookup"><span data-stu-id="bd686-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="bd686-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd686-121">CommonParameters</span></span>
<span data-ttu-id="bd686-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd686-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bd686-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd686-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd686-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="bd686-124">INPUTS</span></span>

### <span data-ttu-id="bd686-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd686-125">None</span></span>

## <span data-ttu-id="bd686-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd686-126">OUTPUTS</span></span>

### <span data-ttu-id="bd686-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="bd686-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="bd686-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="bd686-128">NOTES</span></span>

## <span data-ttu-id="bd686-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd686-129">RELATED LINKS</span></span>
[<span data-ttu-id="bd686-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd686-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd686-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd686-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd686-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd686-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd686-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd686-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd686-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd686-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd686-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="bd686-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="bd686-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bd686-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
