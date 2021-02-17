---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192494"
---
# <span data-ttu-id="b5414-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="b5414-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="b5414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5414-102">SYNOPSIS</span></span>
<span data-ttu-id="b5414-103">Creare una nuova configurazione del motore di regole per una porta anteriore specifica.</span><span class="sxs-lookup"><span data-stu-id="b5414-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="b5414-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5414-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5414-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5414-105">DESCRIPTION</span></span>
<span data-ttu-id="b5414-106">Creare una nuova configurazione del motore di regole per una porta anteriore specifica.</span><span class="sxs-lookup"><span data-stu-id="b5414-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="b5414-107">Usare il cmdlet "New-AzFrontDoorRulesRulesRule" per creare regole del motore di regole da passare al parametro "-Rules" di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5414-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="b5414-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5414-108">EXAMPLES</span></span>

### <span data-ttu-id="b5414-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5414-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="b5414-110">Creare una nuova configurazione del motore di regole per una porta specifica.</span><span class="sxs-lookup"><span data-stu-id="b5414-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="b5414-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5414-111">PARAMETERS</span></span>

### <span data-ttu-id="b5414-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5414-112">-DefaultProfile</span></span>
<span data-ttu-id="b5414-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5414-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5414-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="b5414-114">-FrontDoorName</span></span>
<span data-ttu-id="b5414-115">Nome della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="b5414-115">Front Door name.</span></span>

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

### <span data-ttu-id="b5414-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b5414-116">-Name</span></span>
<span data-ttu-id="b5414-117">Nome del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="b5414-117">Rules engine name.</span></span>

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

### <span data-ttu-id="b5414-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5414-118">-ResourceGroupName</span></span>
<span data-ttu-id="b5414-119">Nome del gruppo di risorse con cui verrà creata la porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="b5414-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="b5414-120">-Rule</span><span class="sxs-lookup"><span data-stu-id="b5414-120">-Rule</span></span>
<span data-ttu-id="b5414-121">Elenco di regole che definiscono una particolare configurazione del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="b5414-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="b5414-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5414-122">-Confirm</span></span>
<span data-ttu-id="b5414-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5414-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5414-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5414-124">-WhatIf</span></span>
<span data-ttu-id="b5414-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5414-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5414-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5414-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5414-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5414-127">CommonParameters</span></span>
<span data-ttu-id="b5414-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5414-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5414-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5414-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5414-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5414-130">INPUTS</span></span>

### <span data-ttu-id="b5414-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b5414-131">None</span></span>

## <span data-ttu-id="b5414-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5414-132">OUTPUTS</span></span>

### <span data-ttu-id="b5414-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesGrafo</span><span class="sxs-lookup"><span data-stu-id="b5414-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="b5414-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5414-134">NOTES</span></span>

## <span data-ttu-id="b5414-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5414-135">RELATED LINKS</span></span>
