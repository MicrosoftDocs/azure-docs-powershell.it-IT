---
title: Usare le entità servizio di Azure con Azure PowerShell
description: Informazioni su come creare e usare entità servizio con Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: 4c47d2bac2c63f13ac0ebbccda3e2eed12cd658f
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "81740015"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="8f152-103">Creare un'entità servizio di Azure con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8f152-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="8f152-104">Gli strumenti automatici che usano i servizi di Azure devono sempre avere autorizzazioni limitate.</span><span class="sxs-lookup"><span data-stu-id="8f152-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="8f152-105">Invece di consentire alle applicazioni l'accesso come utenti con privilegi completi, Azure offre le identità servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="8f152-106">Un'entità servizio di Azure è un'identità creata per l'uso con applicazioni, servizi in hosting e strumenti automatici per l'accesso alle risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="8f152-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="8f152-107">Questo accesso è limitato dai ruoli assegnati all'entità servizio e consente quindi di definire quali risorse siano accessibili e a quale livello.</span><span class="sxs-lookup"><span data-stu-id="8f152-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="8f152-108">Per motivi di sicurezza è sempre consigliabile usare le identità servizio per gli strumenti automatici, invece di consentire loro di accedere con un'identità utente.</span><span class="sxs-lookup"><span data-stu-id="8f152-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="8f152-109">Questo articolo illustra i passaggi per la creazione, l'acquisizione di informazioni correlate e il ripristino di un'entità servizio con Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8f152-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="8f152-110">Creare un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="8f152-110">Create a service principal</span></span>

<span data-ttu-id="8f152-111">Creare un'entità servizio con il cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="8f152-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="8f152-112">Quando si crea un'entità servizio, si sceglie il tipo di autenticazione per l'accesso che verrà usata dall'entità.</span><span class="sxs-lookup"><span data-stu-id="8f152-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="8f152-113">Se l'account in uso non è autorizzato a creare un'entità servizio, `New-AzADServicePrincipal` restituirà un messaggio di errore contenente "I privilegi non sono sufficienti per completare l'operazione".</span><span class="sxs-lookup"><span data-stu-id="8f152-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="8f152-114">Per creare un'entità servizio, contattare l'amministratore di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f152-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="8f152-115">Sono disponibili due tipi di autenticazione per le entità servizio: autenticazione basata su password e autenticazione basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="8f152-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="8f152-116">Autenticazione basata su password</span><span class="sxs-lookup"><span data-stu-id="8f152-116">Password-based authentication</span></span>

