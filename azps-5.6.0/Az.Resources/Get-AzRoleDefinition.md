---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 724daa3cce0bd8fe38a645fcdd3acd2d3ce7bf1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990778"
---
# <span data-ttu-id="1ae31-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1ae31-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="1ae31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ae31-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae31-103">Elenco di tutti i ruoli di Azure RBAC disponibili per l'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="1ae31-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="1ae31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ae31-104">SYNTAX</span></span>

### <span data-ttu-id="1ae31-105">RoleDefinitionNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ae31-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ae31-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae31-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ae31-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae31-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ae31-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1ae31-108">DESCRIPTION</span></span>
<span data-ttu-id="1ae31-109">Usare il Get-AzRoleDefinition comando Visualizza con un particolare nome di ruolo per visualizzarne i dettagli.</span><span class="sxs-lookup"><span data-stu-id="1ae31-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="1ae31-110">Per esaminare le singole operazioni a cui un ruolo concede l'accesso, esaminare le proprietà Actions e NotActions del ruolo.</span><span class="sxs-lookup"><span data-stu-id="1ae31-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="1ae31-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ae31-111">EXAMPLES</span></span>

### <span data-ttu-id="1ae31-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1ae31-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="1ae31-113">Ottenere la definizione del ruolo di lettore</span><span class="sxs-lookup"><span data-stu-id="1ae31-113">Get the Reader role definition</span></span>

### <span data-ttu-id="1ae31-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1ae31-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="1ae31-115">Elenco di tutte le definizioni di ruolo RBAC</span><span class="sxs-lookup"><span data-stu-id="1ae31-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="1ae31-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ae31-116">PARAMETERS</span></span>

### <span data-ttu-id="1ae31-117">-Personalizzato</span><span class="sxs-lookup"><span data-stu-id="1ae31-117">-Custom</span></span>
<span data-ttu-id="1ae31-118">Se specificato, nella directory vengono visualizzati solo i ruoli creati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="1ae31-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="1ae31-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae31-119">-DefaultProfile</span></span>
<span data-ttu-id="1ae31-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1ae31-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ae31-121">-Id</span><span class="sxs-lookup"><span data-stu-id="1ae31-121">-Id</span></span>
<span data-ttu-id="1ae31-122">ID definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="1ae31-122">Role definition Id.</span></span>

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

### <span data-ttu-id="1ae31-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1ae31-123">-Name</span></span>
<span data-ttu-id="1ae31-124">Nome della definizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="1ae31-124">Role definition name.</span></span>
<span data-ttu-id="1ae31-125">Ad esempio Lettore, Collaboratore, Collaboratore macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ae31-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="1ae31-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="1ae31-126">-Scope</span></span>
<span data-ttu-id="1ae31-127">Ambito della definizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="1ae31-127">Role definition scope.</span></span>

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

### <span data-ttu-id="1ae31-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae31-128">CommonParameters</span></span>
<span data-ttu-id="1ae31-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae31-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae31-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1ae31-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae31-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="1ae31-131">INPUTS</span></span>

### <span data-ttu-id="1ae31-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1ae31-132">System.String</span></span>

### <span data-ttu-id="1ae31-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1ae31-133">System.Guid</span></span>

### <span data-ttu-id="1ae31-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ae31-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1ae31-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ae31-135">OUTPUTS</span></span>

### <span data-ttu-id="1ae31-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1ae31-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="1ae31-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="1ae31-137">NOTES</span></span>
<span data-ttu-id="1ae31-138">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione</span><span class="sxs-lookup"><span data-stu-id="1ae31-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1ae31-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ae31-139">RELATED LINKS</span></span>

[<span data-ttu-id="1ae31-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1ae31-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="1ae31-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1ae31-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="1ae31-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1ae31-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="1ae31-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1ae31-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

