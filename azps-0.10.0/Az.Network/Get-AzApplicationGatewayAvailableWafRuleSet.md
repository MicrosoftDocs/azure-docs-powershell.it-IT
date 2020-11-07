---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableWafRuleSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: f8f8411a40ddbc4d0e2f0e4b508385717e0c4173
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860913"
---
# <span data-ttu-id="7b7e9-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="7b7e9-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="7b7e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b7e9-102">SYNOPSIS</span></span>
<span data-ttu-id="7b7e9-103">Ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="7b7e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b7e9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b7e9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b7e9-105">DESCRIPTION</span></span>
<span data-ttu-id="7b7e9-106">Il cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="7b7e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b7e9-107">EXAMPLES</span></span>

### <span data-ttu-id="7b7e9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b7e9-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="7b7e9-109">Questi comandi restituiscono tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="7b7e9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b7e9-110">PARAMETERS</span></span>

### <span data-ttu-id="7b7e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b7e9-111">-DefaultProfile</span></span>
<span data-ttu-id="7b7e9-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b7e9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b7e9-113">CommonParameters</span></span>
<span data-ttu-id="7b7e9-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b7e9-115">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b7e9-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b7e9-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b7e9-116">INPUTS</span></span>

### <span data-ttu-id="7b7e9-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7b7e9-117">None</span></span>

## <span data-ttu-id="7b7e9-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b7e9-118">OUTPUTS</span></span>

### <span data-ttu-id="7b7e9-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="7b7e9-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="7b7e9-120">Note</span><span class="sxs-lookup"><span data-stu-id="7b7e9-120">NOTES</span></span>
<span data-ttu-id="7b7e9-121">**List-AzApplicationGatewayAvailableWafRuleSet** è un alias per il cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="7b7e9-121">**List-AzApplicationGatewayAvailableWafRuleSet** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="7b7e9-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b7e9-122">RELATED LINKS</span></span>

