---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688063"
---
# <span data-ttu-id="5a9a3-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="5a9a3-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="5a9a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="5a9a3-103">Connettersi a Azure con un account autenticato da usare con le richieste di cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a9a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a9a3-104">SYNTAX</span></span>

### <span data-ttu-id="5a9a3-105">UserWithSubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a9a3-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a9a3-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a9a3-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a9a3-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a9a3-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a9a3-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a9a3-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a9a3-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="5a9a3-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a9a3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a9a3-110">DESCRIPTION</span></span>
<span data-ttu-id="5a9a3-111">Il cmdlet Connect-AzureRmAccount si connette a Azure con un account autenticato da usare con le richieste di cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="5a9a3-112">Puoi usare questo account autenticato solo con i cmdlet di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="5a9a3-113">Per aggiungere un account autenticato da usare con i cmdlet di gestione dei servizi, usare il cmdlet Add-AzureAccount o Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="5a9a3-114">Se non viene trovato alcun contesto per l'utente corrente, questo comando compilerà l'elenco di contesto dell'utente con un contesto per ogni abbonamento (primo 25).</span><span class="sxs-lookup"><span data-stu-id="5a9a3-114">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="5a9a3-115">L'elenco dei contesti creati per l'utente può essere trovato eseguendo "Get-AzureRmContext-ListAvailable".</span><span class="sxs-lookup"><span data-stu-id="5a9a3-115">The list of contexts created for the user can be found by running "Get-AzureRmContext -ListAvailable".</span></span> <span data-ttu-id="5a9a3-116">Per ignorare questa popolazione di contesto, è possibile eseguire questo comando con il parametro di opzione "-SkipContextPopulation".</span><span class="sxs-lookup"><span data-stu-id="5a9a3-116">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="5a9a3-117">Dopo l'esecuzione di questo cmdlet, è possibile disconnettersi da un account di Azure usando Disconnect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-117">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="5a9a3-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a9a3-118">EXAMPLES</span></span>

### <span data-ttu-id="5a9a3-119">Esempio 1: usare un login interattivo per connettersi a un account di Azure</span><span class="sxs-lookup"><span data-stu-id="5a9a3-119">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="5a9a3-120">Questo comando consente di connettersi a un account di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-120">This command connects to an Azure account.</span></span>
<span data-ttu-id="5a9a3-121">Per eseguire i cmdlet di Azure Resource Manager con questo account, è necessario specificare le credenziali dell'account Microsoft o dell'ID organizzazione alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-121">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="5a9a3-122">Se per le credenziali è abilitata l'autenticazione a più fattori, è necessario eseguire l'accesso usando l'opzione interattiva o usare l'autenticazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-122">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="5a9a3-123">Esempio 2: connettersi a un account di Azure usando le credenziali dell'ID organizzazione</span><span class="sxs-lookup"><span data-stu-id="5a9a3-123">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="5a9a3-124">Il primo comando richiederà le credenziali utente (nome utente e password) e li archivierà nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-124">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="5a9a3-125">Il secondo comando si connette a un account di Azure usando le credenziali archiviate in $Credential.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-125">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="5a9a3-126">Questo account esegue l'autenticazione con Azure Resource Manager usando le credenziali dell'ID organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-126">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="5a9a3-127">Non è possibile usare l'autenticazione a più fattori o le credenziali dell'account Microsoft per eseguire i cmdlet di Azure Resource Manager con questo account.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-127">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="5a9a3-128">Esempio 3: connettersi a un account principale di Azure Service</span><span class="sxs-lookup"><span data-stu-id="5a9a3-128">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="5a9a3-129">Il primo comando ottiene le credenziali dell'entità servizio (ID applicazione e segreto principale del servizio), quindi le archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-129">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="5a9a3-130">Il secondo comando consente di connettersi a Azure usando le credenziali dell'entità servizio archiviate in $Credential per il tenant specificato.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-130">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="5a9a3-131">Il parametro ServicePrincipal switch indica che l'account viene autenticato come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-131">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="5a9a3-132">Esempio 4: usare un account di accesso interattivo per connettersi a un account per un tenant e un abbonamento specifici</span><span class="sxs-lookup"><span data-stu-id="5a9a3-132">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="5a9a3-133">Questo comando consente di connettersi a un account di Azure e configurare AzureRM PowerShell per eseguire i cmdlet per il tenant e la sottoscrizione specificati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-133">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="5a9a3-134">Esempio 5: aggiungere un account con l'accesso all'identità del servizio gestito</span><span class="sxs-lookup"><span data-stu-id="5a9a3-134">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="5a9a3-135">Questo comando consente di connettersi usando l'identità del servizio gestito dell'ambiente host, ad esempio se eseguito su un VirtualMachine con un'identità del servizio gestito assegnata, in modo da consentire al codice di accedere usando l'identità assegnata.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-135">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="5a9a3-136">Esempio 6: aggiungere un account usando i certificati</span><span class="sxs-lookup"><span data-stu-id="5a9a3-136">Example 6: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="5a9a3-137">Questo comando consente di connettersi a un account di Azure usando l'autenticazione dell'entità servizio basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-137">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="5a9a3-138">Il theservice Principal usato per l'autenticazione deve essere stato creato con il certificato indicato.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-138">Theservice principal used for authentication should have been created with the given certificate.</span></span>

