---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182406"
---
# <span data-ttu-id="e95b2-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e95b2-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="e95b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e95b2-102">SYNOPSIS</span></span>
<span data-ttu-id="e95b2-103">Crea una nuova regola del firewall di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="e95b2-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="e95b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e95b2-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e95b2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e95b2-105">DESCRIPTION</span></span>
<span data-ttu-id="e95b2-106">LNew-AzAnalysisServicesFirewallRule crea un nuovo oggetto regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="e95b2-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="e95b2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e95b2-107">EXAMPLES</span></span>

### <span data-ttu-id="e95b2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e95b2-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="e95b2-109">Crea una regola del firewall denominata regola1 con intervallo di inizio 0.0.0.0 e intervallo finale 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="e95b2-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="e95b2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e95b2-110">PARAMETERS</span></span>

### <span data-ttu-id="e95b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95b2-111">-DefaultProfile</span></span>
<span data-ttu-id="e95b2-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e95b2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e95b2-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="e95b2-113">-FirewallRuleName</span></span>
<span data-ttu-id="e95b2-114">Nome della regola del firewall</span><span class="sxs-lookup"><span data-stu-id="e95b2-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="e95b2-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="e95b2-115">-RangeEnd</span></span>
<span data-ttu-id="e95b2-116">Fine dell'intervallo di una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="e95b2-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="e95b2-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="e95b2-117">-RangeStart</span></span>
<span data-ttu-id="e95b2-118">L'inizio dell'intervallo di una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="e95b2-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="e95b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95b2-119">CommonParameters</span></span>
<span data-ttu-id="e95b2-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95b2-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e95b2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95b2-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="e95b2-122">INPUTS</span></span>

### <span data-ttu-id="e95b2-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e95b2-123">System.String</span></span>

## <span data-ttu-id="e95b2-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e95b2-124">OUTPUTS</span></span>

### <span data-ttu-id="e95b2-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e95b2-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="e95b2-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="e95b2-126">NOTES</span></span>

## <span data-ttu-id="e95b2-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e95b2-127">RELATED LINKS</span></span>

[<span data-ttu-id="e95b2-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="e95b2-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)