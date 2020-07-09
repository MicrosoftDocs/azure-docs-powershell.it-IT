---
title: Usare le entità servizio di Azure con Azure PowerShell
description: Informazioni su come creare e usare entità servizio con Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.openlocfilehash: 9d1f0e3be894a592bdf105c2070e9db0cf882921
ms.sourcegitcommit: e324ad44921c9d8228ec7b91f3f8b333d2c520d4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2020
ms.locfileid: "86127773"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="dcf19-103">Creare un'entità servizio di Azure con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="dcf19-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="dcf19-104">Gli strumenti automatici che usano i servizi di Azure devono sempre avere autorizzazioni limitate.</span><span class="sxs-lookup"><span data-stu-id="dcf19-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="dcf19-105">Invece di consentire alle applicazioni l'accesso come utenti con privilegi completi, Azure offre le identità servizio.</span><span class="sxs-lookup"><span data-stu-id="dcf19-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="dcf19-106">Un'entità servizio di Azure è un'identità creata per l'uso con applicazioni, servizi in hosting e strumenti automatici per l'accesso alle risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf19-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="dcf19-107">Questo accesso è limitato dai ruoli assegnati all'entità servizio e consente quindi di definire quali risorse siano accessibili e a quale livello.</span><span class="sxs-lookup"><span data-stu-id="dcf19-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="dcf19-108">Per motivi di sicurezza è sempre consigliabile usare le identità servizio per gli strumenti automatici, invece di consentire loro di accedere con un'identità utente.</span><span class="sxs-lookup"><span data-stu-id="dcf19-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="dcf19-109">Questo articolo illustra i passaggi per la creazione, l'acquisizione di informazioni correlate e il ripristino di un'entità servizio con Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dcf19-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="dcf19-110">Creare un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="dcf19-110">Create a service principal</span></span>

<span data-ttu-id="dcf19-111">Creare un'entità servizio con il cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="dcf19-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="dcf19-112">Quando si crea un'entità servizio, si sceglie il tipo di autenticazione per l'accesso che verrà usata dall'entità.</span><span class="sxs-lookup"><span data-stu-id="dcf19-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="dcf19-113">Se l'account in uso non è autorizzato a creare un'entità servizio, `New-AzADServicePrincipal` restituisce un messaggio di errore contenente "I privilegi non sono sufficienti per completare l'operazione".</span><span class="sxs-lookup"><span data-stu-id="dcf19-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="dcf19-114">Per creare un'entità servizio, contattare l'amministratore di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dcf19-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="dcf19-115">Sono disponibili due tipi di autenticazione per le entità servizio: autenticazione basata su password e autenticazione basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="dcf19-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="dcf19-116">Autenticazione basata su password</span><span class="sxs-lookup"><span data-stu-id="dcf19-116">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcf19-117">Il ruolo predefinito di un'entità servizio di autenticazione basata su password è **Collaboratore**.</span><span class="sxs-lookup"><span data-stu-id="dcf19-117">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="dcf19-118">Questo ruolo ha autorizzazioni complete per la lettura e la scrittura in un account di Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf19-118">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="dcf19-119">Per informazioni sulla gestione delle assegnazioni di ruolo, vedere [Gestire i ruoli delle entità servizio](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="dcf19-119">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="dcf19-120">Senza altri parametri di autenticazione, viene usata l'autenticazione basata su password e viene creata automaticamente una password casuale.</span><span class="sxs-lookup"><span data-stu-id="dcf19-120">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="dcf19-121">Se si intende implementare l'autenticazione basata su password, si consiglia questo metodo.</span><span class="sxs-lookup"><span data-stu-id="dcf19-121">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="dcf19-122">L'oggetto restituito contiene il membro `Secret`, ovvero un oggetto `SecureString` contenente la password generata.</span><span class="sxs-lookup"><span data-stu-id="dcf19-122">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="dcf19-123">Assicurarsi di conservare questo valore in un posto sicuro per eseguire l'autenticazione con l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="dcf19-123">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="dcf19-124">Il valore _non_ verrà visualizzato nell'output della console.</span><span class="sxs-lookup"><span data-stu-id="dcf19-124">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="dcf19-125">Se si perde la password, [reimpostare le credenziali dell'entità servizio](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="dcf19-125">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="dcf19-126">Il codice seguente consentirà di esportare il segreto:</span><span class="sxs-lookup"><span data-stu-id="dcf19-126">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="dcf19-127">Per le password definite dall'utente, l'argomento `-PasswordCredential` accetta oggetti `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="dcf19-127">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="dcf19-128">Questi oggetti devono avere valori validi di `StartDate` e `EndDate` e accettano `Password` in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="dcf19-128">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="dcf19-129">Quando si crea una password, assicurarsi di seguire le [regole e limitazioni per le password di Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="dcf19-129">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="dcf19-130">Non usare password vulnerabili o già usate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="dcf19-130">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="dcf19-131">L'oggetto restituito da `New-AzADServicePrincipal` contiene i membri `Id` e `DisplayName`, che possono essere entrambi usati per l'accesso con l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="dcf19-131">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcf19-132">L'accesso con un'entità servizio richiede l'ID del tenant in cui è stata creata.</span><span class="sxs-lookup"><span data-stu-id="dcf19-132">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="dcf19-133">Per ottenere il tenant attivo quando è stata creata l'entità servizio, eseguire il comando seguente _immediatamente dopo_ averla creata:</span><span class="sxs-lookup"><span data-stu-id="dcf19-133">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="dcf19-134">Autenticazione basata su certificati</span><span class="sxs-lookup"><span data-stu-id="dcf19-134">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcf19-135">Quando viene creata, a un'entità servizio di autenticazione basata su certificato non è assegnato alcun ruolo predefinito.</span><span class="sxs-lookup"><span data-stu-id="dcf19-135">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="dcf19-136">Per informazioni sulla gestione delle assegnazioni di ruolo, vedere [Gestire i ruoli delle entità servizio](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="dcf19-136">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="dcf19-137">Le entità servizio che usano l'autenticazione basata su certificato vengono create con il parametro `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="dcf19-137">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="dcf19-138">Questo parametro accetta una stringa ASCII con codifica Base64 del certificato pubblico,</span><span class="sxs-lookup"><span data-stu-id="dcf19-138">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="dcf19-139">rappresentato da un file PEM oppure da un file CRT o CER con codifica di testo.</span><span class="sxs-lookup"><span data-stu-id="dcf19-139">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="dcf19-140">Le codifiche binarie del certificato pubblico non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="dcf19-140">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="dcf19-141">Queste istruzioni presuppongono che sia già disponibile un certificato.</span><span class="sxs-lookup"><span data-stu-id="dcf19-141">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="dcf19-142">È anche possibile usare il parametro `-KeyCredential`, che accetta oggetti `PSADKeyCredential`.</span><span class="sxs-lookup"><span data-stu-id="dcf19-142">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="dcf19-143">Questi oggetti devono avere valori validi di `StartDate` e `EndDate`. Inoltre, il membro `CertValue` deve essere impostato su una stringa ASCII con codifica Base64 del certificato pubblico.</span><span class="sxs-lookup"><span data-stu-id="dcf19-143">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="dcf19-144">L'oggetto restituito da `New-AzADServicePrincipal` contiene i membri `Id` e `DisplayName`, che possono essere entrambi usati per l'accesso con l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="dcf19-144">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="dcf19-145">I client che accedono con l'entità servizio devono anche accedere alla chiave privata del certificato.</span><span class="sxs-lookup"><span data-stu-id="dcf19-145">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcf19-146">L'accesso con un'entità servizio richiede l'ID del tenant in cui è stata creata.</span><span class="sxs-lookup"><span data-stu-id="dcf19-146">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="dcf19-147">Per ottenere il tenant attivo quando è stata creata l'entità servizio, eseguire il comando seguente _immediatamente dopo_ averla creata:</span><span class="sxs-lookup"><span data-stu-id="dcf19-147">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="dcf19-148">Ottenere un'entità servizio esistente</span><span class="sxs-lookup"><span data-stu-id="dcf19-148">Get an existing service principal</span></span>

