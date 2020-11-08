---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192353"
---
# <span data-ttu-id="62a9b-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="62a9b-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="62a9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="62a9b-103">Crea un'esclusione per i criteri del firewall</span><span class="sxs-lookup"><span data-stu-id="62a9b-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="62a9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62a9b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62a9b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62a9b-105">DESCRIPTION</span></span>
<span data-ttu-id="62a9b-106">Cmdlet **New-AzApplicationGatewayFirewallPolicyExclusion** un nuovo elenco di regole di esclusione per i criteri firewall.</span><span class="sxs-lookup"><span data-stu-id="62a9b-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="62a9b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62a9b-107">EXAMPLES</span></span>

### <span data-ttu-id="62a9b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62a9b-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="62a9b-109">Questo comando crea una nuova voce di esclusione per la variabile denominata RequestHeaderNames e operator denominata StartsWith e Selector denominata XYZ.</span><span class="sxs-lookup"><span data-stu-id="62a9b-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="62a9b-110">La voce di esclusione viene salvata in $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="62a9b-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="62a9b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62a9b-111">PARAMETERS</span></span>

### <span data-ttu-id="62a9b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a9b-112">-DefaultProfile</span></span>
<span data-ttu-id="62a9b-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62a9b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62a9b-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="62a9b-114">-MatchVariable</span></span>
<span data-ttu-id="62a9b-115">Variabile da escludere.</span><span class="sxs-lookup"><span data-stu-id="62a9b-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a9b-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="62a9b-116">-Selector</span></span>
<span data-ttu-id="62a9b-117">Quando la variabile è una raccolta, operator usato per specificare gli elementi della raccolta a cui si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="62a9b-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="62a9b-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="62a9b-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="62a9b-119">Quando la variabile è una raccolta, usare il selettore per specificare gli elementi della raccolta a cui si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="62a9b-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a9b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a9b-120">CommonParameters</span></span>
<span data-ttu-id="62a9b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62a9b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a9b-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62a9b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a9b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62a9b-123">INPUTS</span></span>

### <span data-ttu-id="62a9b-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="62a9b-124">None</span></span>

## <span data-ttu-id="62a9b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62a9b-125">OUTPUTS</span></span>

### <span data-ttu-id="62a9b-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="62a9b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="62a9b-127">Note</span><span class="sxs-lookup"><span data-stu-id="62a9b-127">NOTES</span></span>

## <span data-ttu-id="62a9b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62a9b-128">RELATED LINKS</span></span>