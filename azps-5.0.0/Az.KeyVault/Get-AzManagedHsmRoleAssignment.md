---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 20e80617d47cd0a1f0ffb5cdb80d836656cd9abd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193264"
---
# <span data-ttu-id="30353-101">Get-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="30353-101">Get-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="30353-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30353-102">SYNOPSIS</span></span>
<span data-ttu-id="30353-103">Ottenere o elencare le assegnazioni di ruolo di un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="30353-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="30353-104">Usare i rispettivi parametri per elencare le assegnazioni a un utente specifico o a una definizione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="30353-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="30353-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30353-105">SYNTAX</span></span>

### <span data-ttu-id="30353-106">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="30353-106">List (Default)</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30353-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="30353-107">GetByName</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30353-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30353-108">DESCRIPTION</span></span>
<span data-ttu-id="30353-109">Usare il `Get-AzManagedHsmRoleAssignment` comando per elencare tutte le assegnazioni di ruolo effettive in un ambito.</span><span class="sxs-lookup"><span data-stu-id="30353-109">Use the `Get-AzManagedHsmRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="30353-110">Senza parametri, questo comando restituisce tutte le assegnazioni di ruolo effettuate sotto l'HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="30353-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="30353-111">Questo elenco può essere filtrato usando i parametri di filtro per Principal, Role e scope.</span><span class="sxs-lookup"><span data-stu-id="30353-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="30353-112">L'oggetto dell'assegnazione deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="30353-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="30353-113">Per specificare un utente, USA SignInName o i parametri di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="30353-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="30353-114">Per specificare un gruppo di sicurezza, usare il parametro di Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="30353-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="30353-115">Per specificare un'applicazione Azure AD, USA i parametri ApplicationId o ObjectId.</span><span class="sxs-lookup"><span data-stu-id="30353-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="30353-116">Il ruolo che viene assegnato deve essere specificato usando il parametro RoleDefinitionName o RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="30353-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="30353-117">L'ambito in cui viene concesso l'accesso può essere specificato.</span><span class="sxs-lookup"><span data-stu-id="30353-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="30353-118">Il valore predefinito è "/".</span><span class="sxs-lookup"><span data-stu-id="30353-118">It defaults to "/".</span></span>

## <span data-ttu-id="30353-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30353-119">EXAMPLES</span></span>

### <span data-ttu-id="30353-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30353-120">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="30353-121">Questo esempio elenca tutte le assegnazioni di ruolo di "myHsm" in tutti gli ambiti.</span><span class="sxs-lookup"><span data-stu-id="30353-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="30353-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="30353-122">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="30353-123">Questo esempio elenca tutte le assegnazioni di ruolo di "myHsm" nell'ambito "/Keys" e filtra il risultato per nome di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="30353-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="30353-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30353-124">PARAMETERS</span></span>

### <span data-ttu-id="30353-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="30353-125">-ApplicationId</span></span>
<span data-ttu-id="30353-126">SPN dell'app.</span><span class="sxs-lookup"><span data-stu-id="30353-126">The app SPN.</span></span>

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

### <span data-ttu-id="30353-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30353-127">-DefaultProfile</span></span>
<span data-ttu-id="30353-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30353-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30353-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="30353-129">-HsmName</span></span>
<span data-ttu-id="30353-130">Nome dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="30353-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="30353-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="30353-131">-ObjectId</span></span>
<span data-ttu-id="30353-132">ID oggetto utente o gruppo.</span><span class="sxs-lookup"><span data-stu-id="30353-132">The user or group object id.</span></span>

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

### <span data-ttu-id="30353-133">-RoleAssignmentname</span><span class="sxs-lookup"><span data-stu-id="30353-133">-RoleAssignmentName</span></span>
<span data-ttu-id="30353-134">Nome dell'assegnazione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="30353-134">Name of the role assignment.</span></span>

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

### <span data-ttu-id="30353-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="30353-135">-RoleDefinitionId</span></span>
<span data-ttu-id="30353-136">ID ruolo a cui è assegnata l'entità.</span><span class="sxs-lookup"><span data-stu-id="30353-136">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="30353-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="30353-137">-RoleDefinitionName</span></span>
<span data-ttu-id="30353-138">Nome del ruolo RBAC a cui assegnare l'entità.</span><span class="sxs-lookup"><span data-stu-id="30353-138">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="30353-139">-Ambito</span><span class="sxs-lookup"><span data-stu-id="30353-139">-Scope</span></span>
<span data-ttu-id="30353-140">Ambito a cui si applica l'assegnazione di ruolo o la definizione, ad esempio "/" o "/Keys" o "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="30353-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="30353-141">Quando viene omesso, viene usato "/".</span><span class="sxs-lookup"><span data-stu-id="30353-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="30353-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="30353-142">-SignInName</span></span>
<span data-ttu-id="30353-143">L'utente SignInName.</span><span class="sxs-lookup"><span data-stu-id="30353-143">The user SignInName.</span></span>

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

### <span data-ttu-id="30353-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30353-144">CommonParameters</span></span>
<span data-ttu-id="30353-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30353-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30353-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30353-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30353-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30353-147">INPUTS</span></span>

### <span data-ttu-id="30353-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="30353-148">None</span></span>

## <span data-ttu-id="30353-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30353-149">OUTPUTS</span></span>

### <span data-ttu-id="30353-150">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="30353-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="30353-151">Note</span><span class="sxs-lookup"><span data-stu-id="30353-151">NOTES</span></span>

## <span data-ttu-id="30353-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30353-152">RELATED LINKS</span></span>
