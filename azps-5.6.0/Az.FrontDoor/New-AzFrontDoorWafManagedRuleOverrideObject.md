---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: ee4193fff69e8b46362ac75019cc76178001c2e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970846"
---
# <span data-ttu-id="f0bd8-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="f0bd8-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="f0bd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="f0bd8-103">Crea oggetto override regola gestita</span><span class="sxs-lookup"><span data-stu-id="f0bd8-103">Create managed rule override object</span></span>

## <span data-ttu-id="f0bd8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0bd8-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0bd8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0bd8-105">DESCRIPTION</span></span>
<span data-ttu-id="f0bd8-106">Creare l'oggetto PSAzureManagedRuleOverride per il gruppo di regole WAF gestito e ignorare la creazione di oggetti.</span><span class="sxs-lookup"><span data-stu-id="f0bd8-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="f0bd8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0bd8-107">EXAMPLES</span></span>

### <span data-ttu-id="f0bd8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f0bd8-108">Example 1</span></span>
<span data-ttu-id="f0bd8-109">Creare un oggetto override della regola gestita per la regola 942250 (nel gruppo SQLI).</span><span class="sxs-lookup"><span data-stu-id="f0bd8-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="f0bd8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0bd8-110">PARAMETERS</span></span>

### <span data-ttu-id="f0bd8-111">-Action</span><span class="sxs-lookup"><span data-stu-id="f0bd8-111">-Action</span></span>
<span data-ttu-id="f0bd8-112">Azione Ignora</span><span class="sxs-lookup"><span data-stu-id="f0bd8-112">Override Action</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bd8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0bd8-113">-DefaultProfile</span></span>
<span data-ttu-id="f0bd8-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0bd8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0bd8-115">-Disabled</span><span class="sxs-lookup"><span data-stu-id="f0bd8-115">-Disabled</span></span>
<span data-ttu-id="f0bd8-116">Stato disabilitato</span><span class="sxs-lookup"><span data-stu-id="f0bd8-116">Disabled state</span></span>

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

### <span data-ttu-id="f0bd8-117">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="f0bd8-117">-Exclusion</span></span>
<span data-ttu-id="f0bd8-118">Esclusione</span><span class="sxs-lookup"><span data-stu-id="f0bd8-118">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bd8-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="f0bd8-119">-RuleId</span></span>
<span data-ttu-id="f0bd8-120">ID regola</span><span class="sxs-lookup"><span data-stu-id="f0bd8-120">Rule ID</span></span>

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

### <span data-ttu-id="f0bd8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0bd8-121">CommonParameters</span></span>
<span data-ttu-id="f0bd8-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0bd8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0bd8-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f0bd8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0bd8-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0bd8-124">INPUTS</span></span>

### <span data-ttu-id="f0bd8-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f0bd8-125">None</span></span>

## <span data-ttu-id="f0bd8-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0bd8-126">OUTPUTS</span></span>

### <span data-ttu-id="f0bd8-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f0bd8-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="f0bd8-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0bd8-128">NOTES</span></span>

## <span data-ttu-id="f0bd8-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0bd8-129">RELATED LINKS</span></span>

[<span data-ttu-id="f0bd8-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="f0bd8-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)