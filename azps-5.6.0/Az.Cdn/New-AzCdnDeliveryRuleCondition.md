---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 6367910117ff00219c3194a06bb51754913df063
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009214"
---
# <span data-ttu-id="51f40-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="51f40-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="51f40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51f40-102">SYNOPSIS</span></span>
<span data-ttu-id="51f40-103">Crea una condizione della regola di recapito.</span><span class="sxs-lookup"><span data-stu-id="51f40-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="51f40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51f40-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51f40-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="51f40-105">DESCRIPTION</span></span>
<span data-ttu-id="51f40-106">Il cmdlet **New-AzCdnDeliveryRule** crea una regola di recapito per la creazione dell'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="51f40-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="51f40-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51f40-107">EXAMPLES</span></span>

### <span data-ttu-id="51f40-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="51f40-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="51f40-109">Creare una condizione semplice.</span><span class="sxs-lookup"><span data-stu-id="51f40-109">Create a simple condition.</span></span>

## <span data-ttu-id="51f40-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51f40-110">PARAMETERS</span></span>

### <span data-ttu-id="51f40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f40-111">-DefaultProfile</span></span>
<span data-ttu-id="51f40-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51f40-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51f40-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="51f40-113">-MatchValue</span></span>
<span data-ttu-id="51f40-114">Elenco di valori di corrispondenza possibili.</span><span class="sxs-lookup"><span data-stu-id="51f40-114">List of possible match values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f40-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="51f40-115">-MatchVariable</span></span>
<span data-ttu-id="51f40-116">Variabile corrispondente della condizione.</span><span class="sxs-lookup"><span data-stu-id="51f40-116">Match variable of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f40-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="51f40-117">-NegateCondition</span></span>
<span data-ttu-id="51f40-118">Descrive se il risultato di questa condizione deve essere negata.</span><span class="sxs-lookup"><span data-stu-id="51f40-118">Describes if the result of this condition should be negated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f40-119">-Operatore</span><span class="sxs-lookup"><span data-stu-id="51f40-119">-Operator</span></span>
<span data-ttu-id="51f40-120">Descrive l'operatore di cui trovare una corrispondenza</span><span class="sxs-lookup"><span data-stu-id="51f40-120">Describes operator to be matched</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f40-121">-Selettore</span><span class="sxs-lookup"><span data-stu-id="51f40-121">-Selector</span></span>
<span data-ttu-id="51f40-122">Nome del selettore di cui trovare una corrispondenza</span><span class="sxs-lookup"><span data-stu-id="51f40-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="51f40-123">-Transform</span><span class="sxs-lookup"><span data-stu-id="51f40-123">-Transform</span></span>
<span data-ttu-id="51f40-124">Trasformazione da applicare prima della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="51f40-124">Transform to apply before matching.</span></span>
<span data-ttu-id="51f40-125">I valori possibili sono Minuscole e Tutto maiuscole</span><span class="sxs-lookup"><span data-stu-id="51f40-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="51f40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f40-126">CommonParameters</span></span>
<span data-ttu-id="51f40-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f40-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51f40-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f40-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="51f40-129">INPUTS</span></span>

### <span data-ttu-id="51f40-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="51f40-130">None</span></span>

## <span data-ttu-id="51f40-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51f40-131">OUTPUTS</span></span>

### <span data-ttu-id="51f40-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="51f40-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="51f40-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="51f40-133">NOTES</span></span>

## <span data-ttu-id="51f40-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51f40-134">RELATED LINKS</span></span>
