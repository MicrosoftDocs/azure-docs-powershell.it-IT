---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: f7ed4b70b3b0575b41f081e088e55944b46656aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677281"
---
# <span data-ttu-id="93c3e-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="93c3e-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="93c3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="93c3e-103">Elimina un ruolo personalizzato in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="93c3e-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="93c3e-104">Il ruolo da eliminare viene specificato tramite la proprietà ID del ruolo.</span><span class="sxs-lookup"><span data-stu-id="93c3e-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="93c3e-105">L'eliminazione non riesce se sono presenti assegnazioni di ruolo esistenti al ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="93c3e-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="93c3e-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93c3e-106">SYNTAX</span></span>

### <span data-ttu-id="93c3e-107">RoleDefinitionIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93c3e-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93c3e-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="93c3e-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93c3e-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93c3e-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93c3e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93c3e-110">DESCRIPTION</span></span>
<span data-ttu-id="93c3e-111">Il cmdlet Remove-AzRoleDefinition Elimina un ruolo personalizzato in Azure Role-Based controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="93c3e-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="93c3e-112">Fornisci il parametro ID di un ruolo personalizzato esistente per eliminare il ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="93c3e-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="93c3e-113">Per impostazione predefinita, Remove-AzRoleDefinition richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="93c3e-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="93c3e-114">Per eliminare il prompt, usa il parametro Force.</span><span class="sxs-lookup"><span data-stu-id="93c3e-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="93c3e-115">Se sono state apportate assegnazioni di ruolo per il ruolo personalizzato da eliminare, l'eliminazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="93c3e-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="93c3e-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93c3e-116">EXAMPLES</span></span>

### <span data-ttu-id="93c3e-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="93c3e-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="93c3e-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="93c3e-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="93c3e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93c3e-119">PARAMETERS</span></span>

### <span data-ttu-id="93c3e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c3e-120">-DefaultProfile</span></span>
<span data-ttu-id="93c3e-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="93c3e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93c3e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="93c3e-122">-Force</span></span>
<span data-ttu-id="93c3e-123">Se impostato, non richiede una conferma prima di eliminare il ruolo personalizzato</span><span class="sxs-lookup"><span data-stu-id="93c3e-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="93c3e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="93c3e-124">-Id</span></span>
<span data-ttu-id="93c3e-125">ID della definizione del ruolo da eliminare</span><span class="sxs-lookup"><span data-stu-id="93c3e-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="93c3e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93c3e-126">-InputObject</span></span>
<span data-ttu-id="93c3e-127">Oggetto che rappresenta la definizione del ruolo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="93c3e-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="93c3e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="93c3e-128">-Name</span></span>
<span data-ttu-id="93c3e-129">Nome della definizione del ruolo da eliminare.</span><span class="sxs-lookup"><span data-stu-id="93c3e-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="93c3e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93c3e-130">-PassThru</span></span>
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

### <span data-ttu-id="93c3e-131">-Ambito</span><span class="sxs-lookup"><span data-stu-id="93c3e-131">-Scope</span></span>
<span data-ttu-id="93c3e-132">Ambito della definizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="93c3e-132">Role definition scope.</span></span>

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

### <span data-ttu-id="93c3e-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="93c3e-133">-Confirm</span></span>
<span data-ttu-id="93c3e-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93c3e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93c3e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93c3e-135">-WhatIf</span></span>
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

### <span data-ttu-id="93c3e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c3e-136">CommonParameters</span></span>
<span data-ttu-id="93c3e-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93c3e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c3e-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93c3e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c3e-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93c3e-139">INPUTS</span></span>

### <span data-ttu-id="93c3e-140">System. Guid</span><span class="sxs-lookup"><span data-stu-id="93c3e-140">System.Guid</span></span>

### <span data-ttu-id="93c3e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="93c3e-141">System.String</span></span>

### <span data-ttu-id="93c3e-142">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="93c3e-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="93c3e-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93c3e-143">OUTPUTS</span></span>

### <span data-ttu-id="93c3e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93c3e-144">System.Boolean</span></span>

## <span data-ttu-id="93c3e-145">Note</span><span class="sxs-lookup"><span data-stu-id="93c3e-145">NOTES</span></span>
<span data-ttu-id="93c3e-146">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="93c3e-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="93c3e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93c3e-147">RELATED LINKS</span></span>

[<span data-ttu-id="93c3e-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="93c3e-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="93c3e-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="93c3e-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="93c3e-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="93c3e-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

