---
title: Creare un'entità servizio di Azure con Azure PowerShell
description: Informazioni su come creare un'entità servizio per un'app o un servizio con Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure AD, AD, Controllo degli accessi in base al ruolo
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342059"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="66fef-104">Creare un'entità servizio di Azure con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="66fef-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="66fef-105">Se si prevede di gestire un'app o un servizio con Azure PowerShell, è consigliabile eseguire tale app o servizio in un'entità servizio di Azure Active Directory (AAD), anziché con le proprie credenziali.</span><span class="sxs-lookup"><span data-stu-id="66fef-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="66fef-106">Questo articolo illustra la creazione di un'entità di sicurezza con Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="66fef-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="66fef-107">Che cos'è un'entità servizio?</span><span class="sxs-lookup"><span data-stu-id="66fef-107">What is a service principal?</span></span>

<span data-ttu-id="66fef-108">Un'entità servizio di Azure è un'identità di sicurezza usata da app, servizi e strumenti di automazione creati dall'utente per accedere a risorse di Azure specifiche.</span><span class="sxs-lookup"><span data-stu-id="66fef-108">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="66fef-109">Alle entità servizio vengono assegnate autorizzazioni specifiche correlate alle relative attività, offrendo un controllo di sicurezza migliore.</span><span class="sxs-lookup"><span data-stu-id="66fef-109">Service principals are assigned specific permissions related to their tasks, giving you better security control.</span></span> <span data-ttu-id="66fef-110">È diverso da un'identità utente generica, che in genere è autorizzata ad apportare modifiche.</span><span class="sxs-lookup"><span data-stu-id="66fef-110">This is unlike a general user identity, which is usually authorized to make any changes.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="66fef-111">Verificare il proprio livello di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="66fef-111">Verify your own permission level</span></span>

