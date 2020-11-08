---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193398"
---
# <span data-ttu-id="972ce-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="972ce-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="972ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="972ce-102">SYNOPSIS</span></span>
<span data-ttu-id="972ce-103">Rimuovi motore di regole da porta principale</span><span class="sxs-lookup"><span data-stu-id="972ce-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="972ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="972ce-104">SYNTAX</span></span>

### <span data-ttu-id="972ce-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="972ce-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972ce-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="972ce-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972ce-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="972ce-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="972ce-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="972ce-108">DESCRIPTION</span></span>
<span data-ttu-id="972ce-109">Rimuovi motore di regole da porta principale</span><span class="sxs-lookup"><span data-stu-id="972ce-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="972ce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="972ce-110">EXAMPLES</span></span>

### <span data-ttu-id="972ce-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="972ce-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="972ce-112">Rimuovi configurazione motore regole.</span><span class="sxs-lookup"><span data-stu-id="972ce-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="972ce-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="972ce-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="972ce-114">Risultato previsto durante la rimozione di una configurazione del motore di regole inesistente.</span><span class="sxs-lookup"><span data-stu-id="972ce-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="972ce-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="972ce-115">PARAMETERS</span></span>

### <span data-ttu-id="972ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="972ce-116">-DefaultProfile</span></span>
<span data-ttu-id="972ce-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="972ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="972ce-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="972ce-118">-FrontDoorName</span></span>
<span data-ttu-id="972ce-119">Nome porta principale.</span><span class="sxs-lookup"><span data-stu-id="972ce-119">Front Door name.</span></span>

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

### <span data-ttu-id="972ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="972ce-120">-InputObject</span></span>
<span data-ttu-id="972ce-121">Oggetto Engine Rules da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="972ce-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="972ce-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="972ce-122">-Name</span></span>
<span data-ttu-id="972ce-123">Nome motore regole.</span><span class="sxs-lookup"><span data-stu-id="972ce-123">Rules engine name.</span></span>

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

### <span data-ttu-id="972ce-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="972ce-124">-PassThru</span></span>
<span data-ttu-id="972ce-125">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="972ce-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="972ce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="972ce-126">-ResourceGroupName</span></span>
<span data-ttu-id="972ce-127">Nome del gruppo di risorse in cui verrà creata la porta principale.</span><span class="sxs-lookup"><span data-stu-id="972ce-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="972ce-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="972ce-128">-ResourceId</span></span>
<span data-ttu-id="972ce-129">ID risorsa di RulesEngine da aggiornare</span><span class="sxs-lookup"><span data-stu-id="972ce-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="972ce-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="972ce-130">-Confirm</span></span>
<span data-ttu-id="972ce-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="972ce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="972ce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="972ce-132">-WhatIf</span></span>
<span data-ttu-id="972ce-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="972ce-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="972ce-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="972ce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="972ce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="972ce-135">CommonParameters</span></span>
<span data-ttu-id="972ce-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="972ce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="972ce-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="972ce-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="972ce-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="972ce-138">INPUTS</span></span>

### <span data-ttu-id="972ce-139">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="972ce-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="972ce-140">System. String</span><span class="sxs-lookup"><span data-stu-id="972ce-140">System.String</span></span>

## <span data-ttu-id="972ce-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="972ce-141">OUTPUTS</span></span>

### <span data-ttu-id="972ce-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="972ce-142">System.Boolean</span></span>

## <span data-ttu-id="972ce-143">Note</span><span class="sxs-lookup"><span data-stu-id="972ce-143">NOTES</span></span>

## <span data-ttu-id="972ce-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="972ce-144">RELATED LINKS</span></span>
