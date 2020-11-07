---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 87e8615e7862e8b3314c9dace4849621a8ed4c78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860257"
---
# <span data-ttu-id="7c9bc-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7c9bc-101">Connect-AzAccount</span></span>

## <span data-ttu-id="7c9bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c9bc-102">SYNOPSIS</span></span>
<span data-ttu-id="7c9bc-103">Connettersi a Azure con un account autenticato da usare con le richieste di cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="7c9bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c9bc-104">SYNTAX</span></span>

### <span data-ttu-id="7c9bc-105">UserWithSubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c9bc-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c9bc-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c9bc-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c9bc-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="7c9bc-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c9bc-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c9bc-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c9bc-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c9bc-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c9bc-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="7c9bc-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c9bc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c9bc-111">DESCRIPTION</span></span>
<span data-ttu-id="7c9bc-112">Il cmdlet Connect-AzAccount si connette a Azure con un account autenticato da usare con le richieste di cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-112">The Connect-AzAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="7c9bc-113">Puoi usare questo account autenticato solo con i cmdlet di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-113">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="7c9bc-114">Per aggiungere un account autenticato da usare con i cmdlet di gestione dei servizi, usare il cmdlet Add-AzAccount o Import-AzPublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-114">To add an authenticated account for use with Service Management cmdlets, use the Add-AzAccount or the Import-AzPublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="7c9bc-115">Se non viene trovato alcun contesto per l'utente corrente, questo comando compilerà l'elenco di contesto dell'utente con un contesto per ogni abbonamento (primo 25).</span><span class="sxs-lookup"><span data-stu-id="7c9bc-115">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="7c9bc-116">L'elenco dei contesti creati per l'utente può essere trovato eseguendo "Get-AzContext-ListAvailable".</span><span class="sxs-lookup"><span data-stu-id="7c9bc-116">The list of contexts created for the user can be found by running "Get-AzContext -ListAvailable".</span></span> <span data-ttu-id="7c9bc-117">Per ignorare questa popolazione di contesto, è possibile eseguire questo comando con il parametro di opzione "-SkipContextPopulation".</span><span class="sxs-lookup"><span data-stu-id="7c9bc-117">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="7c9bc-118">Dopo l'esecuzione di questo cmdlet, è possibile disconnettersi da un account di Azure usando Disconnect-AzAccount.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-118">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzAccount.</span></span>

## <span data-ttu-id="7c9bc-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c9bc-119">EXAMPLES</span></span>

