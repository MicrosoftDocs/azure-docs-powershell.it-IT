---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleOverrideObject.md
ms.openlocfilehash: e45abaae34f3b8449920dad122736c46b9d946ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836139"
---
# <span data-ttu-id="86075-101">New-AzFrontDoorManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="86075-101">New-AzFrontDoorManagedRuleOverrideObject</span></span>

## <span data-ttu-id="86075-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86075-102">SYNOPSIS</span></span>
<span data-ttu-id="86075-103">Creare un oggetto di override della regola gestita</span><span class="sxs-lookup"><span data-stu-id="86075-103">Create managed rule override object</span></span>

## <span data-ttu-id="86075-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86075-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleOverrideObject -RuleId <String> [-Action <PSAction>] [-Disabled]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86075-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86075-105">DESCRIPTION</span></span>
<span data-ttu-id="86075-106">Creare un oggetto PSAzureManagedRuleOverride per il gruppo di regole WAF gestito ignora la creazione di oggetti.</span><span class="sxs-lookup"><span data-stu-id="86075-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="86075-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86075-107">EXAMPLES</span></span>

### <span data-ttu-id="86075-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86075-108">Example 1</span></span>
<span data-ttu-id="86075-109">Creare un oggetto di override della regola gestita per la regola 942250 (che si trova nel gruppo SQLI).</span><span class="sxs-lookup"><span data-stu-id="86075-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="86075-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86075-110">PARAMETERS</span></span>

### <span data-ttu-id="86075-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="86075-111">-Action</span></span>
<span data-ttu-id="86075-112">Azione di override</span><span class="sxs-lookup"><span data-stu-id="86075-112">Override Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86075-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86075-113">-DefaultProfile</span></span>
<span data-ttu-id="86075-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86075-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86075-115">-Disabled</span><span class="sxs-lookup"><span data-stu-id="86075-115">-Disabled</span></span>
<span data-ttu-id="86075-116">Stato disabilitato</span><span class="sxs-lookup"><span data-stu-id="86075-116">Disabled state</span></span>

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

### <span data-ttu-id="86075-117">-RuleId</span><span class="sxs-lookup"><span data-stu-id="86075-117">-RuleId</span></span>
<span data-ttu-id="86075-118">ID regola</span><span class="sxs-lookup"><span data-stu-id="86075-118">Rule ID</span></span>

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

### <span data-ttu-id="86075-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86075-119">CommonParameters</span></span>
<span data-ttu-id="86075-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86075-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86075-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86075-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86075-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86075-122">INPUTS</span></span>

### <span data-ttu-id="86075-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="86075-123">None</span></span>

## <span data-ttu-id="86075-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86075-124">OUTPUTS</span></span>

### <span data-ttu-id="86075-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="86075-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="86075-126">Note</span><span class="sxs-lookup"><span data-stu-id="86075-126">NOTES</span></span>

## <span data-ttu-id="86075-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86075-127">RELATED LINKS</span></span>

[<span data-ttu-id="86075-128">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="86075-128">New-AzFrontDoorRuleGroupOverrideObject</span></span>](./New-AzFrontDoorRuleGroupOverrideObject.md)