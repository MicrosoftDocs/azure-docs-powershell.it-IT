---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: dcf4e78e9b6e467961eb05dd141396e426dfe5e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999121"
---
# <span data-ttu-id="39988-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="39988-101">Connect-AzAccount</span></span>

## <span data-ttu-id="39988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39988-102">SYNOPSIS</span></span>
<span data-ttu-id="39988-103">Connettersi ad Azure con un account autenticato per usarlo con i cmdlet dei moduli di PowerShell di Az.</span><span class="sxs-lookup"><span data-stu-id="39988-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="39988-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39988-104">SYNTAX</span></span>

### <span data-ttu-id="39988-105">UserWithSubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39988-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39988-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39988-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39988-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="39988-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39988-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39988-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39988-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39988-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39988-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="39988-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39988-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39988-111">DESCRIPTION</span></span>

<span data-ttu-id="39988-112">Il cmdlet si connette ad Azure con un account autenticato da usare con `Connect-AzAccount` i cmdlet dei moduli di PowerShell di Az.</span><span class="sxs-lookup"><span data-stu-id="39988-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="39988-113">È possibile usare questo account autenticato solo con le richieste di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="39988-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="39988-114">Per aggiungere un account autenticato da usare con Gestione servizi, usare il `Add-AzureAccount` cmdlet del modulo Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="39988-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="39988-115">Se non viene trovato alcun contesto per l'utente corrente, l'elenco di contesto dell'utente viene popolato con un contesto per ognuna delle prime 25 sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="39988-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="39988-116">L'elenco dei contesti creati per l'utente è disponibile eseguendo `Get-AzContext -ListAvailable` .</span><span class="sxs-lookup"><span data-stu-id="39988-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="39988-117">Per ignorare questa popolazione di contesto, specificare il **parametro SkipContextPopulation.**</span><span class="sxs-lookup"><span data-stu-id="39988-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="39988-118">Dopo aver eseguito questo cmdlet, puoi disconnetterti da un account Azure tramite `Disconnect-AzAccount` .</span><span class="sxs-lookup"><span data-stu-id="39988-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="39988-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39988-119">EXAMPLES</span></span>

### <span data-ttu-id="39988-120">Esempio 1: Connettersi a un account di Azure</span><span class="sxs-lookup"><span data-stu-id="39988-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="39988-121">Questo esempio si connette a un account di Azure.</span><span class="sxs-lookup"><span data-stu-id="39988-121">This example connects to an Azure account.</span></span> <span data-ttu-id="39988-122">È necessario specificare le credenziali di un account Microsoft o di un ID organizzazione.</span><span class="sxs-lookup"><span data-stu-id="39988-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="39988-123">Se per le credenziali è abilitata l'autenticazione a più fattori, è necessario accedere con l'opzione interattiva o usare l'autenticazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="39988-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="39988-124">Esempio 2: (solo Windows PowerShell 5.1) Connettersi ad Azure usando le credenziali dell'ID organizzazione</span><span class="sxs-lookup"><span data-stu-id="39988-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="39988-125">Questo scenario funziona solo in Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="39988-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="39988-126">Il primo comando richiede le credenziali utente e le archivia nella `$Credential` variabile.</span><span class="sxs-lookup"><span data-stu-id="39988-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="39988-127">Il secondo comando si connette a un account Azure usando le credenziali archiviate `$Credential` in.</span><span class="sxs-lookup"><span data-stu-id="39988-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="39988-128">Questo account esegue l'autenticazione con Azure usando le credenziali dell'ID organizzazione.</span><span class="sxs-lookup"><span data-stu-id="39988-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="39988-129">Esempio 3: Connettersi ad Azure usando un account dell'entità servizio</span><span class="sxs-lookup"><span data-stu-id="39988-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="39988-130">Il primo comando richiede le credenziali dell'entità servizio e le archivia nella `$Credential` variabile.</span><span class="sxs-lookup"><span data-stu-id="39988-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="39988-131">Immettere l'ID applicazione per il nome utente e il segreto entità servizio come password quando richiesto.</span><span class="sxs-lookup"><span data-stu-id="39988-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="39988-132">Il secondo comando connette il tenant di Azure specificato usando le credenziali dell'entità servizio archiviate nella `$Credential` variabile.</span><span class="sxs-lookup"><span data-stu-id="39988-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="39988-133">Il **parametro ServicePrincipal** switch indica che l'account esegue l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="39988-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="39988-134">Esempio 4: Usare un accesso interattivo per connettersi a un tenant e a un abbonamento specifico</span><span class="sxs-lookup"><span data-stu-id="39988-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="39988-135">Questo esempio si connette a un account azure con il tenant e la sottoscrizione specificati.</span><span class="sxs-lookup"><span data-stu-id="39988-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="39988-136">Esempio 5: Connettersi usando un'identità del servizio gestito</span><span class="sxs-lookup"><span data-stu-id="39988-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="39988-137">Questo esempio si connette usando l'identità del servizio gestito (MSI) dell'ambiente host.</span><span class="sxs-lookup"><span data-stu-id="39988-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="39988-138">Ad esempio, si accede ad Azure da una macchina virtuale a cui è assegnato un file MSI.</span><span class="sxs-lookup"><span data-stu-id="39988-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="39988-139">Esempio 6: Connettersi usando l'accesso all'identità del servizio gestito e ClientId</span><span class="sxs-lookup"><span data-stu-id="39988-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="39988-140">Questo esempio si connette usando l'identità del servizio gestito **di myUserAssignedIdentity.**</span><span class="sxs-lookup"><span data-stu-id="39988-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="39988-141">Aggiunge l'identità assegnata all'utente alla macchina virtuale, quindi si connette usando l'ID Client dell'identità assegnata all'utente.</span><span class="sxs-lookup"><span data-stu-id="39988-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="39988-142">Per altre informazioni, vedere [Configurare le identità gestite per le risorse di Azure in una macchina virtuale di Azure.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)</span><span class="sxs-lookup"><span data-stu-id="39988-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

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

