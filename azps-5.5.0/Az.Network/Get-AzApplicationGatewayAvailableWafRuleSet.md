---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189871"
---
# <span data-ttu-id="24e71-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="24e71-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="24e71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24e71-102">SYNOPSIS</span></span>
<span data-ttu-id="24e71-103">Recupera tutti i set di regole del firewall dell'applicazione Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="24e71-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="24e71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24e71-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24e71-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="24e71-105">DESCRIPTION</span></span>
<span data-ttu-id="24e71-106">Il cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** ottiene tutti i set di regole del firewall dell'applicazione Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="24e71-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="24e71-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24e71-107">EXAMPLES</span></span>

### <span data-ttu-id="24e71-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="24e71-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="24e71-109">Questo comando restituisce tutti i set di regole firewall dell'applicazione Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="24e71-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="24e71-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24e71-110">PARAMETERS</span></span>

### <span data-ttu-id="24e71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e71-111">-DefaultProfile</span></span>
<span data-ttu-id="24e71-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24e71-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24e71-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e71-113">CommonParameters</span></span>
<span data-ttu-id="24e71-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e71-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e71-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="24e71-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e71-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="24e71-116">INPUTS</span></span>

### <span data-ttu-id="24e71-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="24e71-117">None</span></span>

## <span data-ttu-id="24e71-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24e71-118">OUTPUTS</span></span>

### <span data-ttu-id="24e71-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="24e71-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="24e71-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="24e71-120">NOTES</span></span>
<span data-ttu-id="24e71-121">**List-AzApplicationGatewayAvailableWafRuleSets** è un alias per il cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet.**</span><span class="sxs-lookup"><span data-stu-id="24e71-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="24e71-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24e71-122">RELATED LINKS</span></span>
