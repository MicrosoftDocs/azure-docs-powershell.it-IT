---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 41f59b46595d45932010b1fcbedae07cdeca5f78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971774"
---
# <span data-ttu-id="7fcbd-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="7fcbd-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="7fcbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fcbd-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcbd-103">Rimuove un'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="7fcbd-103">Removes a managed application</span></span>

## <span data-ttu-id="7fcbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fcbd-104">SYNTAX</span></span>

### <span data-ttu-id="7fcbd-105">RemoveByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7fcbd-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fcbd-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="7fcbd-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fcbd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7fcbd-107">DESCRIPTION</span></span>
<span data-ttu-id="7fcbd-108">Il cmdlet **Remove-AzManagedApplication** rimuove un'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="7fcbd-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="7fcbd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fcbd-109">EXAMPLES</span></span>

### <span data-ttu-id="7fcbd-110">Esempio 1: Rimuovere l'applicazione gestita in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="7fcbd-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="7fcbd-111">Il primo comando ottiene un'applicazione gestita denominata myApp usando il cmdlet Get-AzManagedApplication gestione applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="7fcbd-112">Il comando lo archivia nella $Application variabile.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="7fcbd-113">Il secondo comando rimuove l'applicazione gestita identificata dalla **proprietà ResourceId** dell'$Application.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="7fcbd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fcbd-114">PARAMETERS</span></span>

### <span data-ttu-id="7fcbd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7fcbd-115">-ApiVersion</span></span>
<span data-ttu-id="7fcbd-116">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7fcbd-117">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="7fcbd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fcbd-118">-DefaultProfile</span></span>
<span data-ttu-id="7fcbd-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fcbd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7fcbd-120">-Force</span></span>
<span data-ttu-id="7fcbd-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7fcbd-122">-Id</span><span class="sxs-lookup"><span data-stu-id="7fcbd-122">-Id</span></span>
<span data-ttu-id="7fcbd-123">ID applicazione gestita completo, inclusa la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="7fcbd-124">ad esempio /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="7fcbd-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcbd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7fcbd-125">-Name</span></span>
<span data-ttu-id="7fcbd-126">Nome dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcbd-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="7fcbd-127">-Pre</span></span>
<span data-ttu-id="7fcbd-128">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7fcbd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fcbd-129">-ResourceGroupName</span></span>
<span data-ttu-id="7fcbd-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcbd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fcbd-131">-Confirm</span></span>
<span data-ttu-id="7fcbd-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fcbd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fcbd-133">-WhatIf</span></span>
<span data-ttu-id="7fcbd-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fcbd-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fcbd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcbd-136">CommonParameters</span></span>
<span data-ttu-id="7fcbd-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcbd-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7fcbd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcbd-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="7fcbd-139">INPUTS</span></span>

### <span data-ttu-id="7fcbd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7fcbd-140">System.String</span></span>

## <span data-ttu-id="7fcbd-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fcbd-141">OUTPUTS</span></span>

### <span data-ttu-id="7fcbd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7fcbd-142">System.Boolean</span></span>

## <span data-ttu-id="7fcbd-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="7fcbd-143">NOTES</span></span>

## <span data-ttu-id="7fcbd-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fcbd-144">RELATED LINKS</span></span>
