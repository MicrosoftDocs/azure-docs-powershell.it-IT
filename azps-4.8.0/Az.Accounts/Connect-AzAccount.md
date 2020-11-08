---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 073a70077eabbdf20d72874b22c11b7f0dae2844
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189895"
---
# <span data-ttu-id="7ec66-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7ec66-101">Connect-AzAccount</span></span>

## <span data-ttu-id="7ec66-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ec66-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec66-103">Connettersi a Azure con un account autenticato da usare con i cmdlet dei moduli di PowerShell di AZ.</span><span class="sxs-lookup"><span data-stu-id="7ec66-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="7ec66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ec66-104">SYNTAX</span></span>

### <span data-ttu-id="7ec66-105">UserWithSubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7ec66-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ec66-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ec66-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ec66-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="7ec66-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ec66-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ec66-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ec66-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ec66-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ec66-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="7ec66-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ec66-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ec66-111">DESCRIPTION</span></span>

<span data-ttu-id="7ec66-112">Il `Connect-AzAccount` cmdlet si connette a Azure con un account autenticato da usare con i cmdlet dei moduli di PowerShell di AZ.</span><span class="sxs-lookup"><span data-stu-id="7ec66-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="7ec66-113">Puoi usare questo account autenticato solo con le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec66-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="7ec66-114">Per aggiungere un account autenticato da usare con la gestione dei servizi, usare il `Add-AzureAccount` cmdlet dal modulo di PowerShell di Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec66-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="7ec66-115">Se non viene trovato alcun contesto per l'utente corrente, l'elenco di contesto dell'utente viene popolato con un contesto per ognuno dei primi 25 abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="7ec66-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="7ec66-116">L'elenco dei contesti creati per l'utente può essere trovato eseguendo `Get-AzContext -ListAvailable` .</span><span class="sxs-lookup"><span data-stu-id="7ec66-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="7ec66-117">Per ignorare questa popolazione di contesto, specifica il parametro **SkipContextPopulation** switch.</span><span class="sxs-lookup"><span data-stu-id="7ec66-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="7ec66-118">Dopo l'esecuzione di questo cmdlet, è possibile disconnettersi da un account di Azure usando `Disconnect-AzAccount` .</span><span class="sxs-lookup"><span data-stu-id="7ec66-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="7ec66-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ec66-119">EXAMPLES</span></span>

