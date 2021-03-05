---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 029ba60169ee22d86d9e54661296f04bf2242713
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964205"
---
# <span data-ttu-id="51518-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="51518-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="51518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51518-102">SYNOPSIS</span></span>
<span data-ttu-id="51518-103">Crea un nuovo elenco di regole di esclusione per il gateway applicazioni waf</span><span class="sxs-lookup"><span data-stu-id="51518-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="51518-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51518-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51518-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="51518-105">DESCRIPTION</span></span>
<span data-ttu-id="51518-106">Il cmdlet **New-AzApplicationGatewayFirewallExconfigConfig** è un nuovo elenco di regole di esclusione per il gateway di applicazione waf.</span><span class="sxs-lookup"><span data-stu-id="51518-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="51518-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51518-107">EXAMPLES</span></span>

### <span data-ttu-id="51518-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="51518-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="51518-109">Questo comando crea una nuova regola di esclusione che elenca la configurazione per la variabile denominata RequestHeaderNames e l'operatore StartsWith e Selector denominati xyz.</span><span class="sxs-lookup"><span data-stu-id="51518-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="51518-110">La configurazione dell'elenco di esclusione viene salvata in $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="51518-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="51518-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51518-111">PARAMETERS</span></span>

### <span data-ttu-id="51518-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51518-112">-DefaultProfile</span></span>
<span data-ttu-id="51518-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51518-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51518-114">-Operatore</span><span class="sxs-lookup"><span data-stu-id="51518-114">-Operator</span></span>
<span data-ttu-id="51518-115">Quando la variabile è una raccolta, usare il selettore per specificare a quali elementi della raccolta si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="51518-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="51518-116">-Selettore</span><span class="sxs-lookup"><span data-stu-id="51518-116">-Selector</span></span>
<span data-ttu-id="51518-117">Quando la variabile è una raccolta, l'operatore usato per specificare a quali elementi della raccolta si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="51518-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="51518-118">-Variabile</span><span class="sxs-lookup"><span data-stu-id="51518-118">-Variable</span></span>
<span data-ttu-id="51518-119">La variabile da escludere.</span><span class="sxs-lookup"><span data-stu-id="51518-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="51518-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51518-120">CommonParameters</span></span>
<span data-ttu-id="51518-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51518-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51518-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51518-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51518-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="51518-123">INPUTS</span></span>

### <span data-ttu-id="51518-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="51518-124">None</span></span>

## <span data-ttu-id="51518-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51518-125">OUTPUTS</span></span>

### <span data-ttu-id="51518-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExapplication</span><span class="sxs-lookup"><span data-stu-id="51518-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="51518-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="51518-127">NOTES</span></span>

## <span data-ttu-id="51518-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51518-128">RELATED LINKS</span></span>