## <span data-ttu-id="5a9a3-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a9a3-139">PARAMETERS</span></span>

### <span data-ttu-id="5a9a3-140">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="5a9a3-140">-AccessToken</span></span>
<span data-ttu-id="5a9a3-141">Specifica un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-141">Specifies an access token.</span></span>

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

### <span data-ttu-id="5a9a3-142">-AccountId</span><span class="sxs-lookup"><span data-stu-id="5a9a3-142">-AccountId</span></span>
<span data-ttu-id="5a9a3-143">ID account per il token di accesso</span><span class="sxs-lookup"><span data-stu-id="5a9a3-143">Account Id for access token</span></span>

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

### <span data-ttu-id="5a9a3-144">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5a9a3-144">-ApplicationId</span></span>
<span data-ttu-id="5a9a3-145">SPN</span><span class="sxs-lookup"><span data-stu-id="5a9a3-145">SPN</span></span>

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

### <span data-ttu-id="5a9a3-146">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="5a9a3-146">-CertificateThumbprint</span></span>
<span data-ttu-id="5a9a3-147">Hash del certificato (identificazione personale)</span><span class="sxs-lookup"><span data-stu-id="5a9a3-147">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="5a9a3-148">-ContextName</span><span class="sxs-lookup"><span data-stu-id="5a9a3-148">-ContextName</span></span>
<span data-ttu-id="5a9a3-149">Nome del contesto predefinito da questo account di accesso.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-149">Name of the default context from this login.</span></span>  <span data-ttu-id="5a9a3-150">Dopo l'accesso, sarà possibile selezionare questo contesto con questo nome.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-150">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="5a9a3-151">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="5a9a3-151">-Credential</span></span>
<span data-ttu-id="5a9a3-152">Specifica un oggetto PSCredential.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-152">Specifies a PSCredential object.</span></span>
<span data-ttu-id="5a9a3-153">Per altre informazioni sull'oggetto PSCredential, digitare Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-153">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="5a9a3-154">L'oggetto PSCredential fornisce l'ID utente e la password per le credenziali di ID organizzazione oppure l'ID applicazione e il segreto per le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-154">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a9a3-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a9a3-155">-DefaultProfile</span></span>
<span data-ttu-id="5a9a3-156">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a9a3-157">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="5a9a3-157">-Environment</span></span>
<span data-ttu-id="5a9a3-158">Ambiente che contiene l'account per l'accesso</span><span class="sxs-lookup"><span data-stu-id="5a9a3-158">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="5a9a3-159">-Force</span><span class="sxs-lookup"><span data-stu-id="5a9a3-159">-Force</span></span>
<span data-ttu-id="5a9a3-160">Sovrascrivere il contesto esistente con lo stesso nome, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-160">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="5a9a3-161">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="5a9a3-161">-GraphAccessToken</span></span>
<span data-ttu-id="5a9a3-162">AccessToken per il servizio grafico</span><span class="sxs-lookup"><span data-stu-id="5a9a3-162">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="5a9a3-163">-Identità</span><span class="sxs-lookup"><span data-stu-id="5a9a3-163">-Identity</span></span>
<span data-ttu-id="5a9a3-164">Accedere usando l'identità del servizio gestito nell'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-164">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="5a9a3-165">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="5a9a3-165">-KeyVaultAccessToken</span></span>
<span data-ttu-id="5a9a3-166">AccessToken per il servizio con il Vault</span><span class="sxs-lookup"><span data-stu-id="5a9a3-166">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="5a9a3-167">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="5a9a3-167">-ManagedServiceHostName</span></span>
<span data-ttu-id="5a9a3-168">Nome host per l'accesso al servizio gestito</span><span class="sxs-lookup"><span data-stu-id="5a9a3-168">Host name for managed service login</span></span>

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