### <span data-ttu-id="7ec66-120">Esempio 1: connettersi a un account di Azure</span><span class="sxs-lookup"><span data-stu-id="7ec66-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="7ec66-121">Questo esempio si connette a un account di Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec66-121">This example connects to an Azure account.</span></span> <span data-ttu-id="7ec66-122">È necessario specificare un account Microsoft o credenziali di ID organizzazione.</span><span class="sxs-lookup"><span data-stu-id="7ec66-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="7ec66-123">Se per le credenziali è abilitata l'autenticazione a più fattori, è necessario eseguire l'accesso usando l'opzione interattiva o usare l'autenticazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7ec66-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7ec66-124">Esempio 2: (solo Windows PowerShell 5,1) connettersi ad Azure usando le credenziali dell'ID organizzazione</span><span class="sxs-lookup"><span data-stu-id="7ec66-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="7ec66-125">Questo scenario funziona solo in Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="7ec66-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="7ec66-126">Il primo comando richiede le credenziali utente e le archivia nella `$Credential` variabile.</span><span class="sxs-lookup"><span data-stu-id="7ec66-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="7ec66-127">Il secondo comando si connette a un account di Azure usando le credenziali archiviate in `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="7ec66-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="7ec66-128">Questo account esegue l'autenticazione con Azure utilizzando le credenziali di ID organizzazione.</span><span class="sxs-lookup"><span data-stu-id="7ec66-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7ec66-129">Esempio 3: connettersi a Azure usando un account Principal del servizio</span><span class="sxs-lookup"><span data-stu-id="7ec66-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="7ec66-130">Il primo comando richiede le credenziali dell'entità servizio e le archivia nella `$Credential` variabile.</span><span class="sxs-lookup"><span data-stu-id="7ec66-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="7ec66-131">Immettere l'ID applicazione per il nome utente e il segreto principale del servizio come password quando richiesto.</span><span class="sxs-lookup"><span data-stu-id="7ec66-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="7ec66-132">Il secondo comando connette il tenant Azure specificato usando le credenziali dell'entità servizio archiviate nella `$Credential` variabile.</span><span class="sxs-lookup"><span data-stu-id="7ec66-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="7ec66-133">Il parametro **ServicePrincipal** switch indica che l'account viene autenticato come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7ec66-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7ec66-134">Esempio 4: usare un account di accesso interattivo per connettersi a un tenant e un abbonamento specifici</span><span class="sxs-lookup"><span data-stu-id="7ec66-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="7ec66-135">Questo esempio si connette a un account di Azure con il tenant e l'abbonamento specificati.</span><span class="sxs-lookup"><span data-stu-id="7ec66-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7ec66-136">Esempio 5: connettersi tramite un'identità di servizio gestito</span><span class="sxs-lookup"><span data-stu-id="7ec66-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="7ec66-137">Questo esempio si connette usando l'identità del servizio gestito (MSI) dell'ambiente host.</span><span class="sxs-lookup"><span data-stu-id="7ec66-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="7ec66-138">Ad esempio, è possibile accedere a Azure da una macchina virtuale con un MSI assegnato.</span><span class="sxs-lookup"><span data-stu-id="7ec66-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7ec66-139">Esempio 6: connettersi con l'account di accesso e ClientID dell'identità del servizio gestito</span><span class="sxs-lookup"><span data-stu-id="7ec66-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="7ec66-140">Questo esempio si connette usando l'identità del servizio gestito di **myUserAssignedIdentity**.</span><span class="sxs-lookup"><span data-stu-id="7ec66-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="7ec66-141">Aggiunge l'identità assegnata all'utente alla macchina virtuale, quindi si connette usando il ClientID dell'identità assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7ec66-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="7ec66-142">Per altre informazioni, vedere [configurare le identità gestite per le risorse Azure in una VM di Azure](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span><span class="sxs-lookup"><span data-stu-id="7ec66-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="7ec66-143">Esempio 7: connettersi con i certificati</span><span class="sxs-lookup"><span data-stu-id="7ec66-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="7ec66-144">Questo esempio si connette a un account di Azure usando l'autenticazione dell'entità servizio basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="7ec66-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="7ec66-145">L'entità di servizio utilizzata per l'autenticazione deve essere creata con il certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="7ec66-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="7ec66-146">Per altre informazioni sulla creazione di certificati autofirmati e sull'assegnazione di autorizzazioni, vedere [usare Azure PowerShell per creare un'entità di servizio con un certificato](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="7ec66-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## <span data-ttu-id="7ec66-147">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ec66-147">PARAMETERS</span></span>

### <span data-ttu-id="7ec66-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="7ec66-148">-AccessToken</span></span>

<span data-ttu-id="7ec66-149">Specifica un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="7ec66-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="7ec66-150">I token di accesso sono un tipo di credenziale.</span><span class="sxs-lookup"><span data-stu-id="7ec66-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="7ec66-151">Dovresti prendere le opportune precauzioni per la sicurezza per mantenerle riservate.</span><span class="sxs-lookup"><span data-stu-id="7ec66-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="7ec66-152">I token di accesso anche timeout e può impedire il completamento delle attività in esecuzione lunga.</span><span class="sxs-lookup"><span data-stu-id="7ec66-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

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

### <span data-ttu-id="7ec66-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="7ec66-153">-AccountId</span></span>

