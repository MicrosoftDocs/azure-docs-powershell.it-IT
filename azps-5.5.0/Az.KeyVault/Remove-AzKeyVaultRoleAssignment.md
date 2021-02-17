---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 9e2dd07ac0346cacb99bbcc2e05d47b57ac8ccd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180439"
---
# <span data-ttu-id="aa709-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="aa709-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="aa709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa709-102">SYNOPSIS</span></span>
<span data-ttu-id="aa709-103">Rimuove un'assegnazione di ruolo all'entità specificata assegnata a un particolare ruolo in un particolare ambito.</span><span class="sxs-lookup"><span data-stu-id="aa709-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="aa709-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa709-104">SYNTAX</span></span>

### <span data-ttu-id="aa709-105">DefinitionNameSignInName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa709-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa709-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="aa709-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa709-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="aa709-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa709-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="aa709-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa709-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="aa709-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa709-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="aa709-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa709-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa709-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa709-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="aa709-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa709-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aa709-113">DESCRIPTION</span></span>
<span data-ttu-id="aa709-114">Usare il `Remove-AzKeyVaultRoleAssignment` cmdlet per revocare l'accesso a qualsiasi entità in base all'ambito e al ruolo assegnato.</span><span class="sxs-lookup"><span data-stu-id="aa709-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="aa709-115">Oggetto dell'assegnazione, ad esempio l'entità DEVE essere specificata.</span><span class="sxs-lookup"><span data-stu-id="aa709-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="aa709-116">L'entità può essere un utente (usare i parametri SignInName o ObjectId per identificare un utente), un gruppo di sicurezza (usare il parametro ObjectId per identificare un gruppo) o un'entità servizio (usare parametri ApplicationId o ObjectId per identificare un ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="aa709-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="aa709-117">Il ruolo a cui è assegnata l'entità DEVE essere specificato usando il parametro RoleDefinitionName o RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="aa709-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="aa709-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa709-118">EXAMPLES</span></span>

### <span data-ttu-id="aa709-119">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aa709-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="aa709-120">Questo esempio revoca il ruolo di "Amministratore dei criteri HSM gestito" di user1@microsoft.com " " nell'ambito "/keys".</span><span class="sxs-lookup"><span data-stu-id="aa709-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="aa709-121">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="aa709-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="aa709-122">Questo esempio revoca tutti i ruoli di " user1@microsoft.com " in tutti gli ambiti.</span><span class="sxs-lookup"><span data-stu-id="aa709-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="aa709-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa709-123">PARAMETERS</span></span>

### <span data-ttu-id="aa709-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="aa709-124">-ApplicationId</span></span>
<span data-ttu-id="aa709-125">Nome SPN dell'app.</span><span class="sxs-lookup"><span data-stu-id="aa709-125">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameApplicationId, DefinitionIdApplicationId
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa709-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa709-126">-DefaultProfile</span></span>
<span data-ttu-id="aa709-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa709-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa709-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="aa709-128">-HsmName</span></span>
<span data-ttu-id="aa709-129">Nome dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="aa709-129">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId, DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName, RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa709-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa709-130">-InputObject</span></span>
<span data-ttu-id="aa709-131">Oggetto assegnazione ruolo.</span><span class="sxs-lookup"><span data-stu-id="aa709-131">Role assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa709-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="aa709-132">-ObjectId</span></span>
<span data-ttu-id="aa709-133">ID oggetto utente o gruppo.</span><span class="sxs-lookup"><span data-stu-id="aa709-133">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameObjectId, DefinitionIdObjectId
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa709-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa709-134">-PassThru</span></span>
<span data-ttu-id="aa709-135">Restituisce true quando il servizio HSM viene ripristinato.</span><span class="sxs-lookup"><span data-stu-id="aa709-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="aa709-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="aa709-136">-RoleAssignmentName</span></span>
<span data-ttu-id="aa709-137">Nome dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="aa709-137">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa709-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="aa709-138">-RoleDefinitionId</span></span>
<span data-ttu-id="aa709-139">ID ruolo a cui è assegnata l'entità.</span><span class="sxs-lookup"><span data-stu-id="aa709-139">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa709-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="aa709-140">-RoleDefinitionName</span></span>
<span data-ttu-id="aa709-141">Nome del ruolo RBAC a cui assegnare l'entità.</span><span class="sxs-lookup"><span data-stu-id="aa709-141">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa709-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="aa709-142">-Scope</span></span>
<span data-ttu-id="aa709-143">Ambito in cui si applica la definizione o l'assegnazione di ruolo, ad esempio '/' o '/keys' o '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="aa709-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="aa709-144">'/' viene usato quando viene omesso.</span><span class="sxs-lookup"><span data-stu-id="aa709-144">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa709-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="aa709-145">-SignInName</span></span>
<span data-ttu-id="aa709-146">L'utente SignInName.</span><span class="sxs-lookup"><span data-stu-id="aa709-146">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionIdSignInName
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa709-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa709-147">-Confirm</span></span>
<span data-ttu-id="aa709-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa709-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa709-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa709-149">-WhatIf</span></span>
<span data-ttu-id="aa709-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa709-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa709-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa709-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa709-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa709-152">CommonParameters</span></span>
<span data-ttu-id="aa709-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa709-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa709-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa709-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa709-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="aa709-155">INPUTS</span></span>

### <span data-ttu-id="aa709-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="aa709-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="aa709-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa709-157">OUTPUTS</span></span>

### <span data-ttu-id="aa709-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="aa709-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="aa709-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="aa709-159">NOTES</span></span>

## <span data-ttu-id="aa709-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa709-160">RELATED LINKS</span></span>