<span data-ttu-id="8f152-117">Senza altri parametri di autenticazione, viene usata l'autenticazione basata su password e viene creata automaticamente una password casuale.</span><span class="sxs-lookup"><span data-stu-id="8f152-117">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="8f152-118">Se si intende implementare l'autenticazione basata su password, si consiglia questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8f152-118">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="8f152-119">L'oggetto restituito contiene il membro `Secret`, ovvero un oggetto `SecureString` contenente la password generata.</span><span class="sxs-lookup"><span data-stu-id="8f152-119">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="8f152-120">Assicurarsi di conservare questo valore in un posto sicuro per eseguire l'autenticazione con l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-120">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="8f152-121">Il valore __non__ verrà visualizzato nell'output della console.</span><span class="sxs-lookup"><span data-stu-id="8f152-121">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="8f152-122">Se si perde la password, [reimpostare le credenziali dell'entità servizio](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="8f152-122">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="8f152-123">Il codice seguente consentirà di esportare il segreto:</span><span class="sxs-lookup"><span data-stu-id="8f152-123">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="8f152-124">Per le password definite dall'utente, l'argomento `-PasswordCredential` accetta oggetti `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="8f152-124">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="8f152-125">Questi oggetti devono avere valori validi di `StartDate` e `EndDate` e accettano `Password` in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="8f152-125">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="8f152-126">Quando si crea una password, assicurarsi di seguire le [regole e limitazioni per le password di Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="8f152-126">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="8f152-127">Non usare password vulnerabili o già usate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="8f152-127">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="8f152-128">L'oggetto restituito da `New-AzADServicePrincipal` contiene i membri `Id` e `DisplayName`, che possono essere entrambi usati per l'accesso con l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-128">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="8f152-129">L'accesso con un'entità servizio richiede l'ID del tenant in cui è stata creata.</span><span class="sxs-lookup"><span data-stu-id="8f152-129">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="8f152-130">Per ottenere il tenant attivo quando è stata creata l'entità servizio, eseguire il comando seguente __immediatamente dopo__ averla creata:</span><span class="sxs-lookup"><span data-stu-id="8f152-130">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="8f152-131">Autenticazione basata su certificati</span><span class="sxs-lookup"><span data-stu-id="8f152-131">Certificate-based authentication</span></span>

<span data-ttu-id="8f152-132">Le entità servizio che usano l'autenticazione basata su certificato vengono create con il parametro `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="8f152-132">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="8f152-133">Questo parametro accetta una stringa ASCII con codifica Base64 del certificato pubblico,</span><span class="sxs-lookup"><span data-stu-id="8f152-133">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="8f152-134">rappresentato da un file PEM oppure da un file CRT o CER con codifica di testo.</span><span class="sxs-lookup"><span data-stu-id="8f152-134">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="8f152-135">Le codifiche binarie del certificato pubblico non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="8f152-135">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="8f152-136">Queste istruzioni presuppongono che sia già disponibile un certificato.</span><span class="sxs-lookup"><span data-stu-id="8f152-136">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="8f152-137">È anche possibile usare il parametro `-KeyCredential`, che accetta oggetti `PSADKeyCredential`.</span><span class="sxs-lookup"><span data-stu-id="8f152-137">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="8f152-138">Questi oggetti devono avere valori validi di `StartDate` e `EndDate`. Inoltre, il membro `CertValue` deve essere impostato su una stringa ASCII con codifica Base64 del certificato pubblico.</span><span class="sxs-lookup"><span data-stu-id="8f152-138">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="8f152-139">L'oggetto restituito da `New-AzADServicePrincipal` contiene i membri `Id` e `DisplayName`, che possono essere entrambi usati per l'accesso con l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-139">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="8f152-140">I client che accedono con l'entità servizio devono anche accedere alla chiave privata del certificato.</span><span class="sxs-lookup"><span data-stu-id="8f152-140">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="8f152-141">L'accesso con un'entità servizio richiede l'ID del tenant in cui è stata creata.</span><span class="sxs-lookup"><span data-stu-id="8f152-141">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="8f152-142">Per ottenere il tenant attivo quando è stata creata l'entità servizio, eseguire il comando seguente __immediatamente dopo__ averla creata:</span><span class="sxs-lookup"><span data-stu-id="8f152-142">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="8f152-143">Ottenere un'entità servizio esistente</span><span class="sxs-lookup"><span data-stu-id="8f152-143">Get an existing service principal</span></span>

<span data-ttu-id="8f152-144">L'elenco delle entità servizio per il tenant attualmente attivo può essere recuperato con [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="8f152-144">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="8f152-145">Per impostazione predefinita, questo comando restituisce __tutte__ le entità servizio di un tenant, quindi per le organizzazioni più grandi la restituzione di risultati può richiedere tempi lunghi.</span><span class="sxs-lookup"><span data-stu-id="8f152-145">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="8f152-146">In alternativa, è consigliabile usare gli argomenti di filtro facoltativi sul lato server:</span><span class="sxs-lookup"><span data-stu-id="8f152-146">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="8f152-147">`-DisplayNameBeginsWith` richiede entità di servizio che abbiano un _prefisso_ corrispondente al valore specificato.</span><span class="sxs-lookup"><span data-stu-id="8f152-147">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="8f152-148">Il nome visualizzato di un'entità servizio è il valore impostato con `-DisplayName` durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="8f152-148">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="8f152-149">`-DisplayName` richiede una _corrispondenza esatta_ del nome di un'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-149">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="8f152-150">Gestire i ruoli delle entità servizio</span><span class="sxs-lookup"><span data-stu-id="8f152-150">Manage service principal roles</span></span>

<span data-ttu-id="8f152-151">Azure PowerShell include i cmdlet seguenti per gestire le assegnazioni dei ruoli:</span><span class="sxs-lookup"><span data-stu-id="8f152-151">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="8f152-152">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8f152-152">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="8f152-153">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8f152-153">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="8f152-154">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8f152-154">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="8f152-155">Il ruolo predefinito per un'entità servizio è quello **Collaboratore**.</span><span class="sxs-lookup"><span data-stu-id="8f152-155">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="8f152-156">Questo ruolo ha autorizzazioni complete per la lettura e la scrittura in un account di Azure.</span><span class="sxs-lookup"><span data-stu-id="8f152-156">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="8f152-157">Il ruolo **Lettore** è più restrittivo e offre l'accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="8f152-157">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="8f152-158">Per altre informazioni sul controllo degli accessi in base al ruolo e i ruoli, vedere [Controllo degli accessi in base al ruolo: ruoli predefiniti](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="8f152-158">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="8f152-159">Questo esempio aggiunge il ruolo **Lettore** e rimuove il ruolo **Collaboratore**:</span><span class="sxs-lookup"><span data-stu-id="8f152-159">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="8f152-160">I cmdlet per l'assegnazione dei ruoli non accettano l'ID oggetto entità servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-160">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="8f152-161">Accettano l'ID applicazione associato, generato al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="8f152-161">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="8f152-162">Per ottenere l'ID applicazione per un'entità servizio, usare `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="8f152-162">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="8f152-163">Se l'account non ha le autorizzazioni per assegnare un ruolo, verrà visualizzato un messaggio di errore che segnala che l'account non è autorizzato a eseguire l'azione 'Microsoft.Authorization/roleAssignments/write'. Per gestire i ruoli, contattare l'amministratore di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f152-163">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="8f152-164">L'aggiunta di un ruolo _non_ limita le autorizzazioni assegnate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="8f152-164">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="8f152-165">Quando si limitano le autorizzazioni di un'entità servizio, il ruolo __Collaboratore__ deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="8f152-165">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="8f152-166">È possibile verificare le modifiche visualizzando l'elenco dei ruoli assegnati:</span><span class="sxs-lookup"><span data-stu-id="8f152-166">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="8f152-167">Accedere con un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="8f152-167">Sign in using a service principal</span></span>

<span data-ttu-id="8f152-168">Testare le credenziali e le autorizzazioni della nuova entità servizio eseguendo l'accesso.</span><span class="sxs-lookup"><span data-stu-id="8f152-168">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="8f152-169">Per accedere con un'entità servizio, è necessario il valore di `applicationId` associato e il tenant in cui è stata creata.</span><span class="sxs-lookup"><span data-stu-id="8f152-169">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="8f152-170">Per accedere con un'entità servizio usando una password:</span><span class="sxs-lookup"><span data-stu-id="8f152-170">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="8f152-171">Per l'autenticazione basata su certificato, è necessario che Azure PowerShell sia in grado di recuperare informazioni da un archivio certificati locale in base a un'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="8f152-171">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="8f152-172">Per le istruzioni su come importare un certificato in un archivio certificati accessibile a PowerShell, vedere [Accedere con Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="8f152-172">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="8f152-173">Reimpostare le credenziali</span><span class="sxs-lookup"><span data-stu-id="8f152-173">Reset credentials</span></span>

<span data-ttu-id="8f152-174">Se si dimenticano le credenziali per un'entità di servizio, usare [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) per aggiungerne una nuova.</span><span class="sxs-lookup"><span data-stu-id="8f152-174">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="8f152-175">Questo cmdlet accetta gli stessi argomenti e tipi di credenziali di `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="8f152-175">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="8f152-176">Senza argomenti di credenziali, viene creato un nuovo oggetto `PasswordCredential` con una password casuale.</span><span class="sxs-lookup"><span data-stu-id="8f152-176">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f152-177">Prima di assegnare nuove credenziali, è consigliabile rimuovere quelle esistenti per evitare che vengano usate per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="8f152-177">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="8f152-178">A questo scopo, usare il cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="8f152-178">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
