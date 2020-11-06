---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519486"
---
# <span data-ttu-id="f14e9-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f14e9-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="f14e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f14e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f14e9-103">Crea una nuova regola del firewall di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f14e9-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f14e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f14e9-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## <span data-ttu-id="f14e9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f14e9-105">DESCRIPTION</span></span>
<span data-ttu-id="f14e9-106">La New-AzureRmAnalysisServicesFirewallRule crea un nuovo oggetto della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="f14e9-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="f14e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f14e9-107">EXAMPLES</span></span>

### <span data-ttu-id="f14e9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f14e9-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="f14e9-109">Crea una regola del firewall denominata Rule1 con l'intervallo di inizio 0.0.0.0 e l'intervallo finale 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="f14e9-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="f14e9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f14e9-110">PARAMETERS</span></span>

### <span data-ttu-id="f14e9-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f14e9-111">-FirewallRuleName</span></span>
<span data-ttu-id="f14e9-112">Nome della regola del firewall</span><span class="sxs-lookup"><span data-stu-id="f14e9-112">Name of firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f14e9-113">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="f14e9-113">-RangeStart</span></span>
<span data-ttu-id="f14e9-114">Inizio intervallo di una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="f14e9-114">The range start of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f14e9-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="f14e9-115">-RangeEnd</span></span>
<span data-ttu-id="f14e9-116">Fine dell'intervallo di una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="f14e9-116">The range end of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="f14e9-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f14e9-117">INPUTS</span></span>

## <span data-ttu-id="f14e9-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f14e9-118">OUTPUTS</span></span>

### <span data-ttu-id="f14e9-119">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f14e9-119">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="f14e9-120">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f14e9-120">RELATED LINKS</span></span>

[<span data-ttu-id="f14e9-121">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="f14e9-121">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