### <span data-ttu-id="39988-143">Esempio 7: Connettersi usando certificati</span><span class="sxs-lookup"><span data-stu-id="39988-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="39988-144">Questo esempio si connette a un account di Azure usando l'autenticazione dell'entità servizio basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="39988-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="39988-145">L'entità servizio usata per l'autenticazione deve essere creata con il certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="39988-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="39988-146">Per altre informazioni sulla creazione di certificati autofirmati e sull'assegnazione delle autorizzazioni, vedere Usare [Azure PowerShell](/azure/active-directory/develop/howto-authenticate-service-principal-powershell) per creare un'entità servizio con un certificato</span><span class="sxs-lookup"><span data-stu-id="39988-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

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

## <span data-ttu-id="39988-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39988-147">PARAMETERS</span></span>

### <span data-ttu-id="39988-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="39988-148">-AccessToken</span></span>

<span data-ttu-id="39988-149">Specifica un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="39988-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="39988-150">I token di accesso sono un tipo di credenziali.</span><span class="sxs-lookup"><span data-stu-id="39988-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="39988-151">È consigliabile adottare le appropriate precauzioni di sicurezza per mantenerle riservate.</span><span class="sxs-lookup"><span data-stu-id="39988-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="39988-152">Anche i token di accesso timeout e possono impedire il completamento di attività a esecuzione lunga.</span><span class="sxs-lookup"><span data-stu-id="39988-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

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

### <span data-ttu-id="39988-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="39988-153">-AccountId</span></span>

<span data-ttu-id="39988-154">ID account per il token di accesso nel set **di parametri AccessToken.**</span><span class="sxs-lookup"><span data-stu-id="39988-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="39988-155">ID account per il servizio gestito nel **set di parametri ManagedService.**</span><span class="sxs-lookup"><span data-stu-id="39988-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="39988-156">Può essere un ID risorsa del servizio gestito o l'ID client associato.</span><span class="sxs-lookup"><span data-stu-id="39988-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="39988-157">Per usare l'identità assegnata al sistema, lasciare vuoto questo campo.</span><span class="sxs-lookup"><span data-stu-id="39988-157">To use the system assigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="39988-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="39988-158">-ApplicationId</span></span>

