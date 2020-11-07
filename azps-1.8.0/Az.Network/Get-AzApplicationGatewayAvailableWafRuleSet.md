---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: e550d00d1d952fb372db81ec87a35c701d6dedde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678624"
---
# <span data-ttu-id="55944-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="55944-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="55944-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55944-102">SYNOPSIS</span></span>
<span data-ttu-id="55944-103">Ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="55944-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="55944-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55944-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55944-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55944-105">DESCRIPTION</span></span>
<span data-ttu-id="55944-106">Il cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="55944-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="55944-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55944-107">EXAMPLES</span></span>

### <span data-ttu-id="55944-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="55944-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="55944-109">Questi comandi restituiscono tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="55944-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="55944-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55944-110">PARAMETERS</span></span>

### <span data-ttu-id="55944-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55944-111">-DefaultProfile</span></span>
<span data-ttu-id="55944-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55944-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55944-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55944-113">CommonParameters</span></span>
<span data-ttu-id="55944-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55944-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55944-115">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55944-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55944-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55944-116">INPUTS</span></span>

### <span data-ttu-id="55944-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="55944-117">None</span></span>

## <span data-ttu-id="55944-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55944-118">OUTPUTS</span></span>

### <span data-ttu-id="55944-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="55944-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="55944-120">Note</span><span class="sxs-lookup"><span data-stu-id="55944-120">NOTES</span></span>
<span data-ttu-id="55944-121">**List-AzApplicationGatewayAvailableWafRuleSets** è un alias per il cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="55944-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="55944-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55944-122">RELATED LINKS</span></span>
