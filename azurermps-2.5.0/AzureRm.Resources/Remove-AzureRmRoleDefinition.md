---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 90b7b0b1d7909210d86ec1d5ac6b465f6e9fb239
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866628"
---
# <span data-ttu-id="9c02e-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9c02e-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="9c02e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c02e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c02e-103">Elimina un ruolo personalizzato in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="9c02e-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="9c02e-104">Il ruolo da eliminare viene specificato tramite la proprietà ID del ruolo.</span><span class="sxs-lookup"><span data-stu-id="9c02e-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="9c02e-105">L'eliminazione non riesce se sono presenti assegnazioni di ruolo esistenti al ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9c02e-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c02e-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c02e-106">SYNTAX</span></span>

### <span data-ttu-id="9c02e-107">RoleDefinitionIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c02e-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c02e-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c02e-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c02e-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c02e-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c02e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c02e-110">DESCRIPTION</span></span>
<span data-ttu-id="9c02e-111">Il cmdlet Remove-AzureRmRoleDefinition Elimina un ruolo personalizzato in Azure Role-Based controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="9c02e-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="9c02e-112">Fornisci il parametro ID di un ruolo personalizzato esistente per eliminare il ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9c02e-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="9c02e-113">Per impostazione predefinita, Remove-AzureRmRoleDefinition richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="9c02e-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="9c02e-114">Per eliminare il prompt, usa il parametro Force.</span><span class="sxs-lookup"><span data-stu-id="9c02e-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="9c02e-115">Se sono state apportate assegnazioni di ruolo per il ruolo personalizzato da eliminare, l'eliminazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9c02e-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="9c02e-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c02e-116">EXAMPLES</span></span>

### <span data-ttu-id="9c02e-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9c02e-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="9c02e-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9c02e-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="9c02e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c02e-119">PARAMETERS</span></span>

### <span data-ttu-id="9c02e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c02e-120">-DefaultProfile</span></span>
<span data-ttu-id="9c02e-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9c02e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c02e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9c02e-122">-Force</span></span>
<span data-ttu-id="9c02e-123">Se impostato, non richiede una conferma prima di eliminare il ruolo personalizzato</span><span class="sxs-lookup"><span data-stu-id="9c02e-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="9c02e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="9c02e-124">-Id</span></span>
<span data-ttu-id="9c02e-125">ID della definizione del ruolo da eliminare</span><span class="sxs-lookup"><span data-stu-id="9c02e-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="9c02e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c02e-126">-InputObject</span></span>
<span data-ttu-id="9c02e-127">Oggetto che rappresenta la definizione del ruolo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9c02e-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="9c02e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c02e-128">-Name</span></span>
<span data-ttu-id="9c02e-129">Nome della definizione del ruolo da eliminare.</span><span class="sxs-lookup"><span data-stu-id="9c02e-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="9c02e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c02e-130">-PassThru</span></span>
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

### <span data-ttu-id="9c02e-131">-Ambito</span><span class="sxs-lookup"><span data-stu-id="9c02e-131">-Scope</span></span>
<span data-ttu-id="9c02e-132">Ambito della definizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="9c02e-132">Role definition scope.</span></span>

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

### <span data-ttu-id="9c02e-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c02e-133">-Confirm</span></span>
<span data-ttu-id="9c02e-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c02e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c02e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c02e-135">-WhatIf</span></span>
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

### <span data-ttu-id="9c02e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c02e-136">CommonParameters</span></span>
<span data-ttu-id="9c02e-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c02e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c02e-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c02e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c02e-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c02e-139">INPUTS</span></span>

### <span data-ttu-id="9c02e-140">System. Guid</span><span class="sxs-lookup"><span data-stu-id="9c02e-140">System.Guid</span></span>

### <span data-ttu-id="9c02e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9c02e-141">System.String</span></span>

### <span data-ttu-id="9c02e-142">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9c02e-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="9c02e-143">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9c02e-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9c02e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c02e-144">OUTPUTS</span></span>

### <span data-ttu-id="9c02e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c02e-145">System.Boolean</span></span>

## <span data-ttu-id="9c02e-146">Note</span><span class="sxs-lookup"><span data-stu-id="9c02e-146">NOTES</span></span>
<span data-ttu-id="9c02e-147">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="9c02e-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9c02e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c02e-148">RELATED LINKS</span></span>

[<span data-ttu-id="9c02e-149">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9c02e-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="9c02e-150">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9c02e-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="9c02e-151">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9c02e-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

