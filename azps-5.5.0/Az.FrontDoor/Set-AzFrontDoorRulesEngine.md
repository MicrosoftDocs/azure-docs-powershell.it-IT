---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: cf98121f535f60c7d1ddc3b29e33f10fd8f29842
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209458"
---
# <span data-ttu-id="b258f-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="b258f-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="b258f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b258f-102">SYNOPSIS</span></span>
<span data-ttu-id="b258f-103">Aggiornare un motore di regole.</span><span class="sxs-lookup"><span data-stu-id="b258f-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="b258f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b258f-104">SYNTAX</span></span>

### <span data-ttu-id="b258f-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b258f-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b258f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b258f-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b258f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b258f-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b258f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b258f-108">DESCRIPTION</span></span>
<span data-ttu-id="b258f-109">Aggiornare un motore di regole.</span><span class="sxs-lookup"><span data-stu-id="b258f-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="b258f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b258f-110">EXAMPLES</span></span>

### <span data-ttu-id="b258f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b258f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}

PS C:\> $rulesEngineRule2 = New-AzFrontDoorRulesEngineRuleObject -Name rules2 -Priority 3 -Action $rulesEngineAction
PS C:\AFD\azure-powershell\artifacts\Debug\Az.FrontDoor> Set-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1, $rulesEngineRule2

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1, rules2}
```

<span data-ttu-id="b258f-112">Ottenere una configurazione del motore di regole esistente e aggiungerne un'altra.</span><span class="sxs-lookup"><span data-stu-id="b258f-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="b258f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b258f-113">PARAMETERS</span></span>

### <span data-ttu-id="b258f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b258f-114">-DefaultProfile</span></span>
<span data-ttu-id="b258f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b258f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b258f-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="b258f-116">-FrontDoorName</span></span>
<span data-ttu-id="b258f-117">Nome della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="b258f-117">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b258f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b258f-118">-InputObject</span></span>
<span data-ttu-id="b258f-119">Oggetto Motore di regole da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="b258f-119">The Rules Engine object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b258f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b258f-120">-Name</span></span>
<span data-ttu-id="b258f-121">Nome del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="b258f-121">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b258f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b258f-122">-ResourceGroupName</span></span>
<span data-ttu-id="b258f-123">Nome del gruppo di risorse con cui verrà creata la porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="b258f-123">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b258f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b258f-124">-ResourceId</span></span>
<span data-ttu-id="b258f-125">ID risorsa di RulesStudio da aggiornare</span><span class="sxs-lookup"><span data-stu-id="b258f-125">Resource Id of the RulesEngine to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b258f-126">-Rule</span><span class="sxs-lookup"><span data-stu-id="b258f-126">-Rule</span></span>
<span data-ttu-id="b258f-127">Elenco di regole che definiscono una particolare configurazione del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="b258f-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="b258f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b258f-128">-Confirm</span></span>
<span data-ttu-id="b258f-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b258f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b258f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b258f-130">-WhatIf</span></span>
<span data-ttu-id="b258f-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b258f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b258f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b258f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b258f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b258f-133">CommonParameters</span></span>
<span data-ttu-id="b258f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b258f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b258f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b258f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b258f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="b258f-136">INPUTS</span></span>

### <span data-ttu-id="b258f-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesGrafo</span><span class="sxs-lookup"><span data-stu-id="b258f-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="b258f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b258f-138">System.String</span></span>

## <span data-ttu-id="b258f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b258f-139">OUTPUTS</span></span>

### <span data-ttu-id="b258f-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesGrafo</span><span class="sxs-lookup"><span data-stu-id="b258f-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="b258f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="b258f-141">NOTES</span></span>

## <span data-ttu-id="b258f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b258f-142">RELATED LINKS</span></span>
