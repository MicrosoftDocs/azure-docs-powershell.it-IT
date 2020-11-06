---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508075"
---
# <span data-ttu-id="94ce6-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="94ce6-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="94ce6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="94ce6-103">Connettersi a Azure con un account autenticato da usare con le richieste di cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="94ce6-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94ce6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94ce6-104">SYNTAX</span></span>

### <span data-ttu-id="94ce6-105">UserWithSubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94ce6-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ce6-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94ce6-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94ce6-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94ce6-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94ce6-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94ce6-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ce6-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="94ce6-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94ce6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94ce6-110">DESCRIPTION</span></span>
<span data-ttu-id="94ce6-111">Il cmdlet Connect-AzureRmAccount si connette a Azure con un account autenticato da usare con le richieste di cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="94ce6-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="94ce6-112">Puoi usare questo account autenticato solo con i cmdlet di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="94ce6-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>

<span data-ttu-id="94ce6-113">Per aggiungere un account autenticato da usare con i cmdlet di gestione dei servizi, usare il cmdlet Add-AzureAccount o Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="94ce6-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

<span data-ttu-id="94ce6-114">Dopo l'esecuzione di questo cmdlet, è possibile disconnettersi da un account di Azure usando Disconnect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="94ce6-114">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="94ce6-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94ce6-115">EXAMPLES</span></span>

### <span data-ttu-id="94ce6-116">Esempio 1: usare un login interattivo per connettersi a un account di Azure</span><span class="sxs-lookup"><span data-stu-id="94ce6-116">Example 1: Use an interactive login to connect to an Azure account</span></span>
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="94ce6-117">Questo comando consente di connettersi a un account di Azure.</span><span class="sxs-lookup"><span data-stu-id="94ce6-117">This command connects to an Azure account.</span></span>

<span data-ttu-id="94ce6-118">Per eseguire i cmdlet di Azure Resource Manager con questo account, è necessario specificare le credenziali dell'account Microsoft o dell'ID organizzazione alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="94ce6-118">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="94ce6-119">Se per le credenziali è abilitata l'autenticazione a più fattori, è necessario eseguire l'accesso usando l'opzione interattiva o usare l'autenticazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="94ce6-119">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="94ce6-120">Esempio 2: connettersi a un account di Azure usando le credenziali dell'ID organizzazione</span><span class="sxs-lookup"><span data-stu-id="94ce6-120">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="94ce6-121">Il primo comando ottiene le credenziali utente e le archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="94ce6-121">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="94ce6-122">Il secondo comando si connette a un account di Azure usando le credenziali archiviate in $Credential.</span><span class="sxs-lookup"><span data-stu-id="94ce6-122">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>

<span data-ttu-id="94ce6-123">Questo account esegue l'autenticazione con Azure Resource Manager usando le credenziali dell'ID organizzazione.</span><span class="sxs-lookup"><span data-stu-id="94ce6-123">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>

<span data-ttu-id="94ce6-124">Non è possibile usare l'autenticazione a più fattori o le credenziali dell'account Microsoft per eseguire i cmdlet di Azure Resource Manager con questo account.</span><span class="sxs-lookup"><span data-stu-id="94ce6-124">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="94ce6-125">Esempio 3: connettersi a un account principale di Azure Service</span><span class="sxs-lookup"><span data-stu-id="94ce6-125">Example 3: Connect to an Azure service principal account</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="94ce6-126">Il primo comando ottiene le credenziali utente e le archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="94ce6-126">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="94ce6-127">Il secondo comando consente di connettersi a Azure usando le credenziali dell'entità servizio archiviate in $Credential per il tenant specificato.</span><span class="sxs-lookup"><span data-stu-id="94ce6-127">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>

<span data-ttu-id="94ce6-128">Il parametro ServicePrincipal switch indica che l'account viene autenticato come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="94ce6-128">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="94ce6-129">Esempio 4: usare un account di accesso interattivo per connettersi a un account per un tenant e un abbonamento specifici</span><span class="sxs-lookup"><span data-stu-id="94ce6-129">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="94ce6-130">Questo comando consente di connettersi a un account di Azure e configurare AzureRM PowerShell per eseguire i cmdlet per il tenant e la sottoscrizione specificati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="94ce6-130">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="94ce6-131">Esempio 5: aggiungere un account con l'accesso all'identità del servizio gestito</span><span class="sxs-lookup"><span data-stu-id="94ce6-131">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="94ce6-132">Questo comando accede usando l'identità del servizio gestito dell'ambiente host (ad esempio, se eseguito su un VirtualMachine con un'identità del servizio gestito assegnata, questo consentirà al codice di accedere usando l'identità assegnata)</span><span class="sxs-lookup"><span data-stu-id="94ce6-132">This command logs in using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

## <span data-ttu-id="94ce6-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94ce6-133">PARAMETERS</span></span>

