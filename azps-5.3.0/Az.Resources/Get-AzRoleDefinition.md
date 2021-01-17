---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 5cd9a76f71f63b1d16003cce467d2d91eddc5b04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474246"
---
# <span data-ttu-id="8ea11-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8ea11-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="8ea11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ea11-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea11-103">Elenca tutti i ruoli RBAC di Azure disponibili per l'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="8ea11-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="8ea11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ea11-104">SYNTAX</span></span>

### <span data-ttu-id="8ea11-105">RoleDefinitionNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ea11-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ea11-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea11-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ea11-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea11-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ea11-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ea11-108">DESCRIPTION</span></span>
<span data-ttu-id="8ea11-109">Usare il comando Get-AzRoleDefinition con un nome di ruolo specifico per visualizzarne i dettagli.</span><span class="sxs-lookup"><span data-stu-id="8ea11-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="8ea11-110">Per esaminare le singole operazioni a cui un ruolo concede l'accesso, esaminare le proprietà azioni e notaction del ruolo.</span><span class="sxs-lookup"><span data-stu-id="8ea11-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="8ea11-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ea11-111">EXAMPLES</span></span>

### <span data-ttu-id="8ea11-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8ea11-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="8ea11-113">Ottenere la definizione del ruolo di lettura</span><span class="sxs-lookup"><span data-stu-id="8ea11-113">Get the Reader role definition</span></span>

### <span data-ttu-id="8ea11-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8ea11-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="8ea11-115">Elenca tutte le definizioni di ruolo RBAC</span><span class="sxs-lookup"><span data-stu-id="8ea11-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="8ea11-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ea11-116">PARAMETERS</span></span>

### <span data-ttu-id="8ea11-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="8ea11-117">-Custom</span></span>
<span data-ttu-id="8ea11-118">Se specificato, Visualizza solo i ruoli creati personalizzati nella directory.</span><span class="sxs-lookup"><span data-stu-id="8ea11-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea11-119">-DefaultProfile</span></span>
<span data-ttu-id="8ea11-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8ea11-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ea11-121">-ID</span><span class="sxs-lookup"><span data-stu-id="8ea11-121">-Id</span></span>
<span data-ttu-id="8ea11-122">ID definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="8ea11-122">Role definition Id.</span></span>

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

### <span data-ttu-id="8ea11-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ea11-123">-Name</span></span>
<span data-ttu-id="8ea11-124">Nome definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="8ea11-124">Role definition name.</span></span>
<span data-ttu-id="8ea11-125">Ad esempio, Reader, Contributor, Virtual Machine Contributor.</span><span class="sxs-lookup"><span data-stu-id="8ea11-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea11-126">-Ambito</span><span class="sxs-lookup"><span data-stu-id="8ea11-126">-Scope</span></span>
<span data-ttu-id="8ea11-127">Ambito della definizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="8ea11-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea11-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea11-128">CommonParameters</span></span>
<span data-ttu-id="8ea11-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ea11-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea11-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ea11-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea11-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ea11-131">INPUTS</span></span>

### <span data-ttu-id="8ea11-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8ea11-132">System.String</span></span>

### <span data-ttu-id="8ea11-133">System. Guid</span><span class="sxs-lookup"><span data-stu-id="8ea11-133">System.Guid</span></span>

### <span data-ttu-id="8ea11-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8ea11-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8ea11-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ea11-135">OUTPUTS</span></span>

### <span data-ttu-id="8ea11-136">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8ea11-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="8ea11-137">Note</span><span class="sxs-lookup"><span data-stu-id="8ea11-137">NOTES</span></span>
<span data-ttu-id="8ea11-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="8ea11-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8ea11-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ea11-139">RELATED LINKS</span></span>

[<span data-ttu-id="8ea11-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8ea11-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="8ea11-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8ea11-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="8ea11-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8ea11-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="8ea11-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8ea11-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

