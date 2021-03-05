---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 05248a299b907c74f43edddb7caf18697794dc08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970974"
---
# <span data-ttu-id="8325b-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8325b-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="8325b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8325b-102">SYNOPSIS</span></span>
<span data-ttu-id="8325b-103">Creare una nuova configurazione del motore di regole per una porta anteriore specifica.</span><span class="sxs-lookup"><span data-stu-id="8325b-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="8325b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8325b-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8325b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8325b-105">DESCRIPTION</span></span>
<span data-ttu-id="8325b-106">Creare una nuova configurazione del motore di regole per una porta anteriore specifica.</span><span class="sxs-lookup"><span data-stu-id="8325b-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="8325b-107">Usare il cmdlet "New-AzFrontDoorRulesRulesRule" per creare regole del motore di regole da passare al parametro "-Rules" di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8325b-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="8325b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8325b-108">EXAMPLES</span></span>

### <span data-ttu-id="8325b-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8325b-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="8325b-110">Crea una nuova configurazione del motore di regole per il porta anteriore specificata.</span><span class="sxs-lookup"><span data-stu-id="8325b-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="8325b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8325b-111">PARAMETERS</span></span>

### <span data-ttu-id="8325b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8325b-112">-DefaultProfile</span></span>
<span data-ttu-id="8325b-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8325b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8325b-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8325b-114">-FrontDoorName</span></span>
<span data-ttu-id="8325b-115">Nome della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="8325b-115">Front Door name.</span></span>

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

### <span data-ttu-id="8325b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8325b-116">-Name</span></span>
<span data-ttu-id="8325b-117">Nome del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="8325b-117">Rules engine name.</span></span>

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

### <span data-ttu-id="8325b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8325b-118">-ResourceGroupName</span></span>
<span data-ttu-id="8325b-119">Nome del gruppo di risorse con cui verrà creata la porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="8325b-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="8325b-120">-Rule</span><span class="sxs-lookup"><span data-stu-id="8325b-120">-Rule</span></span>
<span data-ttu-id="8325b-121">Elenco di regole che definiscono una particolare configurazione del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="8325b-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8325b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8325b-122">-Confirm</span></span>
<span data-ttu-id="8325b-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8325b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8325b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8325b-124">-WhatIf</span></span>
<span data-ttu-id="8325b-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8325b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8325b-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8325b-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8325b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8325b-127">CommonParameters</span></span>
<span data-ttu-id="8325b-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8325b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8325b-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8325b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8325b-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="8325b-130">INPUTS</span></span>

### <span data-ttu-id="8325b-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8325b-131">None</span></span>

## <span data-ttu-id="8325b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8325b-132">OUTPUTS</span></span>

### <span data-ttu-id="8325b-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesGrafo</span><span class="sxs-lookup"><span data-stu-id="8325b-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="8325b-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="8325b-134">NOTES</span></span>

## <span data-ttu-id="8325b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8325b-135">RELATED LINKS</span></span>
