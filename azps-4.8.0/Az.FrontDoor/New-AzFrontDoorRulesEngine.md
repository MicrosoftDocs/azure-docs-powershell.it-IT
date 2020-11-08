---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031223"
---
# <span data-ttu-id="19e41-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="19e41-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="19e41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19e41-102">SYNOPSIS</span></span>
<span data-ttu-id="19e41-103">Creare una nuova configurazione del motore regole per uno sportello anteriore specificato.</span><span class="sxs-lookup"><span data-stu-id="19e41-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="19e41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19e41-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19e41-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19e41-105">DESCRIPTION</span></span>
<span data-ttu-id="19e41-106">Creare una nuova configurazione del motore regole per uno sportello anteriore specificato.</span><span class="sxs-lookup"><span data-stu-id="19e41-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="19e41-107">Usa il cmdlet "New-AzFrontDoorRulesEngineRule" per creare regole del motore di regole per passare al parametro "-Rules" di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19e41-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="19e41-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19e41-108">EXAMPLES</span></span>

### <span data-ttu-id="19e41-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="19e41-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="19e41-110">Creare una nuova configurazione del motore regole per la porta anteriore specificata.</span><span class="sxs-lookup"><span data-stu-id="19e41-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="19e41-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19e41-111">PARAMETERS</span></span>

### <span data-ttu-id="19e41-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e41-112">-DefaultProfile</span></span>
<span data-ttu-id="19e41-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19e41-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19e41-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="19e41-114">-FrontDoorName</span></span>
<span data-ttu-id="19e41-115">Nome porta principale.</span><span class="sxs-lookup"><span data-stu-id="19e41-115">Front Door name.</span></span>

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

### <span data-ttu-id="19e41-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="19e41-116">-Name</span></span>
<span data-ttu-id="19e41-117">Nome motore regole.</span><span class="sxs-lookup"><span data-stu-id="19e41-117">Rules engine name.</span></span>

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

### <span data-ttu-id="19e41-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19e41-118">-ResourceGroupName</span></span>
<span data-ttu-id="19e41-119">Nome del gruppo di risorse in cui verrà creata la porta principale.</span><span class="sxs-lookup"><span data-stu-id="19e41-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="19e41-120">-Regola</span><span class="sxs-lookup"><span data-stu-id="19e41-120">-Rule</span></span>
<span data-ttu-id="19e41-121">Elenco di regole che definiscono una particolare configurazione del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="19e41-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="19e41-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19e41-122">-Confirm</span></span>
<span data-ttu-id="19e41-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19e41-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19e41-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19e41-124">-WhatIf</span></span>
<span data-ttu-id="19e41-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19e41-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19e41-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19e41-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19e41-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e41-127">CommonParameters</span></span>
<span data-ttu-id="19e41-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19e41-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e41-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19e41-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e41-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19e41-130">INPUTS</span></span>

### <span data-ttu-id="19e41-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="19e41-131">None</span></span>

## <span data-ttu-id="19e41-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19e41-132">OUTPUTS</span></span>

### <span data-ttu-id="19e41-133">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="19e41-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="19e41-134">Note</span><span class="sxs-lookup"><span data-stu-id="19e41-134">NOTES</span></span>

## <span data-ttu-id="19e41-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19e41-135">RELATED LINKS</span></span>