### <span data-ttu-id="94ce6-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="94ce6-134">-AccessToken</span></span>
<span data-ttu-id="94ce6-135">Specifica un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="94ce6-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="94ce6-136">-AccountId</span></span>
<span data-ttu-id="94ce6-137">ID account per il token di accesso</span><span class="sxs-lookup"><span data-stu-id="94ce6-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="94ce6-138">-ApplicationId</span></span>
<span data-ttu-id="94ce6-139">SPN</span><span class="sxs-lookup"><span data-stu-id="94ce6-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="94ce6-140">-CertificateThumbprint</span></span>
<span data-ttu-id="94ce6-141">Hash del certificato (identificazione personale)</span><span class="sxs-lookup"><span data-stu-id="94ce6-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-142">-ContextName</span><span class="sxs-lookup"><span data-stu-id="94ce6-142">-ContextName</span></span>
<span data-ttu-id="94ce6-143">Nome del contesto predefinito da questo account di accesso.</span><span class="sxs-lookup"><span data-stu-id="94ce6-143">Name of the default context from this login.</span></span>  <span data-ttu-id="94ce6-144">Dopo l'accesso, sarà possibile selezionare questo contesto con questo nome.</span><span class="sxs-lookup"><span data-stu-id="94ce6-144">You will be able to select this context by this name after login.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-145">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="94ce6-145">-Credential</span></span>
<span data-ttu-id="94ce6-146">Specifica un oggetto PSCredential.</span><span class="sxs-lookup"><span data-stu-id="94ce6-146">Specifies a PSCredential object.</span></span>
<span data-ttu-id="94ce6-147">Per altre informazioni sull'oggetto PSCredential, digitare Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="94ce6-147">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="94ce6-148">L'oggetto PSCredential fornisce l'ID utente e la password per le credenziali di ID organizzazione oppure l'ID applicazione e il segreto per le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="94ce6-148">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ce6-149">-DefaultProfile</span></span>
<span data-ttu-id="94ce6-150">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94ce6-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-151">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="94ce6-151">-Environment</span></span>
<span data-ttu-id="94ce6-152">Ambiente che contiene l'account per l'accesso</span><span class="sxs-lookup"><span data-stu-id="94ce6-152">Environment containing the account to log into</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-153">-Force</span><span class="sxs-lookup"><span data-stu-id="94ce6-153">-Force</span></span>
<span data-ttu-id="94ce6-154">Sovrascrivere il contesto esistente con lo stesso nome, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="94ce6-154">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-155">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="94ce6-155">-GraphAccessToken</span></span>
<span data-ttu-id="94ce6-156">AccessToken per il servizio grafico</span><span class="sxs-lookup"><span data-stu-id="94ce6-156">AccessToken for Graph Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-157">-Identità</span><span class="sxs-lookup"><span data-stu-id="94ce6-157">-Identity</span></span>
<span data-ttu-id="94ce6-158">Accedere usando l'identità del servizio gestito nell'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="94ce6-158">Login using managed service identity in the current environment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-159">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="94ce6-159">-KeyVaultAccessToken</span></span>
<span data-ttu-id="94ce6-160">AccessToken per il servizio con il Vault</span><span class="sxs-lookup"><span data-stu-id="94ce6-160">AccessToken for KeyVault Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-161">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="94ce6-161">-ManagedServiceHostName</span></span>
<span data-ttu-id="94ce6-162">Nome host per l'accesso al servizio gestito</span><span class="sxs-lookup"><span data-stu-id="94ce6-162">Host name for managed service login</span></span>

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-163">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="94ce6-163">-ManagedServicePort</span></span>
<span data-ttu-id="94ce6-164">Numero di porta per l'accesso al servizio gestito</span><span class="sxs-lookup"><span data-stu-id="94ce6-164">Port number for managed service login</span></span>

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-165">-Ambito</span><span class="sxs-lookup"><span data-stu-id="94ce6-165">-Scope</span></span>
<span data-ttu-id="94ce6-166">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="94ce6-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-167">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="94ce6-167">-ServicePrincipal</span></span>
<span data-ttu-id="94ce6-168">Indica che l'account viene autenticato fornendo le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="94ce6-168">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-169">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="94ce6-169">-SkipValidation</span></span>
<span data-ttu-id="94ce6-170">Ignorare la convalida per il token di accesso</span><span class="sxs-lookup"><span data-stu-id="94ce6-170">Skip validation for access token</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-171">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="94ce6-171">-Subscription</span></span>
<span data-ttu-id="94ce6-172">Nome dell'abbonamento o ID</span><span class="sxs-lookup"><span data-stu-id="94ce6-172">Subscription Name or ID</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-173">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="94ce6-173">-TenantId</span></span>
<span data-ttu-id="94ce6-174">Nome del tenant o ID facoltativo</span><span class="sxs-lookup"><span data-stu-id="94ce6-174">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-175">-Confermare</span><span class="sxs-lookup"><span data-stu-id="94ce6-175">-Confirm</span></span>
<span data-ttu-id="94ce6-176">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94ce6-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94ce6-177">-WhatIf</span></span>
<span data-ttu-id="94ce6-178">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94ce6-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94ce6-179">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94ce6-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ce6-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ce6-180">CommonParameters</span></span>
<span data-ttu-id="94ce6-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ce6-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ce6-182">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94ce6-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ce6-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94ce6-183">INPUTS</span></span>

### <span data-ttu-id="94ce6-184">Stringa</span><span class="sxs-lookup"><span data-stu-id="94ce6-184">String</span></span>
<span data-ttu-id="94ce6-185">Il parametro ' SubscriptionId ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="94ce6-185">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="94ce6-186">Stringa</span><span class="sxs-lookup"><span data-stu-id="94ce6-186">String</span></span>
<span data-ttu-id="94ce6-187">Il parametro "Subscriptionname" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="94ce6-187">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="94ce6-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94ce6-188">OUTPUTS</span></span>

### <span data-ttu-id="94ce6-189">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="94ce6-189">PSAzureProfile</span></span>
<span data-ttu-id="94ce6-190">Informazioni su credenziali, abbonamenti, account e tenant per l'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="94ce6-190">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="94ce6-191">Note</span><span class="sxs-lookup"><span data-stu-id="94ce6-191">NOTES</span></span>

## <span data-ttu-id="94ce6-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94ce6-192">RELATED LINKS</span></span>

