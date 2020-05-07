---
title: Creare un'entità servizio di Azure con Azure PowerShell
description: Informazioni su come creare un'entità servizio per un'app o un servizio con Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure AD, AD, Controllo degli accessi in base al ruolo
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: dd2528cf91495361343ff562b7a602e7c115d13b
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534685"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="a9c19-104">Creare un'entità servizio di Azure con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a9c19-104">Create an Azure service principal with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="a9c19-105">Se si prevede di gestire un'app o un servizio con Azure PowerShell, è consigliabile eseguire tale app o servizio in un'entità servizio di Azure Active Directory (AAD), anziché con le proprie credenziali.</span><span class="sxs-lookup"><span data-stu-id="a9c19-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="a9c19-106">Questo argomento illustra come creare un'entità di sicurezza con Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a9c19-106">This topic steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="a9c19-107">È inoltre possibile creare un'entità servizio tramite il portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c19-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="a9c19-108">Per informazioni dettagliate, vedere [Usare il portale per creare un'applicazione Active Directory e un'entità servizio che accedono alle risorse](/azure/azure-resource-manager/resource-group-create-service-principal-portal).</span><span class="sxs-lookup"><span data-stu-id="a9c19-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="a9c19-109">Che cos'è un'"entità servizio"?</span><span class="sxs-lookup"><span data-stu-id="a9c19-109">What is a 'service principal'?</span></span>

<span data-ttu-id="a9c19-110">Un'entità servizio di Azure è un'identità di sicurezza usata da app, servizi e strumenti di automazione creati dall'utente per accedere a risorse di Azure specifiche.</span><span class="sxs-lookup"><span data-stu-id="a9c19-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="a9c19-111">Può essere considerata come una "identità utente" (nome utente e password o certificato) con un ruolo specifico e autorizzazioni attentamente controllate.</span><span class="sxs-lookup"><span data-stu-id="a9c19-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="a9c19-112">A differenza di un'identità utente generica, essa deve essere in grado di eseguire soltanto operazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="a9c19-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="a9c19-113">Se le viene concesso solo il livello minimo di autorizzazioni necessarie per eseguire le attività di gestione, un'entità servizio migliora la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a9c19-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="a9c19-114">Verificare il proprio livello di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="a9c19-114">Verify your own permission level</span></span>

<span data-ttu-id="a9c19-115">Innanzitutto, è necessario avere autorizzazioni sufficienti sia nell'istanza di Azure Active Directory che nella sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c19-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="a9c19-116">In particolare, è necessario poter creare un'app in Active Directory e assegnare un ruolo all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="a9c19-116">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span>

