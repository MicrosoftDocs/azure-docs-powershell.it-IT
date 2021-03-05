---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: d4ce9ef88f7043a369d8e566de75651944ea1e88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014894"
---
# <span data-ttu-id="85a7c-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="85a7c-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="85a7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="85a7c-103">Elimina un ruolo personalizzato nel controllo degli accessi in base al ruolo di Azure.</span><span class="sxs-lookup"><span data-stu-id="85a7c-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="85a7c-104">Il ruolo da eliminare viene specificato usando la proprietà ID del ruolo.</span><span class="sxs-lookup"><span data-stu-id="85a7c-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="85a7c-105">L'eliminazione non riesce se sono presenti assegnazioni di ruoli esistenti apportate al ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="85a7c-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="85a7c-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85a7c-106">SYNTAX</span></span>

### <span data-ttu-id="85a7c-107">RoleDefinitionIdParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85a7c-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a7c-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="85a7c-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a7c-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85a7c-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85a7c-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="85a7c-110">DESCRIPTION</span></span>
<span data-ttu-id="85a7c-111">Il cmdlet Remove-AzRoleDefinition elimina un ruolo personalizzato in Azure Role-Based controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="85a7c-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="85a7c-112">Specificare il parametro ID di un ruolo personalizzato esistente per eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="85a7c-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="85a7c-113">Per impostazione predefinita, Remove-AzRoleDefinition richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="85a7c-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="85a7c-114">Per eliminare la richiesta, usare il parametro Force.</span><span class="sxs-lookup"><span data-stu-id="85a7c-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="85a7c-115">Se ci sono assegnazioni di ruoli esistenti apportate al ruolo personalizzato da eliminare, l'eliminazione non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="85a7c-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="85a7c-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85a7c-116">EXAMPLES</span></span>

### <span data-ttu-id="85a7c-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85a7c-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="85a7c-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="85a7c-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="85a7c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85a7c-119">PARAMETERS</span></span>

### <span data-ttu-id="85a7c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a7c-120">-DefaultProfile</span></span>
<span data-ttu-id="85a7c-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="85a7c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85a7c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="85a7c-122">-Force</span></span>
<span data-ttu-id="85a7c-123">Se impostato, non richiede conferma prima di eliminare il ruolo personalizzato</span><span class="sxs-lookup"><span data-stu-id="85a7c-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="85a7c-124">-Id</span><span class="sxs-lookup"><span data-stu-id="85a7c-124">-Id</span></span>
<span data-ttu-id="85a7c-125">ID della definizione di ruolo da eliminare</span><span class="sxs-lookup"><span data-stu-id="85a7c-125">Id of the Role definition to be deleted</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a7c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85a7c-126">-InputObject</span></span>
<span data-ttu-id="85a7c-127">Oggetto che rappresenta la definizione di ruolo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="85a7c-127">The object representing the role definition to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85a7c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="85a7c-128">-Name</span></span>
<span data-ttu-id="85a7c-129">Nome della definizione di ruolo da eliminare.</span><span class="sxs-lookup"><span data-stu-id="85a7c-129">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a7c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85a7c-130">-PassThru</span></span>
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

### <span data-ttu-id="85a7c-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="85a7c-131">-Scope</span></span>
<span data-ttu-id="85a7c-132">Ambito della definizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="85a7c-132">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionIdParameterSet, RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a7c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85a7c-133">-Confirm</span></span>
<span data-ttu-id="85a7c-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85a7c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a7c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a7c-135">-WhatIf</span></span>
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

### <span data-ttu-id="85a7c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a7c-136">CommonParameters</span></span>
<span data-ttu-id="85a7c-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85a7c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a7c-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85a7c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a7c-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="85a7c-139">INPUTS</span></span>

### <span data-ttu-id="85a7c-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="85a7c-140">System.Guid</span></span>

### <span data-ttu-id="85a7c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="85a7c-141">System.String</span></span>

### <span data-ttu-id="85a7c-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="85a7c-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="85a7c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85a7c-143">OUTPUTS</span></span>

### <span data-ttu-id="85a7c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85a7c-144">System.Boolean</span></span>

## <span data-ttu-id="85a7c-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="85a7c-145">NOTES</span></span>
<span data-ttu-id="85a7c-146">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione</span><span class="sxs-lookup"><span data-stu-id="85a7c-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="85a7c-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85a7c-147">RELATED LINKS</span></span>

[<span data-ttu-id="85a7c-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="85a7c-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="85a7c-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="85a7c-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="85a7c-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="85a7c-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