### <span data-ttu-id="7c9bc-120">Esempio 1: usare un login interattivo per connettersi a un account di Azure</span><span class="sxs-lookup"><span data-stu-id="7c9bc-120">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="7c9bc-121">Questo comando consente di connettersi a un account di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-121">This command connects to an Azure account.</span></span>
<span data-ttu-id="7c9bc-122">Per eseguire i cmdlet di Azure Resource Manager con questo account, è necessario specificare le credenziali dell'account Microsoft o dell'ID organizzazione alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-122">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="7c9bc-123">Se per le credenziali è abilitata l'autenticazione a più fattori, è necessario eseguire l'accesso usando l'opzione interattiva o usare l'autenticazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="7c9bc-124">Esempio 2: (solo Windows PowerShell 5,1) connettersi a un account di Azure utilizzando le credenziali di ID organizzazione</span><span class="sxs-lookup"><span data-stu-id="7c9bc-124">Example 2: (Windows PowerShell 5.1 only) Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="7c9bc-125">Questo scenario funziona solo in Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="7c9bc-126">Il primo comando richiederà le credenziali utente (nome utente e password) e li archivierà nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-126">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="7c9bc-127">Il secondo comando si connette a un account di Azure usando le credenziali archiviate in $Credential.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-127">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="7c9bc-128">Questo account esegue l'autenticazione con Azure Resource Manager usando le credenziali dell'ID organizzazione.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-128">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="7c9bc-129">Non è possibile usare l'autenticazione a più fattori o le credenziali dell'account Microsoft per eseguire i cmdlet di Azure Resource Manager con questo account.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-129">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="7c9bc-130">Esempio 3: connettersi a un account principale di Azure Service</span><span class="sxs-lookup"><span data-stu-id="7c9bc-130">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="7c9bc-131">Il primo comando ottiene le credenziali dell'entità servizio (ID applicazione e segreto principale del servizio), quindi le archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-131">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="7c9bc-132">Il secondo comando consente di connettersi a Azure usando le credenziali dell'entità servizio archiviate in $Credential per il tenant specificato.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-132">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="7c9bc-133">Il parametro ServicePrincipal switch indica che l'account viene autenticato come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-133">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="7c9bc-134">Esempio 4: usare un account di accesso interattivo per connettersi a un account per un tenant e un abbonamento specifici</span><span class="sxs-lookup"><span data-stu-id="7c9bc-134">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="7c9bc-135">Questo comando consente di connettersi a un account di Azure e configurare AzureRM PowerShell per eseguire i cmdlet per il tenant e la sottoscrizione specificati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-135">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="7c9bc-136">Esempio 5: aggiungere un account con l'accesso all'identità del servizio gestito</span><span class="sxs-lookup"><span data-stu-id="7c9bc-136">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="7c9bc-137">Questo comando consente di connettersi usando l'identità del servizio gestito dell'ambiente host, ad esempio se eseguito su un VirtualMachine con un'identità del servizio gestito assegnata, in modo da consentire al codice di accedere usando l'identità assegnata.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-137">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="7c9bc-138">Esempio 6: aggiungere un account con l'accesso alle identità del servizio gestito e ClientID</span><span class="sxs-lookup"><span data-stu-id="7c9bc-138">Example 6: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="7c9bc-139">Questo comando consente di connettersi usando l'identità del servizio gestito di "myUserAssignedIdentity" aggiungendo l'identità assegnata all'utente alla macchina virtuale, quindi connettendosi usando il ClientID dell'identità assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-139">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the ClientId of the User Assigned Identity.</span></span>
<span data-ttu-id="7c9bc-140">Altre informazioni sulla configurazione delle identità gestite possono essere trovate qui: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="7c9bc-140">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="7c9bc-141">Esempio 7: aggiungere un account con l'accesso alle identità del servizio gestito e ClientID</span><span class="sxs-lookup"><span data-stu-id="7c9bc-141">Example 7: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="7c9bc-142">Questo comando consente di connettersi usando l'identità del servizio gestito di "myUserAssignedIdentity" aggiungendo l'identità assegnata all'utente alla macchina virtuale, quindi connettendosi con l'ID dell'identità assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-142">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the Id of the User Assigned Identity.</span></span>
<span data-ttu-id="7c9bc-143">Altre informazioni sulla configurazione delle identità gestite possono essere trovate qui: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="7c9bc-143">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="7c9bc-144">Esempio 8: aggiungere un account con i certificati</span><span class="sxs-lookup"><span data-stu-id="7c9bc-144">Example 8: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="7c9bc-145">Questo comando consente di connettersi a un account di Azure usando l'autenticazione dell'entità servizio basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-145">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="7c9bc-146">L'entità di servizio utilizzata per l'autenticazione deve essere stata creata con il certificato indicato.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-146">The service principal used for authentication should have been created with the given certificate.</span></span>

