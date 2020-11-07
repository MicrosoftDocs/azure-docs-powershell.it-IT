---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 830b561a3d46e23f083d77dcac627b28f7dbb94e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675540"
---
# <span data-ttu-id="09798-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="09798-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="09798-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09798-102">SYNOPSIS</span></span>
<span data-ttu-id="09798-103">Crea una condizione della regola di recapito.</span><span class="sxs-lookup"><span data-stu-id="09798-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="09798-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09798-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> -MatchValue <String[]>
 [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09798-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09798-105">DESCRIPTION</span></span>
<span data-ttu-id="09798-106">Il cmdlet **New-AzCdnDeliveryRule** crea una regola di recapito per la creazione di endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="09798-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="09798-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09798-107">EXAMPLES</span></span>

### <span data-ttu-id="09798-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09798-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="09798-109">Creare una condizione semplice.</span><span class="sxs-lookup"><span data-stu-id="09798-109">Create a simple condition.</span></span>

## <span data-ttu-id="09798-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09798-110">PARAMETERS</span></span>

### <span data-ttu-id="09798-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09798-111">-DefaultProfile</span></span>
<span data-ttu-id="09798-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09798-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09798-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="09798-113">-MatchValue</span></span>
<span data-ttu-id="09798-114">Elenco di valori di corrispondenza possibili.</span><span class="sxs-lookup"><span data-stu-id="09798-114">List of possible match values.</span></span>

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

### <span data-ttu-id="09798-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="09798-115">-MatchVariable</span></span>
<span data-ttu-id="09798-116">Corrispondere alla variabile della condizione.</span><span class="sxs-lookup"><span data-stu-id="09798-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="09798-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="09798-117">-NegateCondition</span></span>
<span data-ttu-id="09798-118">Descrive se il risultato di questa condizione deve essere negato.</span><span class="sxs-lookup"><span data-stu-id="09798-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="09798-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="09798-119">-Operator</span></span>
<span data-ttu-id="09798-120">Descrive l'operatore che deve essere abbinato</span><span class="sxs-lookup"><span data-stu-id="09798-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="09798-121">-Transform</span><span class="sxs-lookup"><span data-stu-id="09798-121">-Transform</span></span>
<span data-ttu-id="09798-122">Trasforma da applicare prima della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="09798-122">Transform to apply before matching.</span></span>
<span data-ttu-id="09798-123">I valori possibili sono maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="09798-123">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="09798-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09798-124">CommonParameters</span></span>
<span data-ttu-id="09798-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09798-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09798-126">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09798-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09798-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09798-127">INPUTS</span></span>

### <span data-ttu-id="09798-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="09798-128">None</span></span>

## <span data-ttu-id="09798-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09798-129">OUTPUTS</span></span>

### <span data-ttu-id="09798-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="09798-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="09798-131">Note</span><span class="sxs-lookup"><span data-stu-id="09798-131">NOTES</span></span>

## <span data-ttu-id="09798-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09798-132">RELATED LINKS</span></span>
