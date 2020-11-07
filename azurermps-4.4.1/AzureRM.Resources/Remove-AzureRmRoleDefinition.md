---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 476555b271d58f8e594f0cae1422bcdde1fc46e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686783"
---
# <span data-ttu-id="48b85-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="48b85-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="48b85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48b85-102">SYNOPSIS</span></span>
<span data-ttu-id="48b85-103">Elimina un ruolo personalizzato in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="48b85-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="48b85-104">Il ruolo da eliminare viene specificato tramite la proprietà ID del ruolo.</span><span class="sxs-lookup"><span data-stu-id="48b85-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="48b85-105">L'eliminazione non riesce se sono presenti assegnazioni di ruolo esistenti al ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="48b85-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48b85-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48b85-106">SYNTAX</span></span>

### <span data-ttu-id="48b85-107">RoleDefinitionIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48b85-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48b85-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="48b85-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48b85-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48b85-109">DESCRIPTION</span></span>
<span data-ttu-id="48b85-110">Il cmdlet Remove-AzureRmRoleDefinition Elimina un ruolo personalizzato in Azure Role-Based controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="48b85-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="48b85-111">Fornisci il parametro ID di un ruolo personalizzato esistente per eliminare il ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="48b85-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="48b85-112">Per impostazione predefinita, Remove-AzureRmRoleDefinition richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="48b85-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="48b85-113">Per eliminare il prompt, usa il parametro Force.</span><span class="sxs-lookup"><span data-stu-id="48b85-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="48b85-114">Se sono state apportate assegnazioni di ruolo per il ruolo personalizzato da eliminare, l'eliminazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="48b85-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="48b85-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48b85-115">EXAMPLES</span></span>

### <span data-ttu-id="48b85-116">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="48b85-116">--------------------------  Example 1  --------------------------</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="48b85-117">--------------------------Esempio 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="48b85-117">--------------------------  Example 2  --------------------------</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="48b85-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48b85-118">PARAMETERS</span></span>

### <span data-ttu-id="48b85-119">-Force</span><span class="sxs-lookup"><span data-stu-id="48b85-119">-Force</span></span>
<span data-ttu-id="48b85-120">Se impostato, non richiede una conferma prima di eliminare il ruolo personalizzato</span><span class="sxs-lookup"><span data-stu-id="48b85-120">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="48b85-121">-ID</span><span class="sxs-lookup"><span data-stu-id="48b85-121">-Id</span></span>
<span data-ttu-id="48b85-122">ID della definizione del ruolo da eliminare</span><span class="sxs-lookup"><span data-stu-id="48b85-122">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="48b85-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="48b85-123">-Name</span></span>
<span data-ttu-id="48b85-124">Nome della definizione del ruolo da eliminare.</span><span class="sxs-lookup"><span data-stu-id="48b85-124">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="48b85-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48b85-125">-PassThru</span></span>
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

### <span data-ttu-id="48b85-126">-Ambito</span><span class="sxs-lookup"><span data-stu-id="48b85-126">-Scope</span></span>
<span data-ttu-id="48b85-127">Ambito della definizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="48b85-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b85-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="48b85-128">-Confirm</span></span>
<span data-ttu-id="48b85-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48b85-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48b85-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b85-130">-WhatIf</span></span>
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

### <span data-ttu-id="48b85-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b85-131">-DefaultProfile</span></span>
<span data-ttu-id="48b85-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48b85-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48b85-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b85-133">CommonParameters</span></span>
<span data-ttu-id="48b85-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b85-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b85-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b85-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b85-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48b85-136">INPUTS</span></span>

## <span data-ttu-id="48b85-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48b85-137">OUTPUTS</span></span>

### <span data-ttu-id="48b85-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48b85-138">System.Boolean</span></span>

## <span data-ttu-id="48b85-139">Note</span><span class="sxs-lookup"><span data-stu-id="48b85-139">NOTES</span></span>
<span data-ttu-id="48b85-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="48b85-140">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="48b85-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48b85-141">RELATED LINKS</span></span>

[<span data-ttu-id="48b85-142">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="48b85-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="48b85-143">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="48b85-143">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="48b85-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="48b85-144">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

