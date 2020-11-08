---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202518"
---
# <span data-ttu-id="ff806-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="ff806-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="ff806-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff806-102">SYNOPSIS</span></span>
<span data-ttu-id="ff806-103">Ottenere le definizioni di set di regole gestite WAF</span><span class="sxs-lookup"><span data-stu-id="ff806-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="ff806-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff806-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff806-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff806-105">DESCRIPTION</span></span>
<span data-ttu-id="ff806-106">Ottiene l'elenco delle definizioni di set di regole gestite WAF da usare come riferimento</span><span class="sxs-lookup"><span data-stu-id="ff806-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="ff806-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff806-107">EXAMPLES</span></span>

### <span data-ttu-id="ff806-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ff806-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="ff806-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="ff806-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ff806-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff806-110">PARAMETERS</span></span>

### <span data-ttu-id="ff806-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff806-111">-DefaultProfile</span></span>
<span data-ttu-id="ff806-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff806-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff806-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff806-113">CommonParameters</span></span>
<span data-ttu-id="ff806-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff806-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff806-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff806-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff806-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff806-116">INPUTS</span></span>

### <span data-ttu-id="ff806-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ff806-117">None</span></span>

## <span data-ttu-id="ff806-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff806-118">OUTPUTS</span></span>

### <span data-ttu-id="ff806-119">Microsoft. Azure. Commands. FrontDoor. Models. PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="ff806-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="ff806-120">Note</span><span class="sxs-lookup"><span data-stu-id="ff806-120">NOTES</span></span>

## <span data-ttu-id="ff806-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff806-121">RELATED LINKS</span></span>

<span data-ttu-id="ff806-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="ff806-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
