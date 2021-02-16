---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179782"
---
# <span data-ttu-id="d50f7-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="d50f7-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="d50f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d50f7-102">SYNOPSIS</span></span>
<span data-ttu-id="d50f7-103">Crea un nuovo elenco di regole di esclusione per il gateway applicazioni waf</span><span class="sxs-lookup"><span data-stu-id="d50f7-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="d50f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d50f7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d50f7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d50f7-105">DESCRIPTION</span></span>
<span data-ttu-id="d50f7-106">Il cmdlet **New-AzApplicationGatewayFirewallExconfigConfig** è un nuovo elenco di regole di esclusione per il gateway di applicazione waf.</span><span class="sxs-lookup"><span data-stu-id="d50f7-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="d50f7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d50f7-107">EXAMPLES</span></span>

### <span data-ttu-id="d50f7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d50f7-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="d50f7-109">Questo comando crea una nuova regola di esclusione che elenca la configurazione per la variabile denominata RequestHeaderNames e l'operatore StartsWith e Selector denominati xyz.</span><span class="sxs-lookup"><span data-stu-id="d50f7-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="d50f7-110">La configurazione dell'elenco di esclusione viene salvata in $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="d50f7-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="d50f7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d50f7-111">PARAMETERS</span></span>

### <span data-ttu-id="d50f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d50f7-112">-DefaultProfile</span></span>
<span data-ttu-id="d50f7-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d50f7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d50f7-114">-Operatore</span><span class="sxs-lookup"><span data-stu-id="d50f7-114">-Operator</span></span>
<span data-ttu-id="d50f7-115">Quando la variabile è una raccolta, usare il selettore per specificare a quali elementi della raccolta si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="d50f7-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="d50f7-116">-Selettore</span><span class="sxs-lookup"><span data-stu-id="d50f7-116">-Selector</span></span>
<span data-ttu-id="d50f7-117">Quando la variabile è una raccolta, l'operatore usato per specificare a quali elementi della raccolta si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="d50f7-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="d50f7-118">-Variabile</span><span class="sxs-lookup"><span data-stu-id="d50f7-118">-Variable</span></span>
<span data-ttu-id="d50f7-119">La variabile da escludere.</span><span class="sxs-lookup"><span data-stu-id="d50f7-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="d50f7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d50f7-120">CommonParameters</span></span>
<span data-ttu-id="d50f7-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d50f7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d50f7-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d50f7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d50f7-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="d50f7-123">INPUTS</span></span>

### <span data-ttu-id="d50f7-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d50f7-124">None</span></span>

## <span data-ttu-id="d50f7-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d50f7-125">OUTPUTS</span></span>

### <span data-ttu-id="d50f7-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExapplication</span><span class="sxs-lookup"><span data-stu-id="d50f7-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="d50f7-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="d50f7-127">NOTES</span></span>

## <span data-ttu-id="d50f7-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d50f7-128">RELATED LINKS</span></span>
