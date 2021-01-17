---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 056a6e006cc0b1b3fd703757dcc07cbb0a8be987
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479083"
---
# <span data-ttu-id="d675c-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="d675c-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="d675c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d675c-102">SYNOPSIS</span></span>
<span data-ttu-id="d675c-103">Crea una nuova configurazione del firewall di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="d675c-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="d675c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d675c-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d675c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d675c-105">DESCRIPTION</span></span>
<span data-ttu-id="d675c-106">La New-AzAnalysisServicesFirewallConfig crea un nuovo oggetto di configurazione del firewall</span><span class="sxs-lookup"><span data-stu-id="d675c-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="d675c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d675c-107">EXAMPLES</span></span>

### <span data-ttu-id="d675c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d675c-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="d675c-109">Crea un oggetto di configurazione firewall con due regole, consentendo anche l'accesso dal servizio Power BI.</span><span class="sxs-lookup"><span data-stu-id="d675c-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="d675c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d675c-110">PARAMETERS</span></span>

### <span data-ttu-id="d675c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d675c-111">-DefaultProfile</span></span>
<span data-ttu-id="d675c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d675c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d675c-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="d675c-113">-EnablePowerBIService</span></span>
<span data-ttu-id="d675c-114">Un contrassegno per indicare se il firewall consente l'accesso da Power BI</span><span class="sxs-lookup"><span data-stu-id="d675c-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="d675c-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="d675c-115">-FirewallRule</span></span>
<span data-ttu-id="d675c-116">Elenco delle regole del firewall</span><span class="sxs-lookup"><span data-stu-id="d675c-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="d675c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d675c-117">CommonParameters</span></span>
<span data-ttu-id="d675c-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d675c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d675c-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d675c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d675c-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d675c-120">INPUTS</span></span>

### <span data-ttu-id="d675c-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. PowerShell. Cmdlets. AnalysisServices, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d675c-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d675c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d675c-122">OUTPUTS</span></span>

### <span data-ttu-id="d675c-123">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="d675c-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="d675c-124">Note</span><span class="sxs-lookup"><span data-stu-id="d675c-124">NOTES</span></span>

## <span data-ttu-id="d675c-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d675c-125">RELATED LINKS</span></span>

[<span data-ttu-id="d675c-126">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d675c-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)