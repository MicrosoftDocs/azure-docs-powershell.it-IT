---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021540"
---
# <span data-ttu-id="dd28d-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd28d-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="dd28d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd28d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd28d-103">Ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="dd28d-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="dd28d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd28d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd28d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd28d-105">DESCRIPTION</span></span>
<span data-ttu-id="dd28d-106">Il cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="dd28d-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="dd28d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd28d-107">EXAMPLES</span></span>

### <span data-ttu-id="dd28d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dd28d-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="dd28d-109">Questi comandi restituiscono tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="dd28d-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="dd28d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd28d-110">PARAMETERS</span></span>

### <span data-ttu-id="dd28d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd28d-111">-DefaultProfile</span></span>
<span data-ttu-id="dd28d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd28d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd28d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd28d-113">CommonParameters</span></span>
<span data-ttu-id="dd28d-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd28d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd28d-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd28d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd28d-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd28d-116">INPUTS</span></span>

### <span data-ttu-id="dd28d-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dd28d-117">None</span></span>

## <span data-ttu-id="dd28d-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd28d-118">OUTPUTS</span></span>

### <span data-ttu-id="dd28d-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="dd28d-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="dd28d-120">Note</span><span class="sxs-lookup"><span data-stu-id="dd28d-120">NOTES</span></span>
<span data-ttu-id="dd28d-121">**List-AzApplicationGatewayAvailableWafRuleSets** è un alias per il cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="dd28d-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="dd28d-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd28d-122">RELATED LINKS</span></span>
