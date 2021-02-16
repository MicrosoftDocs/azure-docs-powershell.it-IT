---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185926"
---
# <span data-ttu-id="558fa-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="558fa-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="558fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="558fa-102">SYNOPSIS</span></span>
<span data-ttu-id="558fa-103">Rimuovere il motore di regole dalla porta anteriore</span><span class="sxs-lookup"><span data-stu-id="558fa-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="558fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="558fa-104">SYNTAX</span></span>

### <span data-ttu-id="558fa-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="558fa-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="558fa-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="558fa-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="558fa-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="558fa-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="558fa-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="558fa-108">DESCRIPTION</span></span>
<span data-ttu-id="558fa-109">Rimuovere il motore di regole dalla porta anteriore</span><span class="sxs-lookup"><span data-stu-id="558fa-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="558fa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="558fa-110">EXAMPLES</span></span>

### <span data-ttu-id="558fa-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="558fa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="558fa-112">Rimuovere la configurazione del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="558fa-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="558fa-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="558fa-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="558fa-114">Risultato previsto quando si rimuove una configurazione del motore di regole inesistente.</span><span class="sxs-lookup"><span data-stu-id="558fa-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="558fa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="558fa-115">PARAMETERS</span></span>

### <span data-ttu-id="558fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="558fa-116">-DefaultProfile</span></span>
<span data-ttu-id="558fa-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="558fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="558fa-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="558fa-118">-FrontDoorName</span></span>
<span data-ttu-id="558fa-119">Nome della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="558fa-119">Front Door name.</span></span>

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

### <span data-ttu-id="558fa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="558fa-120">-InputObject</span></span>
<span data-ttu-id="558fa-121">Oggetto Motore di regole da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="558fa-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="558fa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="558fa-122">-Name</span></span>
<span data-ttu-id="558fa-123">Nome del motore di regole.</span><span class="sxs-lookup"><span data-stu-id="558fa-123">Rules engine name.</span></span>

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

### <span data-ttu-id="558fa-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="558fa-124">-PassThru</span></span>
<span data-ttu-id="558fa-125">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="558fa-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="558fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="558fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="558fa-127">Nome del gruppo di risorse con cui verrà creata la porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="558fa-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="558fa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="558fa-128">-ResourceId</span></span>
<span data-ttu-id="558fa-129">ID risorsa di RulesStudio da aggiornare</span><span class="sxs-lookup"><span data-stu-id="558fa-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="558fa-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="558fa-130">-Confirm</span></span>
<span data-ttu-id="558fa-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="558fa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="558fa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="558fa-132">-WhatIf</span></span>
<span data-ttu-id="558fa-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="558fa-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="558fa-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="558fa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="558fa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="558fa-135">CommonParameters</span></span>
<span data-ttu-id="558fa-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="558fa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="558fa-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="558fa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="558fa-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="558fa-138">INPUTS</span></span>

### <span data-ttu-id="558fa-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesGrafo</span><span class="sxs-lookup"><span data-stu-id="558fa-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="558fa-140">System.String</span><span class="sxs-lookup"><span data-stu-id="558fa-140">System.String</span></span>

## <span data-ttu-id="558fa-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="558fa-141">OUTPUTS</span></span>

### <span data-ttu-id="558fa-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="558fa-142">System.Boolean</span></span>

## <span data-ttu-id="558fa-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="558fa-143">NOTES</span></span>

## <span data-ttu-id="558fa-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="558fa-144">RELATED LINKS</span></span>