<span data-ttu-id="39988-159">ID applicazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="39988-159">Application ID of the service principal.</span></span>

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

### <span data-ttu-id="39988-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="39988-160">-CertificateThumbprint</span></span>

<span data-ttu-id="39988-161">Certificate Hash or Thumbprint.</span><span class="sxs-lookup"><span data-stu-id="39988-161">Certificate Hash or Thumbprint.</span></span>

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

### <span data-ttu-id="39988-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="39988-162">-ContextName</span></span>

<span data-ttu-id="39988-163">Nome del contesto di Azure predefinito per questo accesso.</span><span class="sxs-lookup"><span data-stu-id="39988-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="39988-164">Per altre informazioni sui contesti di Azure, vedere [gli oggetti di contesto di Azure PowerShell.](/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="39988-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="39988-165">-Credential</span><span class="sxs-lookup"><span data-stu-id="39988-165">-Credential</span></span>

<span data-ttu-id="39988-166">Specifica un **oggetto PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="39988-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="39988-167">Per altre informazioni **sull'oggetto PSCredential,** digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="39988-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="39988-168">**L'oggetto PSCredential** fornisce l'ID utente e la password per le credenziali dell'ID organizzazione oppure l'ID applicazione e il segreto per le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="39988-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="39988-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39988-169">-DefaultProfile</span></span>

<span data-ttu-id="39988-170">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39988-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39988-171">-Environment</span><span class="sxs-lookup"><span data-stu-id="39988-171">-Environment</span></span>

<span data-ttu-id="39988-172">Ambiente contenente l'account Azure.</span><span class="sxs-lookup"><span data-stu-id="39988-172">Environment containing the Azure account.</span></span>

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

### <span data-ttu-id="39988-173">-Force</span><span class="sxs-lookup"><span data-stu-id="39988-173">-Force</span></span>

<span data-ttu-id="39988-174">Sovrascrivere il contesto esistente con lo stesso nome senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="39988-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="39988-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="39988-175">-GraphAccessToken</span></span>

<span data-ttu-id="39988-176">AccessToken per il servizio Graph.</span><span class="sxs-lookup"><span data-stu-id="39988-176">AccessToken for Graph Service.</span></span>

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

### <span data-ttu-id="39988-177">-Identity</span><span class="sxs-lookup"><span data-stu-id="39988-177">-Identity</span></span>

<span data-ttu-id="39988-178">Accedere con un'identità del servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="39988-178">Login using a Managed Service Identity.</span></span>

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

### <span data-ttu-id="39988-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="39988-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="39988-180">AccessToken per il servizio KeyVault.</span><span class="sxs-lookup"><span data-stu-id="39988-180">AccessToken for KeyVault Service.</span></span>

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

### <span data-ttu-id="39988-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="39988-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="39988-182">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="39988-182">Obsolete.</span></span> <span data-ttu-id="39988-183">Per usare un endpoint MSI personalizzato, impostare la MSI_ENDPOINT di ambiente, ad esempio " http://localhost:50342/oauth2/token ".</span><span class="sxs-lookup"><span data-stu-id="39988-183">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".</span></span> <span data-ttu-id="39988-184">Nome host per il servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="39988-184">Host name for the managed service.</span></span>

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

### <span data-ttu-id="39988-185">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="39988-185">-ManagedServicePort</span></span>

<span data-ttu-id="39988-186">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="39988-186">Obsolete.</span></span> <span data-ttu-id="39988-187">Per usare un endpoint MSI personalizzato, impostare la MSI_ENDPOINT di ambiente, ad esempio " http://localhost:50342/oauth2/token ". Numero di porta per il servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="39988-187">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".Port number for the managed service.</span></span>

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

### <span data-ttu-id="39988-188">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="39988-188">-ManagedServiceSecret</span></span>

