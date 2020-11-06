---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 6669cdfad83c8e5f4299abe0d1297f7e0659a42c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520868"
---
# <span data-ttu-id="97cbd-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="97cbd-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="97cbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="97cbd-103">Elimina un ruolo personalizzato in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="97cbd-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="97cbd-104">Il ruolo da eliminare viene specificato tramite la proprietà ID del ruolo.</span><span class="sxs-lookup"><span data-stu-id="97cbd-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="97cbd-105">L'eliminazione non riesce se sono presenti assegnazioni di ruolo esistenti al ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="97cbd-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97cbd-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97cbd-106">SYNTAX</span></span>

### <span data-ttu-id="97cbd-107">RoleDefinitionIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97cbd-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97cbd-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="97cbd-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97cbd-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97cbd-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97cbd-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97cbd-110">DESCRIPTION</span></span>
<span data-ttu-id="97cbd-111">Il cmdlet Remove-AzureRmRoleDefinition Elimina un ruolo personalizzato in Azure Role-Based controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="97cbd-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="97cbd-112">Fornisci il parametro ID di un ruolo personalizzato esistente per eliminare il ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="97cbd-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="97cbd-113">Per impostazione predefinita, Remove-AzureRmRoleDefinition richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="97cbd-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="97cbd-114">Per eliminare il prompt, usa il parametro Force.</span><span class="sxs-lookup"><span data-stu-id="97cbd-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="97cbd-115">Se sono state apportate assegnazioni di ruolo per il ruolo personalizzato da eliminare, l'eliminazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="97cbd-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="97cbd-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97cbd-116">EXAMPLES</span></span>

### <span data-ttu-id="97cbd-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97cbd-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="97cbd-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="97cbd-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="97cbd-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97cbd-119">PARAMETERS</span></span>

### <span data-ttu-id="97cbd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97cbd-120">-DefaultProfile</span></span>
<span data-ttu-id="97cbd-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="97cbd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97cbd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="97cbd-122">-Force</span></span>
<span data-ttu-id="97cbd-123">Se impostato, non richiede una conferma prima di eliminare il ruolo personalizzato</span><span class="sxs-lookup"><span data-stu-id="97cbd-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="97cbd-124">-ID</span><span class="sxs-lookup"><span data-stu-id="97cbd-124">-Id</span></span>
<span data-ttu-id="97cbd-125">ID della definizione del ruolo da eliminare</span><span class="sxs-lookup"><span data-stu-id="97cbd-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="97cbd-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97cbd-126">-InputObject</span></span>
<span data-ttu-id="97cbd-127">Oggetto che rappresenta la definizione del ruolo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="97cbd-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="97cbd-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="97cbd-128">-Name</span></span>
<span data-ttu-id="97cbd-129">Nome della definizione del ruolo da eliminare.</span><span class="sxs-lookup"><span data-stu-id="97cbd-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="97cbd-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97cbd-130">-PassThru</span></span>
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

### <span data-ttu-id="97cbd-131">-Ambito</span><span class="sxs-lookup"><span data-stu-id="97cbd-131">-Scope</span></span>
<span data-ttu-id="97cbd-132">Ambito della definizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="97cbd-132">Role definition scope.</span></span>

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

### <span data-ttu-id="97cbd-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97cbd-133">-Confirm</span></span>
<span data-ttu-id="97cbd-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97cbd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97cbd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97cbd-135">-WhatIf</span></span>
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

### <span data-ttu-id="97cbd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97cbd-136">CommonParameters</span></span>
<span data-ttu-id="97cbd-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97cbd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97cbd-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97cbd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97cbd-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97cbd-139">INPUTS</span></span>

### <span data-ttu-id="97cbd-140">System. Guid</span><span class="sxs-lookup"><span data-stu-id="97cbd-140">System.Guid</span></span>

### <span data-ttu-id="97cbd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="97cbd-141">System.String</span></span>

### <span data-ttu-id="97cbd-142">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="97cbd-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="97cbd-143">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="97cbd-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="97cbd-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97cbd-144">OUTPUTS</span></span>

### <span data-ttu-id="97cbd-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97cbd-145">System.Boolean</span></span>

## <span data-ttu-id="97cbd-146">Note</span><span class="sxs-lookup"><span data-stu-id="97cbd-146">NOTES</span></span>
<span data-ttu-id="97cbd-147">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="97cbd-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="97cbd-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97cbd-148">RELATED LINKS</span></span>

[<span data-ttu-id="97cbd-149">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="97cbd-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="97cbd-150">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="97cbd-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="97cbd-151">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="97cbd-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

