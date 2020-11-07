---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: bde2d2edd48edf83efaf7f548daf4f97d6cffbaa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674369"
---
# <span data-ttu-id="1b1b9-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="1b1b9-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="1b1b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1b9-103">Creare un oggetto ManagedRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="1b1b9-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="1b1b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b1b9-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b1b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b1b9-105">DESCRIPTION</span></span>
<span data-ttu-id="1b1b9-106">Creare un oggetto ManagedRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="1b1b9-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="1b1b9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b1b9-107">EXAMPLES</span></span>

### <span data-ttu-id="1b1b9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1b1b9-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="1b1b9-109">Creare un oggetto ManagedRule</span><span class="sxs-lookup"><span data-stu-id="1b1b9-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="1b1b9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b1b9-110">PARAMETERS</span></span>

### <span data-ttu-id="1b1b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1b9-111">-DefaultProfile</span></span>
<span data-ttu-id="1b1b9-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b1b9-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="1b1b9-113">-RuleGroupOverride</span></span>
<span data-ttu-id="1b1b9-114">Elenco della configurazione di override di Azure Managed provider</span><span class="sxs-lookup"><span data-stu-id="1b1b9-114">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1b9-115">-Digitare</span><span class="sxs-lookup"><span data-stu-id="1b1b9-115">-Type</span></span>
<span data-ttu-id="1b1b9-116">Tipo di RuleSet</span><span class="sxs-lookup"><span data-stu-id="1b1b9-116">Type of the ruleset</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1b9-117">-Versione</span><span class="sxs-lookup"><span data-stu-id="1b1b9-117">-Version</span></span>
<span data-ttu-id="1b1b9-118">Versione del set di regole</span><span class="sxs-lookup"><span data-stu-id="1b1b9-118">Version of the ruleset</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1b9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1b9-119">CommonParameters</span></span>
<span data-ttu-id="1b1b9-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b1b9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1b9-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b1b9-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1b9-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b1b9-122">INPUTS</span></span>

### <span data-ttu-id="1b1b9-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b1b9-123">None</span></span>

## <span data-ttu-id="1b1b9-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b1b9-124">OUTPUTS</span></span>

### <span data-ttu-id="1b1b9-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="1b1b9-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="1b1b9-126">Note</span><span class="sxs-lookup"><span data-stu-id="1b1b9-126">NOTES</span></span>

## <span data-ttu-id="1b1b9-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b1b9-127">RELATED LINKS</span></span>

<span data-ttu-id="1b1b9-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="1b1b9-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
