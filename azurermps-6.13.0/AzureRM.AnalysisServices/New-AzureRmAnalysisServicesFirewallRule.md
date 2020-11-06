---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 2a47c97ea189d4064edae7a871e21465d866f1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513999"
---
# <span data-ttu-id="f3457-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3457-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="f3457-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3457-102">SYNOPSIS</span></span>
<span data-ttu-id="f3457-103">Crea una nuova regola del firewall di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f3457-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3457-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3457-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String>
 [-RangeEnd] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3457-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3457-105">DESCRIPTION</span></span>
<span data-ttu-id="f3457-106">La New-AzureRmAnalysisServicesFirewallRule crea un nuovo oggetto della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="f3457-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="f3457-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3457-107">EXAMPLES</span></span>

### <span data-ttu-id="f3457-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f3457-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="f3457-109">Crea una regola del firewall denominata Rule1 con l'intervallo di inizio 0.0.0.0 e l'intervallo finale 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="f3457-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="f3457-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3457-110">PARAMETERS</span></span>

### <span data-ttu-id="f3457-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3457-111">-DefaultProfile</span></span>
<span data-ttu-id="f3457-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3457-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3457-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f3457-113">-FirewallRuleName</span></span>
<span data-ttu-id="f3457-114">Nome della regola del firewall</span><span class="sxs-lookup"><span data-stu-id="f3457-114">Name of firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3457-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="f3457-115">-RangeEnd</span></span>
<span data-ttu-id="f3457-116">Fine dell'intervallo di una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="f3457-116">The range end of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3457-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="f3457-117">-RangeStart</span></span>
<span data-ttu-id="f3457-118">Inizio intervallo di una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="f3457-118">The range start of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3457-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3457-119">CommonParameters</span></span>
<span data-ttu-id="f3457-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3457-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3457-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3457-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3457-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3457-122">INPUTS</span></span>

### <span data-ttu-id="f3457-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f3457-123">System.String</span></span>

## <span data-ttu-id="f3457-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3457-124">OUTPUTS</span></span>

### <span data-ttu-id="f3457-125">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f3457-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="f3457-126">Note</span><span class="sxs-lookup"><span data-stu-id="f3457-126">NOTES</span></span>

## <span data-ttu-id="f3457-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3457-127">RELATED LINKS</span></span>

[<span data-ttu-id="f3457-128">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="f3457-128">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
