---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 88d89e819d97a42a797be81e5cb0b4b401401108
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355552"
---
# <span data-ttu-id="bbbab-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="bbbab-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="bbbab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbbab-102">SYNOPSIS</span></span>
<span data-ttu-id="bbbab-103">Rimuove una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="bbbab-103">Removes a managed application definition</span></span>

## <span data-ttu-id="bbbab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbbab-104">SYNTAX</span></span>

### <span data-ttu-id="bbbab-105">RemoveByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bbbab-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbbab-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="bbbab-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbbab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbbab-107">DESCRIPTION</span></span>
<span data-ttu-id="bbbab-108">Il cmdlet **Remove-AzManagedApplicationDefinition** rimuove una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="bbbab-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="bbbab-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbbab-109">EXAMPLES</span></span>

### <span data-ttu-id="bbbab-110">Esempio 1: rimuovere la definizione di applicazione gestita in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="bbbab-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="bbbab-111">Il primo comando ottiene una definizione di applicazione gestita denominata myAppDef tramite il cmdlet Get-AzManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="bbbab-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="bbbab-112">Il comando lo archivia nella variabile $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="bbbab-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="bbbab-113">Il secondo comando rimuove la definizione dell'applicazione gestita identificata dalla proprietà **resourceId** di $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="bbbab-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="bbbab-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbbab-114">PARAMETERS</span></span>

### <span data-ttu-id="bbbab-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bbbab-115">-ApiVersion</span></span>
<span data-ttu-id="bbbab-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="bbbab-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bbbab-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="bbbab-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="bbbab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbbab-118">-DefaultProfile</span></span>
<span data-ttu-id="bbbab-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbbab-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbbab-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bbbab-120">-Force</span></span>
<span data-ttu-id="bbbab-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="bbbab-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bbbab-122">-ID</span><span class="sxs-lookup"><span data-stu-id="bbbab-122">-Id</span></span>
<span data-ttu-id="bbbab-123">ID di definizione dell'applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bbbab-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="bbbab-124">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="bbbab-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="bbbab-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbbab-125">-Name</span></span>
<span data-ttu-id="bbbab-126">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="bbbab-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="bbbab-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="bbbab-127">-Pre</span></span>
<span data-ttu-id="bbbab-128">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="bbbab-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bbbab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbbab-129">-ResourceGroupName</span></span>
<span data-ttu-id="bbbab-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bbbab-130">The resource group name.</span></span>

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

### <span data-ttu-id="bbbab-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bbbab-131">-Confirm</span></span>
<span data-ttu-id="bbbab-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbbab-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbbab-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbbab-133">-WhatIf</span></span>
<span data-ttu-id="bbbab-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbbab-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbbab-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbbab-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbbab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbbab-136">CommonParameters</span></span>
<span data-ttu-id="bbbab-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbbab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbbab-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbbab-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbbab-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbbab-139">INPUTS</span></span>

### <span data-ttu-id="bbbab-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bbbab-140">System.String</span></span>

## <span data-ttu-id="bbbab-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbbab-141">OUTPUTS</span></span>

### <span data-ttu-id="bbbab-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bbbab-142">System.Boolean</span></span>

## <span data-ttu-id="bbbab-143">Note</span><span class="sxs-lookup"><span data-stu-id="bbbab-143">NOTES</span></span>

## <span data-ttu-id="bbbab-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbbab-144">RELATED LINKS</span></span>