<span data-ttu-id="66fef-112">Innanzitutto, è necessario avere autorizzazioni sufficienti sia nell'istanza di Azure Active Directory che nella sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="66fef-112">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="66fef-113">È necessario poter creare un'app in Active Directory e assegnare un ruolo all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="66fef-113">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="66fef-114">Il modo più semplice per verificare se l'account ha le autorizzazioni corrette è tramite il portale.</span><span class="sxs-lookup"><span data-stu-id="66fef-114">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="66fef-115">Vedere l'articolo su come [controllare le autorizzazioni necessarie nel portale](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="66fef-115">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="66fef-116">Creare un'entità servizio per l'app</span><span class="sxs-lookup"><span data-stu-id="66fef-116">Create a service principal for your app</span></span>

<span data-ttu-id="66fef-117">Dopo aver eseguito l'accesso all'account Azure, è possibile creare l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="66fef-117">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="66fef-118">È necessario disporre di uno dei modi seguenti per identificare l'app distribuita:</span><span class="sxs-lookup"><span data-stu-id="66fef-118">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="66fef-119">Nome univoco dell'app distribuita, ad esempio "MyDemoWebApp" negli esempi seguenti</span><span class="sxs-lookup"><span data-stu-id="66fef-119">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples</span></span>
* <span data-ttu-id="66fef-120">ID dell'applicazione, GUID univoco associato all'app, al servizio o all'oggetto distribuito</span><span class="sxs-lookup"><span data-stu-id="66fef-120">The Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="66fef-121">Ottenere informazioni sull'applicazione</span><span class="sxs-lookup"><span data-stu-id="66fef-121">Get information about your application</span></span>

<span data-ttu-id="66fef-122">Per ottenere informazioni sull'applicazione è possibile usare il cmdlet `Get-AzADApplication`.</span><span class="sxs-lookup"><span data-stu-id="66fef-122">The `Get-AzADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="66fef-123">Creare un'entità servizio per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="66fef-123">Create a service principal for your application</span></span>

<span data-ttu-id="66fef-124">Per creare l'entità servizio si usa il cmdlet `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="66fef-124">The `New-AzADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="66fef-125">Da qui è possibile sia usare direttamente la proprietà `$servicePrincipal.Secret` come argomento per `Connect-AzAccount` (vedere "Accedere con l'entità servizio"), sia convertire `SecureString` in una stringa di testo normale:</span><span class="sxs-lookup"><span data-stu-id="66fef-125">From here, you can either directly use the `$servicePrincipal.Secret` property as an argument to `Connect-AzAccount` (see "Sign in using the service principal"), or you can convert this `SecureString` to a plain text string:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="66fef-126">Accedere con l'entità servizio</span><span class="sxs-lookup"><span data-stu-id="66fef-126">Sign in using the service principal</span></span>

<span data-ttu-id="66fef-127">È ora possibile effettuare l'accesso come nuova entità servizio per l'app usando il valore `appId` fornito e il valore `password`</span><span class="sxs-lookup"><span data-stu-id="66fef-127">You can now sign in as the new service principal for your app using the `appId` you provided and `password` that was</span></span>  
<span data-ttu-id="66fef-128">generato.</span><span class="sxs-lookup"><span data-stu-id="66fef-128">generated.</span></span> <span data-ttu-id="66fef-129">È anche necessario l'ID tenant per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="66fef-129">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="66fef-130">L'ID tenant viene visualizzato quando si accede ad Azure con le credenziali personali.</span><span class="sxs-lookup"><span data-stu-id="66fef-130">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="66fef-131">Per accedere con un'entità servizio, usare i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="66fef-131">To sign in with a service principal, use the commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="66fef-132">Dopo che è stato completato l'accesso, verrà visualizzato un output simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="66fef-132">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="66fef-133">Congratulazioni!</span><span class="sxs-lookup"><span data-stu-id="66fef-133">Congratulations!</span></span> <span data-ttu-id="66fef-134">È possibile usare queste credenziali per eseguire l'app.</span><span class="sxs-lookup"><span data-stu-id="66fef-134">You can use these credentials to run your app.</span></span> <span data-ttu-id="66fef-135">Sarà poi necessario modificare le autorizzazioni dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="66fef-135">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="66fef-136">Gestione dei ruoli</span><span class="sxs-lookup"><span data-stu-id="66fef-136">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="66fef-137">Il controllo di accesso in base al ruolo di Azure (Role-Based Access Control - RBAC) è un modello per la definizione e gestione dei ruoli per le entità utente e servizio.</span><span class="sxs-lookup"><span data-stu-id="66fef-137">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="66fef-138">I ruoli dispongono di set di autorizzazioni associate a essi, che determinano le risorse che un'entità può leggere scrivere o gestire e a cui può accedere.</span><span class="sxs-lookup"><span data-stu-id="66fef-138">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="66fef-139">Per altre informazioni sui ruoli e sul controllo degli accessi in base al ruolo, vedere [Controllo degli accessi in base al ruolo: ruoli predefiniti](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="66fef-139">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="66fef-140">Azure PowerShell fornisce i cmdlet seguenti per gestire le assegnazioni dei ruoli:</span><span class="sxs-lookup"><span data-stu-id="66fef-140">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="66fef-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66fef-141">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="66fef-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66fef-142">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="66fef-143">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66fef-143">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="66fef-144">Il ruolo predefinito per un'entità servizio è quello **Collaboratore**.</span><span class="sxs-lookup"><span data-stu-id="66fef-144">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="66fef-145">Potrebbe non essere la scelta migliore in base allo scope delle interazioni dell'app con i servizi di Azure, date le ampie autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="66fef-145">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="66fef-146">Il ruolo **Lettore** è più restrittivo e può essere una buona scelta per le app di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="66fef-146">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="66fef-147">È possibile visualizzare i dettagli delle autorizzazioni specifiche del ruolo o creare autorizzazioni personalizzate tramite il portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="66fef-147">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="66fef-148">In questo esempio si aggiunge il ruolo**Lettore** all'esempio precedente e si elimina quello **Collaboratore**:</span><span class="sxs-lookup"><span data-stu-id="66fef-148">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="66fef-149">Per visualizzare i ruoli correnti assegnati:</span><span class="sxs-lookup"><span data-stu-id="66fef-149">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="66fef-150">Altri cmdlet di Azure PowerShell per la gestione dei ruoli:</span><span class="sxs-lookup"><span data-stu-id="66fef-150">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="66fef-151">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="66fef-151">Get-AzRoleDefinition</span></span>](/powershell/module/az.resources/Get-azRoleDefinition)
* [<span data-ttu-id="66fef-152">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="66fef-152">New-AzRoleDefinition</span></span>](/powershell/module/az.resources/New-azRoleDefinition)
* [<span data-ttu-id="66fef-153">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="66fef-153">Remove-AzRoleDefinition</span></span>](/powershell/module/az.resources/Remove-azRoleDefinition)
* [<span data-ttu-id="66fef-154">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="66fef-154">Set-AzRoleDefinition</span></span>](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="66fef-155">Modificare le credenziali dell'entità di sicurezza</span><span class="sxs-lookup"><span data-stu-id="66fef-155">Change the credentials of the security principal</span></span>

<span data-ttu-id="66fef-156">È buona norma verificare le autorizzazioni e aggiornare le password a intervalli regolari.</span><span class="sxs-lookup"><span data-stu-id="66fef-156">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="66fef-157">È anche consigliabile gestire e modificare le credenziali di sicurezza quando si modifica un'app.</span><span class="sxs-lookup"><span data-stu-id="66fef-157">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="66fef-158">Ad esempio, si può modificare la password dell'entità servizio creando una nuova password ed eliminando la precedente.</span><span class="sxs-lookup"><span data-stu-id="66fef-158">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="66fef-159">Aggiungere una nuova password per l'entità servizio</span><span class="sxs-lookup"><span data-stu-id="66fef-159">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="66fef-160">Ottenere un elenco di credenziali per l'entità servizio</span><span class="sxs-lookup"><span data-stu-id="66fef-160">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="66fef-161">Rimuovere la vecchia password dall'entità servizio</span><span class="sxs-lookup"><span data-stu-id="66fef-161">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="66fef-162">Verificare l'elenco di credenziali per l'entità servizio</span><span class="sxs-lookup"><span data-stu-id="66fef-162">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="66fef-163">Ottenere informazioni sull'entità servizio</span><span class="sxs-lookup"><span data-stu-id="66fef-163">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