<span data-ttu-id="dcf19-149">L'elenco delle entità servizio per il tenant attivo può essere recuperato con [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="dcf19-149">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="dcf19-150">Per impostazione predefinita, questo comando restituisce _tutte_ le entità servizio in un tenant.</span><span class="sxs-lookup"><span data-stu-id="dcf19-150">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="dcf19-151">Per le organizzazioni di grandi dimensioni, la restituzione dei risultati potrebbe richiedere molto tempo.</span><span class="sxs-lookup"><span data-stu-id="dcf19-151">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="dcf19-152">In alternativa, è consigliabile usare gli argomenti di filtro facoltativi sul lato server:</span><span class="sxs-lookup"><span data-stu-id="dcf19-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="dcf19-153">`-DisplayNameBeginsWith` richiede entità di servizio che abbiano un _prefisso_ corrispondente al valore specificato.</span><span class="sxs-lookup"><span data-stu-id="dcf19-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="dcf19-154">Il nome visualizzato di un'entità servizio è il valore impostato con `-DisplayName` durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="dcf19-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="dcf19-155">`-DisplayName` richiede una _corrispondenza esatta_ del nome di un'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="dcf19-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="dcf19-156">Gestire i ruoli delle entità servizio</span><span class="sxs-lookup"><span data-stu-id="dcf19-156">Manage service principal roles</span></span>

