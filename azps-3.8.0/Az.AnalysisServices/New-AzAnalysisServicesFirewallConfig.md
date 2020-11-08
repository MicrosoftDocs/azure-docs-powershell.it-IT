---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 056a6e006cc0b1b3fd703757dcc07cbb0a8be987
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019139"
---
# <span data-ttu-id="9c758-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="9c758-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="9c758-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c758-102">SYNOPSIS</span></span>
<span data-ttu-id="9c758-103">Crea una nuova configurazione del firewall di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9c758-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="9c758-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c758-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c758-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c758-105">DESCRIPTION</span></span>
<span data-ttu-id="9c758-106">La New-AzAnalysisServicesFirewallConfig crea un nuovo oggetto di configurazione del firewall</span><span class="sxs-lookup"><span data-stu-id="9c758-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="9c758-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c758-107">EXAMPLES</span></span>

### <span data-ttu-id="9c758-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9c758-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="9c758-109">Crea un oggetto di configurazione firewall con due regole, consentendo anche l'accesso dal servizio Power BI.</span><span class="sxs-lookup"><span data-stu-id="9c758-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="9c758-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c758-110">PARAMETERS</span></span>

### <span data-ttu-id="9c758-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c758-111">-DefaultProfile</span></span>
<span data-ttu-id="9c758-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c758-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c758-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="9c758-113">-EnablePowerBIService</span></span>
<span data-ttu-id="9c758-114">Un contrassegno per indicare se il firewall consente l'accesso da Power BI</span><span class="sxs-lookup"><span data-stu-id="9c758-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c758-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="9c758-115">-FirewallRule</span></span>
<span data-ttu-id="9c758-116">Elenco delle regole del firewall</span><span class="sxs-lookup"><span data-stu-id="9c758-116">A list of firewall rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c758-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c758-117">CommonParameters</span></span>
<span data-ttu-id="9c758-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c758-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c758-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c758-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c758-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c758-120">INPUTS</span></span>

### <span data-ttu-id="9c758-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. PowerShell. Cmdlets. AnalysisServices, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9c758-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9c758-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c758-122">OUTPUTS</span></span>

### <span data-ttu-id="9c758-123">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="9c758-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="9c758-124">Note</span><span class="sxs-lookup"><span data-stu-id="9c758-124">NOTES</span></span>

## <span data-ttu-id="9c758-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c758-125">RELATED LINKS</span></span>

[<span data-ttu-id="9c758-126">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9c758-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)