### <span data-ttu-id="7c9bc-147">Esempio 9: aggiungere un account usando l'autenticazione di AccessToken</span><span class="sxs-lookup"><span data-stu-id="7c9bc-147">Example 9: Add an account using AccessToken authentication</span></span>
```powershell
PS C:\> $url = "https://login.windows.net/<TenantId>/oauth2/token"
PS C:\> $body = "grant_type=refresh_token&refresh_token=<refreshtoken>" # Refresh token obtained from ~/.azure/TokenCache.dat
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body
PS C:\> $AccessToken = $response.access_token
PS C:\> $body1 = $body + "&resource=https%3A%2F%2Fvault.azure.net"
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body1
PS C:\> $body2 = $body + "&resource=https%3A%2F%2Fgraph.windows.net"
PS C:\> $GraphAccessToken = $response.access_token
PS C:\> Connect-AzAccount -AccountId "azureuser@contoso.com" -AccessToken $AccessToken -KeyVaultAccessToken $KeyVaultAccessToken -GraphAccessToken $GraphAccessToken -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="7c9bc-148">Questo comando consente di connettersi a un account di Azure specificato in "AccountId" con AccessToken e KeyVaultAccessToken forniti.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-148">This command connects to an Azure account specified in "AccountId" using the AccessToken and KeyVaultAccessToken provided.</span></span>

## <span data-ttu-id="7c9bc-149">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c9bc-149">PARAMETERS</span></span>

### <span data-ttu-id="7c9bc-150">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="7c9bc-150">-AccessToken</span></span>
<span data-ttu-id="7c9bc-151">Specifica un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-151">Specifies an access token.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-152">-AccountId</span><span class="sxs-lookup"><span data-stu-id="7c9bc-152">-AccountId</span></span>
<span data-ttu-id="7c9bc-153">ID account per il token di accesso nel set di parametri AccessToken.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-153">Account Id for access token in AccessToken parameter set.</span></span> <span data-ttu-id="7c9bc-154">ID account per il servizio gestito nel set di parametri ManagedService.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-154">Account Id for managed service in ManagedService parameter set.</span></span> <span data-ttu-id="7c9bc-155">Può essere un ID di risorsa del servizio gestito o l'ID client associato. Per usare l'identità SystemAssigned, lascia vuoto questo campo.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-155">Can be a managed service resource Id, or the associated client id. To use the SystemAssigned identity, leave this field blank.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-156">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7c9bc-156">-ApplicationId</span></span>
<span data-ttu-id="7c9bc-157">SPN</span><span class="sxs-lookup"><span data-stu-id="7c9bc-157">SPN</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-158">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="7c9bc-158">-CertificateThumbprint</span></span>
<span data-ttu-id="7c9bc-159">Hash del certificato (identificazione personale)</span><span class="sxs-lookup"><span data-stu-id="7c9bc-159">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-160">-ContextName</span><span class="sxs-lookup"><span data-stu-id="7c9bc-160">-ContextName</span></span>
<span data-ttu-id="7c9bc-161">Nome del contesto predefinito da questo account di accesso.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-161">Name of the default context from this login.</span></span>  <span data-ttu-id="7c9bc-162">Dopo l'accesso, sarà possibile selezionare questo contesto con questo nome.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-162">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="7c9bc-163">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="7c9bc-163">-Credential</span></span>
<span data-ttu-id="7c9bc-164">Specifica un oggetto PSCredential.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-164">Specifies a PSCredential object.</span></span>
<span data-ttu-id="7c9bc-165">Per altre informazioni sull'oggetto PSCredential, digitare Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-165">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="7c9bc-166">L'oggetto PSCredential fornisce l'ID utente e la password per le credenziali di ID organizzazione oppure l'ID applicazione e il segreto per le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-166">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c9bc-167">-DefaultProfile</span></span>
<span data-ttu-id="7c9bc-168">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c9bc-169">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="7c9bc-169">-Environment</span></span>
<span data-ttu-id="7c9bc-170">Ambiente che contiene l'account per l'accesso</span><span class="sxs-lookup"><span data-stu-id="7c9bc-170">Environment containing the account to log into</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-171">-Force</span><span class="sxs-lookup"><span data-stu-id="7c9bc-171">-Force</span></span>
<span data-ttu-id="7c9bc-172">Sovrascrivere il contesto esistente con lo stesso nome, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-172">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="7c9bc-173">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="7c9bc-173">-GraphAccessToken</span></span>
<span data-ttu-id="7c9bc-174">AccessToken per il servizio grafico</span><span class="sxs-lookup"><span data-stu-id="7c9bc-174">AccessToken for Graph Service</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-175">-Identità</span><span class="sxs-lookup"><span data-stu-id="7c9bc-175">-Identity</span></span>
<span data-ttu-id="7c9bc-176">Accedere usando l'identità del servizio gestito nell'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-176">Login using managed service identity in the current environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-177">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="7c9bc-177">-KeyVaultAccessToken</span></span>
<span data-ttu-id="7c9bc-178">AccessToken per il servizio con il Vault</span><span class="sxs-lookup"><span data-stu-id="7c9bc-178">AccessToken for KeyVault Service</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-179">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="7c9bc-179">-ManagedServiceHostName</span></span>
<span data-ttu-id="7c9bc-180">Nome host per l'accesso al servizio gestito</span><span class="sxs-lookup"><span data-stu-id="7c9bc-180">Host name for managed service login</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-181">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="7c9bc-181">-ManagedServicePort</span></span>
<span data-ttu-id="7c9bc-182">Numero di porta per l'accesso al servizio gestito</span><span class="sxs-lookup"><span data-stu-id="7c9bc-182">Port number for managed service login</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-183">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="7c9bc-183">-ManagedServiceSecret</span></span>
<span data-ttu-id="7c9bc-184">Segreto, usato per alcuni tipi di accesso al servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-184">Secret, used for some kinds of managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-185">-Ambito</span><span class="sxs-lookup"><span data-stu-id="7c9bc-185">-Scope</span></span>
<span data-ttu-id="7c9bc-186">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-186">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-187">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7c9bc-187">-ServicePrincipal</span></span>
<span data-ttu-id="7c9bc-188">Indica che l'account viene autenticato fornendo le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-188">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-189">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="7c9bc-189">-SkipContextPopulation</span></span>
<span data-ttu-id="7c9bc-190">Ignora la popolazione del contesto se non vengono trovati contesti.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-190">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="7c9bc-191">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="7c9bc-191">-SkipValidation</span></span>
<span data-ttu-id="7c9bc-192">Ignorare la convalida per il token di accesso</span><span class="sxs-lookup"><span data-stu-id="7c9bc-192">Skip validation for access token</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-193">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="7c9bc-193">-Subscription</span></span>
<span data-ttu-id="7c9bc-194">Nome dell'abbonamento o ID</span><span class="sxs-lookup"><span data-stu-id="7c9bc-194">Subscription Name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-195">-Tenant</span><span class="sxs-lookup"><span data-stu-id="7c9bc-195">-Tenant</span></span>
<span data-ttu-id="7c9bc-196">Nome del tenant o ID facoltativo</span><span class="sxs-lookup"><span data-stu-id="7c9bc-196">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-197">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="7c9bc-197">-UseDeviceAuthentication</span></span>
<span data-ttu-id="7c9bc-198">Usare l'autenticazione del codice del dispositivo invece di un controllo browser</span><span class="sxs-lookup"><span data-stu-id="7c9bc-198">Use device code authentication instead of a browser control</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-199">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c9bc-199">-Confirm</span></span>
<span data-ttu-id="7c9bc-200">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-200">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c9bc-201">-WhatIf</span></span>
<span data-ttu-id="7c9bc-202">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c9bc-203">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-203">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9bc-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c9bc-204">CommonParameters</span></span>
<span data-ttu-id="7c9bc-205">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c9bc-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c9bc-206">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c9bc-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c9bc-207">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c9bc-207">INPUTS</span></span>

### <span data-ttu-id="7c9bc-208">System. String</span><span class="sxs-lookup"><span data-stu-id="7c9bc-208">System.String</span></span>

## <span data-ttu-id="7c9bc-209">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c9bc-209">OUTPUTS</span></span>

### <span data-ttu-id="7c9bc-210">Microsoft. Azure. Commands. profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="7c9bc-210">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="7c9bc-211">Note</span><span class="sxs-lookup"><span data-stu-id="7c9bc-211">NOTES</span></span>

## <span data-ttu-id="7c9bc-212">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c9bc-212">RELATED LINKS</span></span>