<span data-ttu-id="a9c19-117">Il modo più semplice per verificare se l'account dispone delle autorizzazioni appropriate è tramite il portale.</span><span class="sxs-lookup"><span data-stu-id="a9c19-117">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="a9c19-118">Vedere l'articolo su come [controllare le autorizzazioni necessarie nel portale](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="a9c19-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="a9c19-119">Creare un'entità servizio per l'app</span><span class="sxs-lookup"><span data-stu-id="a9c19-119">Create a service principal for your app</span></span>

<span data-ttu-id="a9c19-120">Dopo avere eseguito l'accesso all'account Azure, è possibile creare l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="a9c19-120">Once you are signed into your Azure account, you can create the service principal.</span></span> <span data-ttu-id="a9c19-121">È necessario disporre di uno dei modi seguenti per identificare l'app distribuita:</span><span class="sxs-lookup"><span data-stu-id="a9c19-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="a9c19-122">Nome univoco dell'app distribuita, ad esempio "MyDemoWebApp" negli esempi seguenti, oppure</span><span class="sxs-lookup"><span data-stu-id="a9c19-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="a9c19-123">ID dell'applicazione, GUID univoco associato all'app, al servizio o all'oggetto distribuito</span><span class="sxs-lookup"><span data-stu-id="a9c19-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="a9c19-124">Ottenere informazioni sull'applicazione</span><span class="sxs-lookup"><span data-stu-id="a9c19-124">Get information about your application</span></span>

<span data-ttu-id="a9c19-125">Per individuare le informazioni sull'applicazione si può usare il cmdlet `Get-AzureRmADApplication`.</span><span class="sxs-lookup"><span data-stu-id="a9c19-125">The `Get-AzureRmADApplication` cmdlet can be used to discover information about your application.</span></span>

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="a9c19-126">Creare un'entità servizio per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="a9c19-126">Create a service principal for your application</span></span>

<span data-ttu-id="a9c19-127">Per creare l'entità servizio si usa il cmdlet `New-AzureRmADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="a9c19-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="a9c19-128">Ottenere informazioni sull'entità servizio</span><span class="sxs-lookup"><span data-stu-id="a9c19-128">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="a9c19-129">Accedere con l'entità servizio</span><span class="sxs-lookup"><span data-stu-id="a9c19-129">Sign in using the service principal</span></span>

<span data-ttu-id="a9c19-130">È ora possibile effettuare l'accesso come nuova entità servizio per l'app usando l'*appId* e la *password* specificati.</span><span class="sxs-lookup"><span data-stu-id="a9c19-130">You can now sign in as the new service principal for your app using the *appId* and *password* you provided.</span></span> <span data-ttu-id="a9c19-131">È necessario fornire l'Id tenant per l'account.</span><span class="sxs-lookup"><span data-stu-id="a9c19-131">You need to supply the Tenant Id for your account.</span></span> <span data-ttu-id="a9c19-132">L'Id tenant viene visualizzato quando si accede ad Azure con le credenziali personali.</span><span class="sxs-lookup"><span data-stu-id="a9c19-132">Your Tenant Id is displayed when you sign into Azure with your personal credentials.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="a9c19-133">Eseguire questo comando da una nuova sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a9c19-133">Run this command from a new PowerShell session.</span></span> <span data-ttu-id="a9c19-134">Dopo aver eseguito correttamente l'accesso, verrà visualizzato un output simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="a9c19-134">After a successfully signing on you see output something like this:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="a9c19-135">Congratulazioni!</span><span class="sxs-lookup"><span data-stu-id="a9c19-135">Congratulations!</span></span> <span data-ttu-id="a9c19-136">È possibile usare queste credenziali per eseguire l'app.</span><span class="sxs-lookup"><span data-stu-id="a9c19-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="a9c19-137">Sarà poi necessario modificare le autorizzazioni dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="a9c19-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="a9c19-138">Gestione dei ruoli</span><span class="sxs-lookup"><span data-stu-id="a9c19-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="a9c19-139">Il controllo di accesso in base al ruolo di Azure (Role-Based Access Control - RBAC) è un modello per la definizione e gestione dei ruoli per le entità utente e servizio.</span><span class="sxs-lookup"><span data-stu-id="a9c19-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="a9c19-140">I ruoli dispongono di set di autorizzazioni associate a essi, che determinano le risorse che un'entità può leggere scrivere o gestire e a cui può accedere.</span><span class="sxs-lookup"><span data-stu-id="a9c19-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="a9c19-141">Per altre informazioni sui ruoli e sul controllo degli accessi in base al ruolo, vedere [Controllo degli accessi in base al ruoli: ruoli predefiniti](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="a9c19-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="a9c19-142">Azure PowerShell fornisce i cmdlet seguenti per gestire le assegnazioni dei ruoli:</span><span class="sxs-lookup"><span data-stu-id="a9c19-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="a9c19-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a9c19-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="a9c19-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a9c19-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="a9c19-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a9c19-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="a9c19-146">Il ruolo predefinito per un'entità servizio è quello **Collaboratore**.</span><span class="sxs-lookup"><span data-stu-id="a9c19-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="a9c19-147">Potrebbe non essere la scelta migliore in base allo scope delle interazioni dell'app con i servizi di Azure, date le ampie autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="a9c19-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="a9c19-148">Il ruolo **Lettore** è più restrittivo e può essere una buona scelta per le app di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a9c19-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="a9c19-149">È possibile visualizzare i dettagli delle autorizzazioni specifiche del ruolo o creare autorizzazioni personalizzate tramite il portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c19-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="a9c19-150">In questo esempio si aggiunge il ruolo**Lettore** all'esempio precedente e si elimina quello **Collaboratore**:</span><span class="sxs-lookup"><span data-stu-id="a9c19-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
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
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="a9c19-151">Per visualizzare i ruoli correnti assegnati:</span><span class="sxs-lookup"><span data-stu-id="a9c19-151">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
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

<span data-ttu-id="a9c19-152">Altri cmdlet di Azure PowerShell per la gestione dei ruoli:</span><span class="sxs-lookup"><span data-stu-id="a9c19-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="a9c19-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9c19-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="a9c19-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9c19-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="a9c19-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9c19-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="a9c19-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9c19-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="a9c19-157">Modificare le credenziali dell'entità di sicurezza</span><span class="sxs-lookup"><span data-stu-id="a9c19-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="a9c19-158">È buona norma verificare le autorizzazioni e aggiornare le password a intervalli regolari.</span><span class="sxs-lookup"><span data-stu-id="a9c19-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="a9c19-159">È anche consigliabile gestire e modificare le credenziali di sicurezza quando si modifica un'app.</span><span class="sxs-lookup"><span data-stu-id="a9c19-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="a9c19-160">Ad esempio, si può modificare la password dell'entità servizio creando una nuova password ed eliminando la precedente.</span><span class="sxs-lookup"><span data-stu-id="a9c19-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="a9c19-161">Aggiungere una nuova password per l'entità servizio</span><span class="sxs-lookup"><span data-stu-id="a9c19-161">Add a new password for the service principal</span></span>

```azurepowershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="a9c19-162">Ottenere un elenco di credenziali per l'entità servizio</span><span class="sxs-lookup"><span data-stu-id="a9c19-162">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="a9c19-163">Rimuovere la vecchia password dall'entità servizio</span><span class="sxs-lookup"><span data-stu-id="a9c19-163">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="a9c19-164">Verificare l'elenco di credenziali per l'entità servizio</span><span class="sxs-lookup"><span data-stu-id="a9c19-164">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