<span data-ttu-id="39988-189">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="39988-189">Obsolete.</span></span> <span data-ttu-id="39988-190">Per usare segreto MSI personalizzato, impostare la variabile di ambiente MSI_SECRET.</span><span class="sxs-lookup"><span data-stu-id="39988-190">To use customized MSI secret, please set environment variable MSI_SECRET.</span></span> <span data-ttu-id="39988-191">Token per l'accesso al servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="39988-191">Token for the managed service login.</span></span>

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

### <span data-ttu-id="39988-192">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="39988-192">-MaxContextPopulation</span></span>

<span data-ttu-id="39988-193">Numero massimo di abbonamento per popolare i contesti dopo l'accesso.</span><span class="sxs-lookup"><span data-stu-id="39988-193">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="39988-194">Il valore predefinito è 25.</span><span class="sxs-lookup"><span data-stu-id="39988-194">Default is 25.</span></span> <span data-ttu-id="39988-195">Per popolare tutte le sottoscrizioni in contesti, impostare su -1.</span><span class="sxs-lookup"><span data-stu-id="39988-195">To populate all subscriptions to contexts, set to -1.</span></span>

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

### <span data-ttu-id="39988-196">-Scope</span><span class="sxs-lookup"><span data-stu-id="39988-196">-Scope</span></span>

<span data-ttu-id="39988-197">Determina l'ambito delle modifiche di contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="39988-197">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="39988-198">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="39988-198">-ServicePrincipal</span></span>

<span data-ttu-id="39988-199">Indica che l'account esegue l'autenticazione fornendo le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="39988-199">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="39988-200">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="39988-200">-SkipContextPopulation</span></span>

<span data-ttu-id="39988-201">Ignora la popolazione di contesto se non vengono trovati contesti.</span><span class="sxs-lookup"><span data-stu-id="39988-201">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="39988-202">-SkipValido</span><span class="sxs-lookup"><span data-stu-id="39988-202">-SkipValidation</span></span>

<span data-ttu-id="39988-203">Ignorare la convalida per il token di accesso.</span><span class="sxs-lookup"><span data-stu-id="39988-203">Skip validation for access token.</span></span>

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

### <span data-ttu-id="39988-204">-Abbonamento</span><span class="sxs-lookup"><span data-stu-id="39988-204">-Subscription</span></span>

<span data-ttu-id="39988-205">ID o nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="39988-205">Subscription Name or ID.</span></span>

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

### <span data-ttu-id="39988-206">-Tenant</span><span class="sxs-lookup"><span data-stu-id="39988-206">-Tenant</span></span>

<span data-ttu-id="39988-207">Id o nome tenant facoltativo.</span><span class="sxs-lookup"><span data-stu-id="39988-207">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="39988-208">A causa delle limitazioni dell'API corrente, è necessario usare un ID tenant invece di un nome tenant quando ci si connette con un account Business to Business (B2B).</span><span class="sxs-lookup"><span data-stu-id="39988-208">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

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

### <span data-ttu-id="39988-209">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="39988-209">-UseDeviceAuthentication</span></span>

<span data-ttu-id="39988-210">Usare l'autenticazione del codice del dispositivo invece di un controllo browser.</span><span class="sxs-lookup"><span data-stu-id="39988-210">Use device code authentication instead of a browser control.</span></span>

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

### <span data-ttu-id="39988-211">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39988-211">-Confirm</span></span>

<span data-ttu-id="39988-212">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39988-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39988-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39988-213">-WhatIf</span></span>

<span data-ttu-id="39988-214">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39988-214">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39988-215">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39988-215">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39988-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39988-216">CommonParameters</span></span>
<span data-ttu-id="39988-217">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39988-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39988-218">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39988-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39988-219">INPUT</span><span class="sxs-lookup"><span data-stu-id="39988-219">INPUTS</span></span>

### <span data-ttu-id="39988-220">System.String</span><span class="sxs-lookup"><span data-stu-id="39988-220">System.String</span></span>

## <span data-ttu-id="39988-221">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39988-221">OUTPUTS</span></span>

### <span data-ttu-id="39988-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="39988-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="39988-223">NOTE</span><span class="sxs-lookup"><span data-stu-id="39988-223">NOTES</span></span>

## <span data-ttu-id="39988-224">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39988-224">RELATED LINKS</span></span>
