---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: f3c84b22a9ea8c913cb520ae913fff89ae9470ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676125"
---
# <span data-ttu-id="78ccb-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="78ccb-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="78ccb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="78ccb-103">Crea una nuova configurazione del firewall di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="78ccb-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="78ccb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78ccb-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78ccb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="78ccb-106">La New-AzAnalysisServicesFirewallConfig crea un nuovo oggetto di configurazione del firewall</span><span class="sxs-lookup"><span data-stu-id="78ccb-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="78ccb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78ccb-107">EXAMPLES</span></span>

### <span data-ttu-id="78ccb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="78ccb-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="78ccb-109">Crea un oggetto di configurazione firewall con due regole, consentendo anche l'accesso dal servizio Power BI.</span><span class="sxs-lookup"><span data-stu-id="78ccb-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="78ccb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78ccb-110">PARAMETERS</span></span>

### <span data-ttu-id="78ccb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ccb-111">-DefaultProfile</span></span>
<span data-ttu-id="78ccb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78ccb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78ccb-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="78ccb-113">-EnablePowerBIService</span></span>
<span data-ttu-id="78ccb-114">Un contrassegno per indicare se il firewall consente l'accesso da Power BI</span><span class="sxs-lookup"><span data-stu-id="78ccb-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="78ccb-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="78ccb-115">-FirewallRule</span></span>
<span data-ttu-id="78ccb-116">Elenco delle regole del firewall</span><span class="sxs-lookup"><span data-stu-id="78ccb-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="78ccb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ccb-117">CommonParameters</span></span>
<span data-ttu-id="78ccb-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78ccb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ccb-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78ccb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ccb-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78ccb-120">INPUTS</span></span>

### <span data-ttu-id="78ccb-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. PowerShell. Cmdlets. AnalysisServices, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="78ccb-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="78ccb-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78ccb-122">OUTPUTS</span></span>

### <span data-ttu-id="78ccb-123">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="78ccb-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="78ccb-124">Note</span><span class="sxs-lookup"><span data-stu-id="78ccb-124">NOTES</span></span>

## <span data-ttu-id="78ccb-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78ccb-125">RELATED LINKS</span></span>

[<span data-ttu-id="78ccb-126">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="78ccb-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)