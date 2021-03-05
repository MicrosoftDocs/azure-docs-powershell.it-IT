---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: bd958c9157a5e47b1fc4a878c9ce72405490ec2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005005"
---
# <span data-ttu-id="fdb27-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="fdb27-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="fdb27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdb27-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb27-103">Crea una nuova configurazione del firewall di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="fdb27-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="fdb27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdb27-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdb27-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fdb27-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb27-106">LNew-AzAnalysisServicesFirewallConfig crea un nuovo oggetto configurazione firewall</span><span class="sxs-lookup"><span data-stu-id="fdb27-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="fdb27-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdb27-107">EXAMPLES</span></span>

### <span data-ttu-id="fdb27-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fdb27-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="fdb27-109">Crea un oggetto configurazione firewall con due regole e allo stesso tempo abilita l'accesso dal servizio Power BI.</span><span class="sxs-lookup"><span data-stu-id="fdb27-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="fdb27-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdb27-110">PARAMETERS</span></span>

### <span data-ttu-id="fdb27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb27-111">-DefaultProfile</span></span>
<span data-ttu-id="fdb27-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb27-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdb27-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="fdb27-113">-EnablePowerBIService</span></span>
<span data-ttu-id="fdb27-114">Un contrassegno per indicare se il firewall consente l'accesso da Power BI</span><span class="sxs-lookup"><span data-stu-id="fdb27-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="fdb27-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="fdb27-115">-FirewallRule</span></span>
<span data-ttu-id="fdb27-116">Elenco di regole del firewall</span><span class="sxs-lookup"><span data-stu-id="fdb27-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="fdb27-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb27-117">CommonParameters</span></span>
<span data-ttu-id="fdb27-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb27-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb27-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb27-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb27-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="fdb27-120">INPUTS</span></span>

### <span data-ttu-id="fdb27-121">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="fdb27-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fdb27-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdb27-122">OUTPUTS</span></span>

### <span data-ttu-id="fdb27-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="fdb27-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="fdb27-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="fdb27-124">NOTES</span></span>

## <span data-ttu-id="fdb27-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdb27-125">RELATED LINKS</span></span>

[<span data-ttu-id="fdb27-126">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fdb27-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)