---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: ee90ab1b4ba22f1a5c40427f7fc435c75cef992d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336976"
---
# <span data-ttu-id="a2585-101">New-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a2585-101">New-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="a2585-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2585-102">SYNOPSIS</span></span>
<span data-ttu-id="a2585-103">Assegna il ruolo RBAC specificato all'oggetto Principal specificato, in corrispondenza dell'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="a2585-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="a2585-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2585-104">SYNTAX</span></span>

### <span data-ttu-id="a2585-105">DefinitionNameSignInName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2585-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2585-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="a2585-106">DefinitionNameApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2585-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="a2585-107">DefinitionNameObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2585-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="a2585-108">DefinitionIdApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2585-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="a2585-109">DefinitionIdObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2585-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="a2585-110">DefinitionIdSignInName</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2585-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2585-111">DESCRIPTION</span></span>
<span data-ttu-id="a2585-112">Usare il `New-AzKeyVaultRoleAssignment` comando per concedere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="a2585-112">Use the `New-AzKeyVaultRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="a2585-113">L'accesso viene concesso assegnando il ruolo RBAC appropriato all'ambito corretto.</span><span class="sxs-lookup"><span data-stu-id="a2585-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="a2585-114">L'oggetto dell'assegnazione deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="a2585-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="a2585-115">Per specificare un utente, USA SignInName o i parametri di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="a2585-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="a2585-116">Per specificare un gruppo di sicurezza, usare il parametro di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="a2585-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="a2585-117">Per specificare un'applicazione Azure AD, USA i parametri ApplicationId o ObjectId.</span><span class="sxs-lookup"><span data-stu-id="a2585-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="a2585-118">Il ruolo che viene assegnato deve essere specificato usando il parametro RoleDefinitionName PR RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="a2585-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="a2585-119">L'ambito in cui viene concesso l'accesso può essere specificato.</span><span class="sxs-lookup"><span data-stu-id="a2585-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="a2585-120">Il valore predefinito è l'abbonamento selezionato.</span><span class="sxs-lookup"><span data-stu-id="a2585-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="a2585-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2585-121">EXAMPLES</span></span>

### <span data-ttu-id="a2585-122">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2585-122">Example 1</span></span>
```powershell
PS C:\> New-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="a2585-123">Questo esempio assegna il ruolo "amministratore dei criteri HSM gestito" all'utente " user1@microsoft.com " all'ambito superiore.</span><span class="sxs-lookup"><span data-stu-id="a2585-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="a2585-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2585-124">PARAMETERS</span></span>

### <span data-ttu-id="a2585-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a2585-125">-ApplicationId</span></span>
<span data-ttu-id="a2585-126">SPN dell'app.</span><span class="sxs-lookup"><span data-stu-id="a2585-126">The app SPN.</span></span>

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

### <span data-ttu-id="a2585-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2585-127">-DefaultProfile</span></span>
<span data-ttu-id="a2585-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2585-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2585-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="a2585-129">-HsmName</span></span>
<span data-ttu-id="a2585-130">Nome dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="a2585-130">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2585-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a2585-131">-ObjectId</span></span>
<span data-ttu-id="a2585-132">ID oggetto utente o gruppo.</span><span class="sxs-lookup"><span data-stu-id="a2585-132">The user or group object id.</span></span>

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

### <span data-ttu-id="a2585-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a2585-133">-RoleDefinitionId</span></span>
<span data-ttu-id="a2585-134">ID ruolo a cui è assegnata l'entità.</span><span class="sxs-lookup"><span data-stu-id="a2585-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="a2585-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a2585-135">-RoleDefinitionName</span></span>
<span data-ttu-id="a2585-136">Nome del ruolo RBAC a cui assegnare l'entità.</span><span class="sxs-lookup"><span data-stu-id="a2585-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="a2585-137">-Ambito</span><span class="sxs-lookup"><span data-stu-id="a2585-137">-Scope</span></span>
<span data-ttu-id="a2585-138">Ambito a cui si applica l'assegnazione di ruolo o la definizione, ad esempio "/" o "/Keys" o "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="a2585-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="a2585-139">Quando viene omesso, viene usato "/".</span><span class="sxs-lookup"><span data-stu-id="a2585-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="a2585-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="a2585-140">-SignInName</span></span>
<span data-ttu-id="a2585-141">L'utente SignInName.</span><span class="sxs-lookup"><span data-stu-id="a2585-141">The user SignInName.</span></span>

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

### <span data-ttu-id="a2585-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a2585-142">-Confirm</span></span>
<span data-ttu-id="a2585-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2585-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2585-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2585-144">-WhatIf</span></span>
<span data-ttu-id="a2585-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2585-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2585-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2585-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2585-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2585-147">CommonParameters</span></span>
<span data-ttu-id="a2585-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2585-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2585-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2585-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2585-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2585-150">INPUTS</span></span>

### <span data-ttu-id="a2585-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a2585-151">None</span></span>

## <span data-ttu-id="a2585-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2585-152">OUTPUTS</span></span>

### <span data-ttu-id="a2585-153">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a2585-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="a2585-154">Note</span><span class="sxs-lookup"><span data-stu-id="a2585-154">NOTES</span></span>

## <span data-ttu-id="a2585-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2585-155">RELATED LINKS</span></span>
