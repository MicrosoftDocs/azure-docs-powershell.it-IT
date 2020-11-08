---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 1cdea9a2d5deb9fbe93da0a090070f7ed1b07653
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019155"
---
# <span data-ttu-id="8dbc8-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="8dbc8-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="8dbc8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8dbc8-102">SYNOPSIS</span></span>
<span data-ttu-id="8dbc8-103">Elimina una regola di azione</span><span class="sxs-lookup"><span data-stu-id="8dbc8-103">Deletes a action rule</span></span>

## <span data-ttu-id="8dbc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dbc8-104">SYNTAX</span></span>

### <span data-ttu-id="8dbc8-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8dbc8-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbc8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8dbc8-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbc8-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8dbc8-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dbc8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dbc8-108">DESCRIPTION</span></span>
<span data-ttu-id="8dbc8-109">Cmdlet **Remove-AzActionRule** Elimina una regola di azione.</span><span class="sxs-lookup"><span data-stu-id="8dbc8-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="8dbc8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dbc8-110">EXAMPLES</span></span>

### <span data-ttu-id="8dbc8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8dbc8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="8dbc8-112">Questo cmdlet elimina la regola di azione con il nome ActionRuleName nel gruppo di risorse test-RG</span><span class="sxs-lookup"><span data-stu-id="8dbc8-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="8dbc8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8dbc8-113">PARAMETERS</span></span>

### <span data-ttu-id="8dbc8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dbc8-114">-DefaultProfile</span></span>
<span data-ttu-id="8dbc8-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbc8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dbc8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dbc8-116">-InputObject</span></span>
<span data-ttu-id="8dbc8-117">Risorsa della regola di azione</span><span class="sxs-lookup"><span data-stu-id="8dbc8-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dbc8-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8dbc8-118">-Name</span></span>
<span data-ttu-id="8dbc8-119">Nome della regola di azione</span><span class="sxs-lookup"><span data-stu-id="8dbc8-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dbc8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dbc8-120">-PassThru</span></span>
<span data-ttu-id="8dbc8-121">PassThru restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="8dbc8-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8dbc8-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8dbc8-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8dbc8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dbc8-123">-ResourceGroupName</span></span>
<span data-ttu-id="8dbc8-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8dbc8-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dbc8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dbc8-125">-ResourceId</span></span>
<span data-ttu-id="8dbc8-126">Ottenere la regola dell'azione tramite ID Resoure.</span><span class="sxs-lookup"><span data-stu-id="8dbc8-126">Get Action rule by resoure id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dbc8-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8dbc8-127">-Confirm</span></span>
<span data-ttu-id="8dbc8-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dbc8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dbc8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dbc8-129">-WhatIf</span></span>
<span data-ttu-id="8dbc8-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dbc8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dbc8-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dbc8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dbc8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dbc8-132">CommonParameters</span></span>
<span data-ttu-id="8dbc8-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dbc8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dbc8-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dbc8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dbc8-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8dbc8-135">INPUTS</span></span>

### <span data-ttu-id="8dbc8-136">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="8dbc8-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="8dbc8-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dbc8-137">OUTPUTS</span></span>

### <span data-ttu-id="8dbc8-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8dbc8-138">System.Boolean</span></span>

## <span data-ttu-id="8dbc8-139">Note</span><span class="sxs-lookup"><span data-stu-id="8dbc8-139">NOTES</span></span>

## <span data-ttu-id="8dbc8-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dbc8-140">RELATED LINKS</span></span>
