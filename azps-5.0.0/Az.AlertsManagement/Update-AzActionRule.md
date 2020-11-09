---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296604"
---
# <span data-ttu-id="974e5-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="974e5-101">Update-AzActionRule</span></span>

## <span data-ttu-id="974e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="974e5-102">SYNOPSIS</span></span>
<span data-ttu-id="974e5-103">Aggiorna le proprietà delle regole di azione.</span><span class="sxs-lookup"><span data-stu-id="974e5-103">Updates action rule properties.</span></span>

## <span data-ttu-id="974e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="974e5-104">SYNTAX</span></span>

### <span data-ttu-id="974e5-105">ByNameSimplifiedPatch (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="974e5-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="974e5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="974e5-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="974e5-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="974e5-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="974e5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="974e5-108">DESCRIPTION</span></span>
<span data-ttu-id="974e5-109">**Update-cmdlet AzActionRule** aggiorna le proprietà delle regole di azione-stato e contrassegni.</span><span class="sxs-lookup"><span data-stu-id="974e5-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="974e5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="974e5-110">EXAMPLES</span></span>

### <span data-ttu-id="974e5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="974e5-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="974e5-112">Questo cmdlet disabilita la regola di azione.</span><span class="sxs-lookup"><span data-stu-id="974e5-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="974e5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="974e5-113">PARAMETERS</span></span>

### <span data-ttu-id="974e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="974e5-114">-DefaultProfile</span></span>
<span data-ttu-id="974e5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="974e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="974e5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="974e5-116">-InputObject</span></span>
<span data-ttu-id="974e5-117">Risorsa della regola di azione</span><span class="sxs-lookup"><span data-stu-id="974e5-117">The action rule resource</span></span>

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

### <span data-ttu-id="974e5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="974e5-118">-Name</span></span>
<span data-ttu-id="974e5-119">Nome della regola di azione</span><span class="sxs-lookup"><span data-stu-id="974e5-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="974e5-120">-ResourceGroupName</span></span>
<span data-ttu-id="974e5-121">Nome della regola di azione</span><span class="sxs-lookup"><span data-stu-id="974e5-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="974e5-122">-ResourceId</span></span>
<span data-ttu-id="974e5-123">ID risorsa della regola di azione</span><span class="sxs-lookup"><span data-stu-id="974e5-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-124">-Stato</span><span class="sxs-lookup"><span data-stu-id="974e5-124">-Status</span></span>
<span data-ttu-id="974e5-125">Stato della regola di azione</span><span class="sxs-lookup"><span data-stu-id="974e5-125">Action rule status</span></span>

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

### <span data-ttu-id="974e5-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="974e5-126">-Tag</span></span>
<span data-ttu-id="974e5-127">Tag delle regole di azione</span><span class="sxs-lookup"><span data-stu-id="974e5-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="974e5-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="974e5-128">-Confirm</span></span>
<span data-ttu-id="974e5-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="974e5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="974e5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="974e5-130">-WhatIf</span></span>
<span data-ttu-id="974e5-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="974e5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="974e5-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="974e5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="974e5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="974e5-133">CommonParameters</span></span>
<span data-ttu-id="974e5-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="974e5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="974e5-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="974e5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="974e5-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="974e5-136">INPUTS</span></span>

### <span data-ttu-id="974e5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="974e5-137">System.String</span></span>

### <span data-ttu-id="974e5-138">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="974e5-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="974e5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="974e5-139">OUTPUTS</span></span>

### <span data-ttu-id="974e5-140">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="974e5-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="974e5-141">Note</span><span class="sxs-lookup"><span data-stu-id="974e5-141">NOTES</span></span>

## <span data-ttu-id="974e5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="974e5-142">RELATED LINKS</span></span>
