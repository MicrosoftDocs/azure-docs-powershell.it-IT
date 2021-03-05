---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: b914e87729e97bb6b8af9ec59605290e0cc025bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978365"
---
# <span data-ttu-id="1b7b6-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="1b7b6-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="1b7b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="1b7b6-103">Recupera tutti i set di regole del firewall dell'applicazione Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="1b7b6-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="1b7b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b7b6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b7b6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1b7b6-105">DESCRIPTION</span></span>
<span data-ttu-id="1b7b6-106">Il cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** ottiene tutti i set di regole del firewall dell'applicazione Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="1b7b6-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="1b7b6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b7b6-107">EXAMPLES</span></span>

### <span data-ttu-id="1b7b6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1b7b6-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="1b7b6-109">Questo comando restituisce tutti i set di regole firewall dell'applicazione Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="1b7b6-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="1b7b6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b7b6-110">PARAMETERS</span></span>

### <span data-ttu-id="1b7b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b7b6-111">-DefaultProfile</span></span>
<span data-ttu-id="1b7b6-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b7b6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b7b6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b7b6-113">CommonParameters</span></span>
<span data-ttu-id="1b7b6-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b7b6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b7b6-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1b7b6-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b7b6-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="1b7b6-116">INPUTS</span></span>

### <span data-ttu-id="1b7b6-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b7b6-117">None</span></span>

## <span data-ttu-id="1b7b6-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b7b6-118">OUTPUTS</span></span>

### <span data-ttu-id="1b7b6-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="1b7b6-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="1b7b6-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="1b7b6-120">NOTES</span></span>
<span data-ttu-id="1b7b6-121">**List-AzApplicationGatewayAvailableWafRuleSets** è un alias per il cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet.**</span><span class="sxs-lookup"><span data-stu-id="1b7b6-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="1b7b6-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b7b6-122">RELATED LINKS</span></span>
