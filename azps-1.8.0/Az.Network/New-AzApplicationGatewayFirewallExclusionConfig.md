---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 58060c488e778510822d9bc86a21de216447e0f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678373"
---
# <span data-ttu-id="466d2-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="466d2-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="466d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="466d2-102">SYNOPSIS</span></span>
<span data-ttu-id="466d2-103">Crea un nuovo elenco di regole di esclusione per Application Gateway WAF</span><span class="sxs-lookup"><span data-stu-id="466d2-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="466d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="466d2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="466d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="466d2-105">DESCRIPTION</span></span>
<span data-ttu-id="466d2-106">Cmdlet **New-AzApplicationGatewayFirewallExclusionConfig** un nuovo elenco di regole di esclusione per il gateway applicazione WAF.</span><span class="sxs-lookup"><span data-stu-id="466d2-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="466d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="466d2-107">EXAMPLES</span></span>

### <span data-ttu-id="466d2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="466d2-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="466d2-109">Questo comando crea una nuova regola di esclusione elenca la configurazione per la variabile denominata RequestHeaderNames e operator denominata StartsWith e Selector denominata XYZ.</span><span class="sxs-lookup"><span data-stu-id="466d2-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="466d2-110">La configurazione dell'elenco di esclusione viene salvata in $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="466d2-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="466d2-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="466d2-111">PARAMETERS</span></span>

### <span data-ttu-id="466d2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="466d2-112">-DefaultProfile</span></span>
<span data-ttu-id="466d2-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="466d2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="466d2-114">-Operator</span><span class="sxs-lookup"><span data-stu-id="466d2-114">-Operator</span></span>
<span data-ttu-id="466d2-115">Quando la variabile è una raccolta, usare il selettore per specificare gli elementi della raccolta a cui si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="466d2-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="466d2-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="466d2-116">-Selector</span></span>
<span data-ttu-id="466d2-117">Quando la variabile è una raccolta, operator usato per specificare gli elementi della raccolta a cui si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="466d2-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="466d2-118">-Variabile</span><span class="sxs-lookup"><span data-stu-id="466d2-118">-Variable</span></span>
<span data-ttu-id="466d2-119">Variabile da escludere.</span><span class="sxs-lookup"><span data-stu-id="466d2-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="466d2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="466d2-120">CommonParameters</span></span>
<span data-ttu-id="466d2-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="466d2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="466d2-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="466d2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="466d2-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="466d2-123">INPUTS</span></span>

### <span data-ttu-id="466d2-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="466d2-124">None</span></span>

## <span data-ttu-id="466d2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="466d2-125">OUTPUTS</span></span>

### <span data-ttu-id="466d2-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="466d2-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="466d2-127">Note</span><span class="sxs-lookup"><span data-stu-id="466d2-127">NOTES</span></span>

## <span data-ttu-id="466d2-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="466d2-128">RELATED LINKS</span></span>