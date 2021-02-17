---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 88d89e819d97a42a797be81e5cb0b4b401401108
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186351"
---
# <span data-ttu-id="abc45-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="abc45-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="abc45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abc45-102">SYNOPSIS</span></span>
<span data-ttu-id="abc45-103">Rimuove una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="abc45-103">Removes a managed application definition</span></span>

## <span data-ttu-id="abc45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abc45-104">SYNTAX</span></span>

### <span data-ttu-id="abc45-105">RemoveByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="abc45-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abc45-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="abc45-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abc45-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="abc45-107">DESCRIPTION</span></span>
<span data-ttu-id="abc45-108">Il cmdlet **Remove-AzManagedApplicationDefinition rimuove** una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="abc45-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="abc45-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abc45-109">EXAMPLES</span></span>

### <span data-ttu-id="abc45-110">Esempio 1: Rimuovere la definizione dell'applicazione gestita in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="abc45-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="abc45-111">Il primo comando ottiene una definizione di applicazione gestita denominata myAppDef usando il cmdlet Get-AzManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="abc45-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="abc45-112">Il comando lo archivia nella $ApplicationDefinition variabile.</span><span class="sxs-lookup"><span data-stu-id="abc45-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="abc45-113">Il secondo comando rimuove la definizione di applicazione gestita identificata dalla **proprietà ResourceId** dell'$ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="abc45-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="abc45-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abc45-114">PARAMETERS</span></span>

### <span data-ttu-id="abc45-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="abc45-115">-ApiVersion</span></span>
<span data-ttu-id="abc45-116">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="abc45-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="abc45-117">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="abc45-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="abc45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc45-118">-DefaultProfile</span></span>
<span data-ttu-id="abc45-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="abc45-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abc45-120">-Force</span><span class="sxs-lookup"><span data-stu-id="abc45-120">-Force</span></span>
<span data-ttu-id="abc45-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="abc45-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="abc45-122">-Id</span><span class="sxs-lookup"><span data-stu-id="abc45-122">-Id</span></span>
<span data-ttu-id="abc45-123">ID di definizione dell'applicazione gestita completa, inclusa la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="abc45-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="abc45-124">ad esempio /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="abc45-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="abc45-125">-Name</span><span class="sxs-lookup"><span data-stu-id="abc45-125">-Name</span></span>
<span data-ttu-id="abc45-126">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="abc45-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="abc45-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="abc45-127">-Pre</span></span>
<span data-ttu-id="abc45-128">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="abc45-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="abc45-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc45-129">-ResourceGroupName</span></span>
<span data-ttu-id="abc45-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="abc45-130">The resource group name.</span></span>

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

### <span data-ttu-id="abc45-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abc45-131">-Confirm</span></span>
<span data-ttu-id="abc45-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abc45-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc45-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc45-133">-WhatIf</span></span>
<span data-ttu-id="abc45-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abc45-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc45-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abc45-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc45-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc45-136">CommonParameters</span></span>
<span data-ttu-id="abc45-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc45-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc45-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="abc45-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc45-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="abc45-139">INPUTS</span></span>

### <span data-ttu-id="abc45-140">System.String</span><span class="sxs-lookup"><span data-stu-id="abc45-140">System.String</span></span>

## <span data-ttu-id="abc45-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abc45-141">OUTPUTS</span></span>

### <span data-ttu-id="abc45-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="abc45-142">System.Boolean</span></span>

## <span data-ttu-id="abc45-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="abc45-143">NOTES</span></span>

## <span data-ttu-id="abc45-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abc45-144">RELATED LINKS</span></span>
