---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 9342ea2486c28a44ba7ff4a22f21619846ac7010
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351688"
---
# <span data-ttu-id="04451-101">Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="04451-101">Set-AzRoleAssignment</span></span>

## <span data-ttu-id="04451-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04451-102">SYNOPSIS</span></span>
<span data-ttu-id="04451-103">Aggiornare un'assegnazione di ruolo esistente.</span><span class="sxs-lookup"><span data-stu-id="04451-103">Update an existing Role Assignment.</span></span>

## <span data-ttu-id="04451-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04451-104">SYNTAX</span></span>

### <span data-ttu-id="04451-105">RoleAssignmentParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="04451-105">RoleAssignmentParameterSet (Default)</span></span>
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04451-106">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="04451-106">InputFileParameterSet</span></span>
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04451-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04451-107">DESCRIPTION</span></span>
<span data-ttu-id="04451-108">Usare il comando New-AzRoleAssignment per modificare un'assegnazione esistente.</span><span class="sxs-lookup"><span data-stu-id="04451-108">Use the New-AzRoleAssignment command to modify an existing assignment.</span></span>  
<span data-ttu-id="04451-109">Le descrizioni possono essere qualsiasi stringa valida, che può essere usata per diferentiate l'una dall'altra.</span><span class="sxs-lookup"><span data-stu-id="04451-109">Descriptions can be any valid string, use that to diferentiate from one another.</span></span>  
<span data-ttu-id="04451-110">Se la condizione è impostata anche la versione della condizione deve essere impostata, ma se si sta aggiornando una condizione che non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="04451-110">if Condition is set Condition Version has to be set as well but if you're updating a Condition that is not necesary.</span></span>
<span data-ttu-id="04451-111">La versione della condizione può essere aggiornata da 1,0 a 2,0, ma non può essere retroceduta.</span><span class="sxs-lookup"><span data-stu-id="04451-111">Condition Version can be upgraded from 1.0 to 2.0 but it can't not be downgraded back.</span></span> <span data-ttu-id="04451-112">Essere prudenti dato che 2,0 non è retrocompatible con 1,0.</span><span class="sxs-lookup"><span data-stu-id="04451-112">Be cautious as 2.0 is not retrocompatible with 1.0.</span></span>

## <span data-ttu-id="04451-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04451-113">EXAMPLES</span></span>

### <span data-ttu-id="04451-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="04451-114">Example 1</span></span>
```powershell
$ConditionVersion = "2.0"
  $Description = "This is a new role assignment for John"
  $Condition = "@Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'"

  $roleAssignment = Get-AzRoleAssignment -Scope "/subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg" -PrincipalId "0c0f6cdc-90dd-4664-83c0-a0d986c4c604"
  $roleAssignment.Description = $Description
  $roleAssignment.Condition = $Condition
  $roleAssignment.ConditionVersion = $ConditionVersion

  Set-AzRoleAssignment -InputObject $roleAssignment -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="04451-115">Aggiornare un'assegnazione di ruolo esistente modificando un oggetto</span><span class="sxs-lookup"><span data-stu-id="04451-115">Update an existing role assignment by modifying an object</span></span>

### <span data-ttu-id="04451-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="04451-116">Example 2</span></span>
```powershell
Set-AzRoleAssignment -InputFile "C:\RoleAssignments\example.json" -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="04451-117">Aggiornare un'assegnazione di ruolo esistente usando un file</span><span class="sxs-lookup"><span data-stu-id="04451-117">Update an existing role assignment by using a file</span></span>

## <span data-ttu-id="04451-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04451-118">PARAMETERS</span></span>

### <span data-ttu-id="04451-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04451-119">-DefaultProfile</span></span>
<span data-ttu-id="04451-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04451-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04451-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="04451-121">-InputFile</span></span>
<span data-ttu-id="04451-122">Nome file contenente una singola definizione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="04451-122">File name containing a single role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04451-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04451-123">-InputObject</span></span>
<span data-ttu-id="04451-124">Assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="04451-124">Role Assignment.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04451-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04451-125">-PassThru</span></span>
<span data-ttu-id="04451-126">Se specificato, Visualizza l'assegnazione di ruolo aggiornata</span><span class="sxs-lookup"><span data-stu-id="04451-126">If specified, displays the updated role assignment</span></span>

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

### <span data-ttu-id="04451-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="04451-127">-Confirm</span></span>
<span data-ttu-id="04451-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04451-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04451-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04451-129">-WhatIf</span></span>
<span data-ttu-id="04451-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04451-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04451-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04451-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04451-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04451-132">CommonParameters</span></span>
<span data-ttu-id="04451-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04451-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04451-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04451-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04451-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04451-135">INPUTS</span></span>

### <span data-ttu-id="04451-136">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="04451-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="04451-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04451-137">OUTPUTS</span></span>

### <span data-ttu-id="04451-138">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="04451-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="04451-139">Note</span><span class="sxs-lookup"><span data-stu-id="04451-139">NOTES</span></span>

## <span data-ttu-id="04451-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04451-140">RELATED LINKS</span></span>