<span data-ttu-id="7ec66-154">ID account per il token di accesso nel set di parametri **AccessToken** .</span><span class="sxs-lookup"><span data-stu-id="7ec66-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="7ec66-155">ID account per il servizio gestito nel set di parametri **ManagedService** .</span><span class="sxs-lookup"><span data-stu-id="7ec66-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="7ec66-156">Può essere un ID di risorsa del servizio gestito o l'ID client associato.</span><span class="sxs-lookup"><span data-stu-id="7ec66-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="7ec66-157">Per usare l'identità assegnata al sistema, lascia vuoto questo campo.</span><span class="sxs-lookup"><span data-stu-id="7ec66-157">To use the system assigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="7ec66-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7ec66-158">-ApplicationId</span></span>

<span data-ttu-id="7ec66-159">ID applicazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7ec66-159">Application ID of the service principal.</span></span>

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

### <span data-ttu-id="7ec66-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="7ec66-160">-CertificateThumbprint</span></span>

<span data-ttu-id="7ec66-161">Hash o identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="7ec66-161">Certificate Hash or Thumbprint.</span></span>

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

### <span data-ttu-id="7ec66-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="7ec66-162">-ContextName</span></span>

<span data-ttu-id="7ec66-163">Nome del contesto Azure predefinito per l'account di accesso.</span><span class="sxs-lookup"><span data-stu-id="7ec66-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="7ec66-164">Per altre informazioni sui contesti di Azure, vedere [oggetti Context di Azure PowerShell](/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="7ec66-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="7ec66-165">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="7ec66-165">-Credential</span></span>

<span data-ttu-id="7ec66-166">Specifica un oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="7ec66-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="7ec66-167">Per altre informazioni sull'oggetto **PSCredential** , digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="7ec66-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="7ec66-168">L'oggetto **PSCredential** fornisce l'ID utente e la password per le credenziali di ID organizzazione oppure l'ID applicazione e il segreto per le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7ec66-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="7ec66-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec66-169">-DefaultProfile</span></span>

<span data-ttu-id="7ec66-170">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec66-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ec66-171">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="7ec66-171">-Environment</span></span>

<span data-ttu-id="7ec66-172">Ambiente che contiene l'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec66-172">Environment containing the Azure account.</span></span>

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

### <span data-ttu-id="7ec66-173">-Force</span><span class="sxs-lookup"><span data-stu-id="7ec66-173">-Force</span></span>

<span data-ttu-id="7ec66-174">Sovrascrivere il contesto esistente con lo stesso nome senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7ec66-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="7ec66-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="7ec66-175">-GraphAccessToken</span></span>

<span data-ttu-id="7ec66-176">AccessToken per il servizio grafico.</span><span class="sxs-lookup"><span data-stu-id="7ec66-176">AccessToken for Graph Service.</span></span>

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

### <span data-ttu-id="7ec66-177">-Identità</span><span class="sxs-lookup"><span data-stu-id="7ec66-177">-Identity</span></span>

<span data-ttu-id="7ec66-178">Accedere usando un'identità di servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="7ec66-178">Login using a Managed Service Identity.</span></span>

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

### <span data-ttu-id="7ec66-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="7ec66-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="7ec66-180">AccessToken per il servizio del Vault.</span><span class="sxs-lookup"><span data-stu-id="7ec66-180">AccessToken for KeyVault Service.</span></span>

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

### <span data-ttu-id="7ec66-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="7ec66-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="7ec66-182">Nome host per il servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="7ec66-182">Host name for the managed service.</span></span>

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

### <span data-ttu-id="7ec66-183">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="7ec66-183">-ManagedServicePort</span></span>

<span data-ttu-id="7ec66-184">Numero di porta per il servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="7ec66-184">Port number for the managed service.</span></span>

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

### <span data-ttu-id="7ec66-185">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="7ec66-185">-ManagedServiceSecret</span></span>

<span data-ttu-id="7ec66-186">Token per l'accesso al servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="7ec66-186">Token for the managed service login.</span></span>

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

### <span data-ttu-id="7ec66-187">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="7ec66-187">-MaxContextPopulation</span></span>

