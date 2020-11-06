---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: ae4f8e11ac213943d8cfcec162b43abde60fe753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520399"
---
# <span data-ttu-id="f268f-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f268f-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="f268f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f268f-102">SYNOPSIS</span></span>
<span data-ttu-id="f268f-103">Elimina un ruolo personalizzato in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="f268f-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="f268f-104">Il ruolo da eliminare viene specificato tramite la proprietà ID del ruolo.</span><span class="sxs-lookup"><span data-stu-id="f268f-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="f268f-105">L'eliminazione non riesce se sono presenti assegnazioni di ruolo esistenti al ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f268f-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f268f-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f268f-106">SYNTAX</span></span>

### <span data-ttu-id="f268f-107">RoleDefinitionIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f268f-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f268f-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f268f-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f268f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f268f-109">DESCRIPTION</span></span>
<span data-ttu-id="f268f-110">Il cmdlet Remove-AzureRmRoleDefinition Elimina un ruolo personalizzato in Azure Role-Based controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="f268f-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="f268f-111">Fornisci il parametro ID di un ruolo personalizzato esistente per eliminare il ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f268f-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="f268f-112">Per impostazione predefinita, Remove-AzureRmRoleDefinition richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="f268f-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="f268f-113">Per eliminare il prompt, usa il parametro Force.</span><span class="sxs-lookup"><span data-stu-id="f268f-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="f268f-114">Se sono state apportate assegnazioni di ruolo per il ruolo personalizzato da eliminare, l'eliminazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f268f-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="f268f-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f268f-115">EXAMPLES</span></span>

### <span data-ttu-id="f268f-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f268f-116">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="f268f-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f268f-117">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="f268f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f268f-118">PARAMETERS</span></span>

### <span data-ttu-id="f268f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f268f-119">-DefaultProfile</span></span>
<span data-ttu-id="f268f-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f268f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f268f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f268f-121">-Force</span></span>
<span data-ttu-id="f268f-122">Se impostato, non richiede una conferma prima di eliminare il ruolo personalizzato</span><span class="sxs-lookup"><span data-stu-id="f268f-122">If set, does not prompt for a confirmation before deleting the custom role</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f268f-123">-ID</span><span class="sxs-lookup"><span data-stu-id="f268f-123">-Id</span></span>
<span data-ttu-id="f268f-124">ID della definizione del ruolo da eliminare</span><span class="sxs-lookup"><span data-stu-id="f268f-124">Id of the Role definition to be deleted</span></span>

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f268f-125">-Name</span></span>
<span data-ttu-id="f268f-126">Nome della definizione del ruolo da eliminare.</span><span class="sxs-lookup"><span data-stu-id="f268f-126">Name of the Role definition to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f268f-127">-PassThru</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f268f-128">-Ambito</span><span class="sxs-lookup"><span data-stu-id="f268f-128">-Scope</span></span>
<span data-ttu-id="f268f-129">Ambito della definizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="f268f-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f268f-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f268f-130">-Confirm</span></span>
<span data-ttu-id="f268f-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f268f-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f268f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f268f-132">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f268f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f268f-133">CommonParameters</span></span>
<span data-ttu-id="f268f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f268f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f268f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f268f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f268f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f268f-136">INPUTS</span></span>

### <span data-ttu-id="f268f-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f268f-137">None</span></span>
<span data-ttu-id="f268f-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f268f-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f268f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f268f-139">OUTPUTS</span></span>

### <span data-ttu-id="f268f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f268f-140">System.Boolean</span></span>

## <span data-ttu-id="f268f-141">Note</span><span class="sxs-lookup"><span data-stu-id="f268f-141">NOTES</span></span>
<span data-ttu-id="f268f-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="f268f-142">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f268f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f268f-143">RELATED LINKS</span></span>

[<span data-ttu-id="f268f-144">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f268f-144">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="f268f-145">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f268f-145">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="f268f-146">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f268f-146">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

