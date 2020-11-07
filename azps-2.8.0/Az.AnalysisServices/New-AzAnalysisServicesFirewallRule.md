---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 7fb766bfa65d37fd8491e93593b3ea423938fd3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676123"
---
# <span data-ttu-id="4249d-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4249d-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="4249d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4249d-102">SYNOPSIS</span></span>
<span data-ttu-id="4249d-103">Crea una nuova regola del firewall di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="4249d-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="4249d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4249d-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4249d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4249d-105">DESCRIPTION</span></span>
<span data-ttu-id="4249d-106">La New-AzAnalysisServicesFirewallRule crea un nuovo oggetto della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="4249d-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="4249d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4249d-107">EXAMPLES</span></span>

### <span data-ttu-id="4249d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4249d-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="4249d-109">Crea una regola del firewall denominata Rule1 con l'intervallo di inizio 0.0.0.0 e l'intervallo finale 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="4249d-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="4249d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4249d-110">PARAMETERS</span></span>

### <span data-ttu-id="4249d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4249d-111">-DefaultProfile</span></span>
<span data-ttu-id="4249d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4249d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4249d-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="4249d-113">-FirewallRuleName</span></span>
<span data-ttu-id="4249d-114">Nome della regola del firewall</span><span class="sxs-lookup"><span data-stu-id="4249d-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="4249d-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="4249d-115">-RangeEnd</span></span>
<span data-ttu-id="4249d-116">Fine dell'intervallo di una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="4249d-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="4249d-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="4249d-117">-RangeStart</span></span>
<span data-ttu-id="4249d-118">Inizio intervallo di una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="4249d-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="4249d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4249d-119">CommonParameters</span></span>
<span data-ttu-id="4249d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4249d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4249d-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4249d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4249d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4249d-122">INPUTS</span></span>

### <span data-ttu-id="4249d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4249d-123">System.String</span></span>

## <span data-ttu-id="4249d-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4249d-124">OUTPUTS</span></span>

### <span data-ttu-id="4249d-125">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4249d-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="4249d-126">Note</span><span class="sxs-lookup"><span data-stu-id="4249d-126">NOTES</span></span>

## <span data-ttu-id="4249d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4249d-127">RELATED LINKS</span></span>

[<span data-ttu-id="4249d-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="4249d-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)