<span data-ttu-id="7ec66-188">Numero massimo di abbonamento per popolare i contesti dopo l'accesso.</span><span class="sxs-lookup"><span data-stu-id="7ec66-188">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="7ec66-189">Il valore predefinito è 25.</span><span class="sxs-lookup"><span data-stu-id="7ec66-189">Default is 25.</span></span> <span data-ttu-id="7ec66-190">Per popolare tutti gli abbonamenti ai contesti, impostare su-1.</span><span class="sxs-lookup"><span data-stu-id="7ec66-190">To populate all subscriptions to contexts, set to -1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ec66-191">-Ambito</span><span class="sxs-lookup"><span data-stu-id="7ec66-191">-Scope</span></span>

<span data-ttu-id="7ec66-192">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="7ec66-192">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="7ec66-193">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7ec66-193">-ServicePrincipal</span></span>

<span data-ttu-id="7ec66-194">Indica che l'account viene autenticato fornendo le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7ec66-194">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="7ec66-195">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="7ec66-195">-SkipContextPopulation</span></span>

<span data-ttu-id="7ec66-196">Ignora la popolazione del contesto se non vengono trovati contesti.</span><span class="sxs-lookup"><span data-stu-id="7ec66-196">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="7ec66-197">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="7ec66-197">-SkipValidation</span></span>

<span data-ttu-id="7ec66-198">Ignorare la convalida per il token di accesso.</span><span class="sxs-lookup"><span data-stu-id="7ec66-198">Skip validation for access token.</span></span>

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

### <span data-ttu-id="7ec66-199">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="7ec66-199">-Subscription</span></span>

<span data-ttu-id="7ec66-200">Nome dell'abbonamento o ID.</span><span class="sxs-lookup"><span data-stu-id="7ec66-200">Subscription Name or ID.</span></span>

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

### <span data-ttu-id="7ec66-201">-Tenant</span><span class="sxs-lookup"><span data-stu-id="7ec66-201">-Tenant</span></span>

<span data-ttu-id="7ec66-202">Nome del tenant o ID facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7ec66-202">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="7ec66-203">A causa di limitazioni dell'API corrente, è necessario usare un ID tenant anziché un nome del tenant quando si esegue la connessione con un account B2B (business-to-business).</span><span class="sxs-lookup"><span data-stu-id="7ec66-203">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

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

### <span data-ttu-id="7ec66-204">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="7ec66-204">-UseDeviceAuthentication</span></span>

<span data-ttu-id="7ec66-205">Usa l'autenticazione del codice del dispositivo invece di un controllo browser.</span><span class="sxs-lookup"><span data-stu-id="7ec66-205">Use device code authentication instead of a browser control.</span></span> <span data-ttu-id="7ec66-206">Questo è il tipo di autenticazione predefinito per PowerShell versione 6 e successive.</span><span class="sxs-lookup"><span data-stu-id="7ec66-206">This is the default authentication type for PowerShell version 6 and higher.</span></span>

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

### <span data-ttu-id="7ec66-207">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7ec66-207">-Confirm</span></span>

<span data-ttu-id="7ec66-208">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ec66-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ec66-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ec66-209">-WhatIf</span></span>

<span data-ttu-id="7ec66-210">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ec66-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ec66-211">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ec66-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ec66-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec66-212">CommonParameters</span></span>
<span data-ttu-id="7ec66-213">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ec66-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec66-214">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ec66-214">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec66-215">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ec66-215">INPUTS</span></span>

### <span data-ttu-id="7ec66-216">System. String</span><span class="sxs-lookup"><span data-stu-id="7ec66-216">System.String</span></span>

## <span data-ttu-id="7ec66-217">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ec66-217">OUTPUTS</span></span>

### <span data-ttu-id="7ec66-218">Microsoft. Azure. Commands. profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="7ec66-218">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="7ec66-219">Note</span><span class="sxs-lookup"><span data-stu-id="7ec66-219">NOTES</span></span>

## <span data-ttu-id="7ec66-220">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ec66-220">RELATED LINKS</span></span>