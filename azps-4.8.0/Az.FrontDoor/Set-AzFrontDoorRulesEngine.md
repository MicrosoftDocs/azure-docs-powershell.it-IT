---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: cf98121f535f60c7d1ddc3b29e33f10fd8f29842
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192899"
---
# <span data-ttu-id="6dfee-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="6dfee-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="6dfee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6dfee-102">SYNOPSIS</span></span>
<span data-ttu-id="6dfee-103">Aggiornare un motore di regole.</span><span class="sxs-lookup"><span data-stu-id="6dfee-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="6dfee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dfee-104">SYNTAX</span></span>

### <span data-ttu-id="6dfee-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6dfee-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6dfee-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dfee-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dfee-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dfee-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dfee-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dfee-108">DESCRIPTION</span></span>
<span data-ttu-id="6dfee-109">Aggiornare un motore di regole.</span><span class="sxs-lookup"><span data-stu-id="6dfee-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="6dfee-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dfee-110">EXAMPLES</span></span>

### <span data-ttu-id="6dfee-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6dfee-111">Example 1</span></span>
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

<span data-ttu-id="6dfee-112">Ottenere una configurazione del motore di regole esistente e aggiungere un'altra regola del motore regole.</span><span class="sxs-lookup"><span data-stu-id="6dfee-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="6dfee-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6dfee-113">PARAMETERS</span></span>

### <span data-ttu-id="6dfee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dfee-114">-DefaultProfile</span></span>
<span data-ttu-id="6dfee-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dfee-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="6dfee-116">-FrontDoorName</span></span>
<span data-ttu-id="6dfee-117">Nome porta principale.</span><span class="sxs-lookup"><span data-stu-id="6dfee-117">Front Door name.</span></span>

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

### <span data-ttu-id="6dfee-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dfee-118">-InputObject</span></span>
<span data-ttu-id="6dfee-119">Oggetto Engine Rules da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="6dfee-119">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="6dfee-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6dfee-120">-Name</span></span>
<span data-ttu-id="6dfee-121">Nome motore regole.</span><span class="sxs-lookup"><span data-stu-id="6dfee-121">Rules engine name.</span></span>

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

### <span data-ttu-id="6dfee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dfee-122">-ResourceGroupName</span></span>
<span data-ttu-id="6dfee-123">Nome del gruppo di risorse in cui verrà creata la porta principale.</span><span class="sxs-lookup"><span data-stu-id="6dfee-123">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="6dfee-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dfee-124">-ResourceId</span></span>
<span data-ttu-id="6dfee-125">ID risorsa di RulesEngine da aggiornare</span><span class="sxs-lookup"><span data-stu-id="6dfee-125">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="6dfee-126">-Regola</span><span class="sxs-lookup"><span data-stu-id="6dfee-126">-Rule</span></span>
<span data-ttu-id="6dfee-127">Elenco di regole che definiscono una particolare configurazione del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="6dfee-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="6dfee-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6dfee-128">-Confirm</span></span>
<span data-ttu-id="6dfee-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dfee-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dfee-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dfee-130">-WhatIf</span></span>
<span data-ttu-id="6dfee-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dfee-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dfee-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dfee-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dfee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dfee-133">CommonParameters</span></span>
<span data-ttu-id="6dfee-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dfee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dfee-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dfee-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dfee-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6dfee-136">INPUTS</span></span>

### <span data-ttu-id="6dfee-137">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="6dfee-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="6dfee-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6dfee-138">System.String</span></span>

## <span data-ttu-id="6dfee-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dfee-139">OUTPUTS</span></span>

### <span data-ttu-id="6dfee-140">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="6dfee-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="6dfee-141">Note</span><span class="sxs-lookup"><span data-stu-id="6dfee-141">NOTES</span></span>

## <span data-ttu-id="6dfee-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dfee-142">RELATED LINKS</span></span>