### <span data-ttu-id="5a9a3-169">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="5a9a3-169">-ManagedServicePort</span></span>
<span data-ttu-id="5a9a3-170">Numero di porta per l'accesso al servizio gestito</span><span class="sxs-lookup"><span data-stu-id="5a9a3-170">Port number for managed service login</span></span>

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

### <span data-ttu-id="5a9a3-171">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="5a9a3-171">-ManagedServiceSecret</span></span>
<span data-ttu-id="5a9a3-172">Segreto, usato per alcuni tipi di accesso al servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-172">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="5a9a3-173">-Ambito</span><span class="sxs-lookup"><span data-stu-id="5a9a3-173">-Scope</span></span>
<span data-ttu-id="5a9a3-174">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-174">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="5a9a3-175">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5a9a3-175">-ServicePrincipal</span></span>
<span data-ttu-id="5a9a3-176">Indica che l'account viene autenticato fornendo le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-176">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="5a9a3-177">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="5a9a3-177">-SkipContextPopulation</span></span>
<span data-ttu-id="5a9a3-178">Ignora la popolazione del contesto se non vengono trovati contesti.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-178">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="5a9a3-179">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="5a9a3-179">-SkipValidation</span></span>
<span data-ttu-id="5a9a3-180">Ignorare la convalida per il token di accesso</span><span class="sxs-lookup"><span data-stu-id="5a9a3-180">Skip validation for access token</span></span>

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

### <span data-ttu-id="5a9a3-181">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="5a9a3-181">-Subscription</span></span>
<span data-ttu-id="5a9a3-182">Nome dell'abbonamento o ID</span><span class="sxs-lookup"><span data-stu-id="5a9a3-182">Subscription Name or ID</span></span>

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

### <span data-ttu-id="5a9a3-183">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="5a9a3-183">-TenantId</span></span>
<span data-ttu-id="5a9a3-184">Nome di dominio facoltativo o ID tenant.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-184">Optional domain name or tenant ID.</span></span> <span data-ttu-id="5a9a3-185">Il nome di dominio non funzionerà in tutte le situazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-185">Domain name will not work in all sign-in situations.</span></span> <span data-ttu-id="5a9a3-186">Per l'accesso al provider di soluzioni cloud (CSP) è necessario l'ID tenant.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-186">For Cloud Solution Provider (CSP) sign-in, tenant ID is required.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a9a3-187">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a9a3-187">-Confirm</span></span>
<span data-ttu-id="5a9a3-188">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a9a3-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a9a3-189">-WhatIf</span></span>
<span data-ttu-id="5a9a3-190">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a9a3-191">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a9a3-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a9a3-192">CommonParameters</span></span>
<span data-ttu-id="5a9a3-193">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a9a3-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a9a3-194">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a9a3-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a9a3-195">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a9a3-195">INPUTS</span></span>

### <span data-ttu-id="5a9a3-196">System. String</span><span class="sxs-lookup"><span data-stu-id="5a9a3-196">System.String</span></span>
<span data-ttu-id="5a9a3-197">Parameters: Subscription (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5a9a3-197">Parameters: Subscription (ByValue)</span></span>

## <span data-ttu-id="5a9a3-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a9a3-198">OUTPUTS</span></span>

### <span data-ttu-id="5a9a3-199">Microsoft. Azure. Commands. profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="5a9a3-199">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="5a9a3-200">Note</span><span class="sxs-lookup"><span data-stu-id="5a9a3-200">NOTES</span></span>

## <span data-ttu-id="5a9a3-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a9a3-201">RELATED LINKS</span></span>
