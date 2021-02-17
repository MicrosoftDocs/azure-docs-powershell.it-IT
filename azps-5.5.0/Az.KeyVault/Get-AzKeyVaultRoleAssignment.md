---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: c610339bf90069f30d6107d46fc92fd896d6816c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188167"
---
# <span data-ttu-id="34e43-101">Get-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="34e43-101">Get-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="34e43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34e43-102">SYNOPSIS</span></span>
<span data-ttu-id="34e43-103">Ottenere o elencare le assegnazioni di ruoli di un servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="34e43-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="34e43-104">Usare i rispettivi parametri per elencare le assegnazioni a un utente specifico o a una definizione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="34e43-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="34e43-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34e43-105">SYNTAX</span></span>

### <span data-ttu-id="34e43-106">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34e43-106">List (Default)</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34e43-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="34e43-107">GetByName</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34e43-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34e43-108">DESCRIPTION</span></span>
<span data-ttu-id="34e43-109">Usare il `Get-AzKeyVaultRoleAssignment` comando per elencare tutte le assegnazioni di ruolo efficaci in un ambito.</span><span class="sxs-lookup"><span data-stu-id="34e43-109">Use the `Get-AzKeyVaultRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="34e43-110">Senza parametri, questo comando restituisce tutte le assegnazioni di ruolo effettuate nel servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="34e43-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="34e43-111">Questo elenco può essere filtrato usando i parametri di filtro per l'entità, il ruolo e l'ambito.</span><span class="sxs-lookup"><span data-stu-id="34e43-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="34e43-112">È necessario specificare l'oggetto dell'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="34e43-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="34e43-113">Per specificare un utente, usare i parametri SignInName o Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="34e43-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="34e43-114">Per specificare un gruppo di sicurezza, usare il parametro ObjectId di Azure AD.</span><span class="sxs-lookup"><span data-stu-id="34e43-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="34e43-115">Per specificare un'applicazione Azure AD, usare i parametri ApplicationId o ObjectId.</span><span class="sxs-lookup"><span data-stu-id="34e43-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="34e43-116">Il ruolo da assegnare deve essere specificato usando il parametro RoleDefinitionName o RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="34e43-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="34e43-117">È possibile specificare l'ambito in cui viene concesso l'accesso.</span><span class="sxs-lookup"><span data-stu-id="34e43-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="34e43-118">Il valore predefinito è "/".</span><span class="sxs-lookup"><span data-stu-id="34e43-118">It defaults to "/".</span></span>

## <span data-ttu-id="34e43-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34e43-119">EXAMPLES</span></span>

### <span data-ttu-id="34e43-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="34e43-120">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="34e43-121">Questo esempio elenca tutte le assegnazioni di ruolo di "myHsm" in tutto l'ambito.</span><span class="sxs-lookup"><span data-stu-id="34e43-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="34e43-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="34e43-122">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="34e43-123">Questo esempio elenca tutte le assegnazioni di ruolo di "myHsm" nell'ambito "/keys" e filtra il risultato in base al nome di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="34e43-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="34e43-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34e43-124">PARAMETERS</span></span>

### <span data-ttu-id="34e43-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="34e43-125">-ApplicationId</span></span>
<span data-ttu-id="34e43-126">Nome SPN dell'app.</span><span class="sxs-lookup"><span data-stu-id="34e43-126">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e43-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e43-127">-DefaultProfile</span></span>
<span data-ttu-id="34e43-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34e43-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34e43-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="34e43-129">-HsmName</span></span>
<span data-ttu-id="34e43-130">Nome dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="34e43-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="34e43-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="34e43-131">-ObjectId</span></span>
<span data-ttu-id="34e43-132">ID oggetto utente o gruppo.</span><span class="sxs-lookup"><span data-stu-id="34e43-132">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e43-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="34e43-133">-RoleAssignmentName</span></span>
<span data-ttu-id="34e43-134">Nome dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="34e43-134">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e43-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="34e43-135">-RoleDefinitionId</span></span>
<span data-ttu-id="34e43-136">ID ruolo a cui è assegnata l'entità.</span><span class="sxs-lookup"><span data-stu-id="34e43-136">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e43-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="34e43-137">-RoleDefinitionName</span></span>
<span data-ttu-id="34e43-138">Nome del ruolo RBAC a cui assegnare l'entità.</span><span class="sxs-lookup"><span data-stu-id="34e43-138">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e43-139">-Scope</span><span class="sxs-lookup"><span data-stu-id="34e43-139">-Scope</span></span>
<span data-ttu-id="34e43-140">Ambito in cui si applica la definizione o l'assegnazione di ruolo, ad esempio '/' o '/keys' o '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="34e43-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="34e43-141">'/' viene usato quando viene omesso.</span><span class="sxs-lookup"><span data-stu-id="34e43-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="34e43-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="34e43-142">-SignInName</span></span>
<span data-ttu-id="34e43-143">L'utente SignInName.</span><span class="sxs-lookup"><span data-stu-id="34e43-143">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e43-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e43-144">CommonParameters</span></span>
<span data-ttu-id="34e43-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e43-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e43-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34e43-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e43-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="34e43-147">INPUTS</span></span>

### <span data-ttu-id="34e43-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="34e43-148">None</span></span>

## <span data-ttu-id="34e43-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34e43-149">OUTPUTS</span></span>

### <span data-ttu-id="34e43-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="34e43-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="34e43-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="34e43-151">NOTES</span></span>

## <span data-ttu-id="34e43-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34e43-152">RELATED LINKS</span></span>
