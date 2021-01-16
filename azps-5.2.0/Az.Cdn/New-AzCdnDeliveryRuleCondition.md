---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358651"
---
# <span data-ttu-id="4f7ec-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="4f7ec-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="4f7ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4f7ec-103">Crea una condizione della regola di recapito.</span><span class="sxs-lookup"><span data-stu-id="4f7ec-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="4f7ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f7ec-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f7ec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f7ec-105">DESCRIPTION</span></span>
<span data-ttu-id="4f7ec-106">Il cmdlet **New-AzCdnDeliveryRule** crea una regola di recapito per la creazione di endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="4f7ec-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="4f7ec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f7ec-107">EXAMPLES</span></span>

### <span data-ttu-id="4f7ec-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4f7ec-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="4f7ec-109">Creare una condizione semplice.</span><span class="sxs-lookup"><span data-stu-id="4f7ec-109">Create a simple condition.</span></span>

## <span data-ttu-id="4f7ec-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f7ec-110">PARAMETERS</span></span>

### <span data-ttu-id="4f7ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f7ec-111">-DefaultProfile</span></span>
<span data-ttu-id="4f7ec-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f7ec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f7ec-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="4f7ec-113">-MatchValue</span></span>
<span data-ttu-id="4f7ec-114">Elenco di valori di corrispondenza possibili.</span><span class="sxs-lookup"><span data-stu-id="4f7ec-114">List of possible match values.</span></span>

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

### <span data-ttu-id="4f7ec-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="4f7ec-115">-MatchVariable</span></span>
<span data-ttu-id="4f7ec-116">Corrispondere alla variabile della condizione.</span><span class="sxs-lookup"><span data-stu-id="4f7ec-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="4f7ec-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="4f7ec-117">-NegateCondition</span></span>
<span data-ttu-id="4f7ec-118">Descrive se il risultato di questa condizione deve essere negato.</span><span class="sxs-lookup"><span data-stu-id="4f7ec-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="4f7ec-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="4f7ec-119">-Operator</span></span>
<span data-ttu-id="4f7ec-120">Descrive l'operatore che deve essere abbinato</span><span class="sxs-lookup"><span data-stu-id="4f7ec-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="4f7ec-121">-Selector</span><span class="sxs-lookup"><span data-stu-id="4f7ec-121">-Selector</span></span>
<span data-ttu-id="4f7ec-122">Nome del selettore da abbinare</span><span class="sxs-lookup"><span data-stu-id="4f7ec-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="4f7ec-123">-Transform</span><span class="sxs-lookup"><span data-stu-id="4f7ec-123">-Transform</span></span>
<span data-ttu-id="4f7ec-124">Trasforma da applicare prima della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="4f7ec-124">Transform to apply before matching.</span></span>
<span data-ttu-id="4f7ec-125">I valori possibili sono maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="4f7ec-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="4f7ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f7ec-126">CommonParameters</span></span>
<span data-ttu-id="4f7ec-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f7ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f7ec-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f7ec-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f7ec-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f7ec-129">INPUTS</span></span>

### <span data-ttu-id="4f7ec-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4f7ec-130">None</span></span>

## <span data-ttu-id="4f7ec-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f7ec-131">OUTPUTS</span></span>

### <span data-ttu-id="4f7ec-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="4f7ec-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="4f7ec-133">Note</span><span class="sxs-lookup"><span data-stu-id="4f7ec-133">NOTES</span></span>

## <span data-ttu-id="4f7ec-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f7ec-134">RELATED LINKS</span></span>
