---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: 9db953cf4c02497fd3056a57ed7b71a78687411d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688544"
---
# <span data-ttu-id="0da23-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0da23-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="0da23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0da23-102">SYNOPSIS</span></span>
<span data-ttu-id="0da23-103">Elenca tutti i ruoli RBAC di Azure disponibili per l'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="0da23-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0da23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0da23-104">SYNTAX</span></span>

### <span data-ttu-id="0da23-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da23-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0da23-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da23-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0da23-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da23-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0da23-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0da23-108">DESCRIPTION</span></span>
<span data-ttu-id="0da23-109">Usare il comando Get-AzureRmRoleDefinition con un nome di ruolo specifico per visualizzarne i dettagli.</span><span class="sxs-lookup"><span data-stu-id="0da23-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="0da23-110">Per esaminare le singole operazioni a cui un ruolo concede l'accesso, esaminare le proprietà azioni e notaction del ruolo.</span><span class="sxs-lookup"><span data-stu-id="0da23-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="0da23-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0da23-111">EXAMPLES</span></span>

### <span data-ttu-id="0da23-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0da23-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="0da23-113">Ottenere la definizione del ruolo di lettura</span><span class="sxs-lookup"><span data-stu-id="0da23-113">Get the Reader role definition</span></span>

### <span data-ttu-id="0da23-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0da23-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="0da23-115">Elenca tutte le definizioni di ruolo RBAC</span><span class="sxs-lookup"><span data-stu-id="0da23-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="0da23-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0da23-116">PARAMETERS</span></span>

### <span data-ttu-id="0da23-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="0da23-117">-Custom</span></span>
<span data-ttu-id="0da23-118">Se specificato, Visualizza solo i ruoli creati personalizzati nella directory.</span><span class="sxs-lookup"><span data-stu-id="0da23-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="0da23-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da23-119">-DefaultProfile</span></span>
<span data-ttu-id="0da23-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0da23-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0da23-121">-ID</span><span class="sxs-lookup"><span data-stu-id="0da23-121">-Id</span></span>
<span data-ttu-id="0da23-122">ID definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="0da23-122">Role definition Id.</span></span>

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

### <span data-ttu-id="0da23-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0da23-123">-Name</span></span>
<span data-ttu-id="0da23-124">Nome definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="0da23-124">Role definition name.</span></span>
<span data-ttu-id="0da23-125">Ad esempio, Reader, Contributor, Virtual Machine Contributor.</span><span class="sxs-lookup"><span data-stu-id="0da23-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="0da23-126">-Ambito</span><span class="sxs-lookup"><span data-stu-id="0da23-126">-Scope</span></span>
<span data-ttu-id="0da23-127">Ambito della definizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="0da23-127">Role definition scope.</span></span>

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

### <span data-ttu-id="0da23-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da23-128">CommonParameters</span></span>
<span data-ttu-id="0da23-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da23-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da23-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da23-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da23-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0da23-131">INPUTS</span></span>

### <span data-ttu-id="0da23-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0da23-132">System.String</span></span>
<span data-ttu-id="0da23-133">Parametri: ambito (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0da23-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="0da23-134">System. Guid</span><span class="sxs-lookup"><span data-stu-id="0da23-134">System.Guid</span></span>

### <span data-ttu-id="0da23-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0da23-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0da23-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0da23-136">OUTPUTS</span></span>

### <span data-ttu-id="0da23-137">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0da23-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="0da23-138">Note</span><span class="sxs-lookup"><span data-stu-id="0da23-138">NOTES</span></span>
<span data-ttu-id="0da23-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="0da23-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0da23-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0da23-140">RELATED LINKS</span></span>

[<span data-ttu-id="0da23-141">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0da23-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="0da23-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0da23-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="0da23-143">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0da23-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="0da23-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0da23-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)