<span data-ttu-id="dcf19-157">Azure PowerShell include i cmdlet seguenti per gestire le assegnazioni dei ruoli:</span><span class="sxs-lookup"><span data-stu-id="dcf19-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="dcf19-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dcf19-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="dcf19-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dcf19-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="dcf19-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dcf19-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="dcf19-161">Il ruolo predefinito di un'entità servizio di autenticazione basata su password è **Collaboratore**.</span><span class="sxs-lookup"><span data-stu-id="dcf19-161">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="dcf19-162">Questo ruolo ha autorizzazioni complete per la lettura e la scrittura in un account di Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf19-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="dcf19-163">Il ruolo **Lettore** è più restrittivo e offre l'accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="dcf19-163">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="dcf19-164">Per altre informazioni sul controllo degli accessi in base al ruolo e i ruoli, vedere [Controllo degli accessi in base al ruolo: ruoli predefiniti](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="dcf19-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="dcf19-165">Questo esempio aggiunge il ruolo **Lettore** e rimuove il ruolo **Collaboratore**:</span><span class="sxs-lookup"><span data-stu-id="dcf19-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="dcf19-166">I cmdlet per l'assegnazione dei ruoli non accettano l'ID oggetto entità servizio.</span><span class="sxs-lookup"><span data-stu-id="dcf19-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="dcf19-167">Accettano l'ID applicazione associato, generato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="dcf19-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="dcf19-168">Per ottenere l'ID applicazione per un'entità servizio, usare `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="dcf19-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="dcf19-169">Se l'account in uso non ha le autorizzazioni per assegnare un ruolo, viene visualizzato un messaggio di errore che segnala che l'account non è autorizzato a eseguire l'azione "Microsoft.Authorization/roleAssignments/write".</span><span class="sxs-lookup"><span data-stu-id="dcf19-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="dcf19-170">Per gestire i ruoli, contattare l'amministratore di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dcf19-170">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="dcf19-171">L'aggiunta di un ruolo _non_ limita le autorizzazioni assegnate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="dcf19-171">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="dcf19-172">Quando si limitano le autorizzazioni di un'entità servizio, il ruolo **Collaboratore** deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="dcf19-172">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="dcf19-173">È possibile verificare le modifiche visualizzando l'elenco dei ruoli assegnati:</span><span class="sxs-lookup"><span data-stu-id="dcf19-173">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="dcf19-174">Accedere con un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="dcf19-174">Sign in using a service principal</span></span>

<span data-ttu-id="dcf19-175">Testare le credenziali e le autorizzazioni della nuova entità servizio eseguendo l'accesso.</span><span class="sxs-lookup"><span data-stu-id="dcf19-175">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="dcf19-176">Per accedere con un'entità servizio, è necessario il valore di `applicationId` associato e il tenant in cui è stata creata.</span><span class="sxs-lookup"><span data-stu-id="dcf19-176">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="dcf19-177">Per accedere con un'entità servizio usando una password:</span><span class="sxs-lookup"><span data-stu-id="dcf19-177">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="dcf19-178">Per l'autenticazione basata su certificato, è necessario che Azure PowerShell sia in grado di recuperare informazioni da un archivio certificati locale in base a un'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="dcf19-178">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

<span data-ttu-id="dcf19-179">Per le istruzioni su come importare un certificato in un archivio certificati accessibile a PowerShell, vedere [Accedere con Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="dcf19-179">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="dcf19-180">Reimpostare le credenziali</span><span class="sxs-lookup"><span data-stu-id="dcf19-180">Reset credentials</span></span>

<span data-ttu-id="dcf19-181">Se si dimenticano le credenziali per un'entità servizio, usare [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) per aggiungere credenziali nuove con una password casuale.</span><span class="sxs-lookup"><span data-stu-id="dcf19-181">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="dcf19-182">Questo cmdlet non supporta le credenziali definite dall'utente per la reimpostazione della password.</span><span class="sxs-lookup"><span data-stu-id="dcf19-182">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcf19-183">Prima di assegnare nuove credenziali, è consigliabile rimuovere quelle esistenti per evitare che vengano usate per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="dcf19-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="dcf19-184">A questo scopo, usare il cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="dcf19-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="dcf19-185">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="dcf19-185">Troubleshooting</span></span>

<span data-ttu-id="dcf19-186">Se viene visualizzato l'errore _"New-AzADServicePrincipal: Esiste già un altro oggetto con lo stesso valore per la proprietà identifierUris"_ , verificare che non sia già presente un'entità servizio con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="dcf19-186">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_, verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="dcf19-187">Se l'entità servizio esistente non è più necessaria, è possibile rimuoverla usando l'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="dcf19-187">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="dcf19-188">Questo errore può verificarsi anche quando in precedenza è stata creata un'entità servizio per un'applicazione Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dcf19-188">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="dcf19-189">Se si rimuove l'entità servizio, l'applicazione rimane disponibile.</span><span class="sxs-lookup"><span data-stu-id="dcf19-189">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="dcf19-190">Questa applicazione impedisce di creare un'altra entità servizio con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="dcf19-190">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="dcf19-191">È possibile usare l'esempio seguente per verificare che non esista un'applicazione Azure Active Directory con lo stesso nome:</span><span class="sxs-lookup"><span data-stu-id="dcf19-191">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="dcf19-192">Se esiste un'applicazione con lo stesso nome ma non è più necessaria, è possibile rimuoverla usando l'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="dcf19-192">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="dcf19-193">In caso contrario, scegliere un nome alternativo per la nuova entità servizio da creare.</span><span class="sxs-lookup"><span data-stu-id="dcf19-193">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>
