---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
ms.openlocfilehash: 11303438a50839bbe05139888cc665198ed09810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521170"
---
# <span data-ttu-id="12e68-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="12e68-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="12e68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12e68-102">SYNOPSIS</span></span>
<span data-ttu-id="12e68-103">Aggiunge un account autenticato da usare per le richieste di cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="12e68-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12e68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12e68-104">SYNTAX</span></span>

### <span data-ttu-id="12e68-105">UserWithSubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12e68-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e68-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12e68-106">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e68-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12e68-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12e68-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12e68-108">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12e68-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12e68-109">DESCRIPTION</span></span>
<span data-ttu-id="12e68-110">Il cmdlet Add-AzureRmAcccount aggiunge un account Azure autenticato da usare per le richieste di cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="12e68-110">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="12e68-111">Puoi usare questo account autenticato solo con i cmdlet di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="12e68-111">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="12e68-112">Per aggiungere un account autenticato da usare con i cmdlet di gestione dei servizi, usare il cmdlet Add-AzureAccount o Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="12e68-112">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="12e68-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12e68-113">EXAMPLES</span></span>

### <span data-ttu-id="12e68-114">Esempio 1: aggiungere un account che richiede l'accesso interattivo</span><span class="sxs-lookup"><span data-stu-id="12e68-114">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="12e68-115">Questo comando aggiunge un account di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="12e68-115">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="12e68-116">Per eseguire i cmdlet di Azure Resource Manager con questo account, è necessario specificare le credenziali dell'account Microsoft o dell'ID organizzazione alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="12e68-116">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="12e68-117">Se per le credenziali è abilitata l'autenticazione a più fattori, è necessario eseguire l'accesso usando l'opzione interattiva o usare l'autenticazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="12e68-117">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="12e68-118">Esempio 2: aggiungere un account che esegue l'autenticazione con le credenziali dell'ID organizzazione</span><span class="sxs-lookup"><span data-stu-id="12e68-118">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="12e68-119">Il primo comando ottiene le credenziali utente e le archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="12e68-119">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="12e68-120">Il secondo comando aggiunge un account di gestione risorse di Azure con le credenziali in $Credential.</span><span class="sxs-lookup"><span data-stu-id="12e68-120">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="12e68-121">Questo account esegue l'autenticazione con Azure Resource Manager usando le credenziali dell'ID organizzazione.</span><span class="sxs-lookup"><span data-stu-id="12e68-121">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="12e68-122">Non è possibile usare l'autenticazione a più fattori o le credenziali dell'account Microsoft per eseguire i cmdlet di Azure Resource Manager con questo account.</span><span class="sxs-lookup"><span data-stu-id="12e68-122">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="12e68-123">Esempio 3: aggiungere un account che esegue l'autenticazione con le credenziali dell'entità servizio</span><span class="sxs-lookup"><span data-stu-id="12e68-123">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="12e68-124">Il primo comando ottiene le credenziali utente e le archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="12e68-124">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="12e68-125">Il secondo comando aggiunge un account di gestione risorse di Azure con le credenziali archiviate in $Credential per il tenant specificato.</span><span class="sxs-lookup"><span data-stu-id="12e68-125">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="12e68-126">Il parametro ServicePrincipal switch indica che l'account viene autenticato come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="12e68-126">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="12e68-127">Esempio 4: aggiungere un account per un tenant e un abbonamento specifici</span><span class="sxs-lookup"><span data-stu-id="12e68-127">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="12e68-128">Questo comando aggiunge un account di gestione risorse di Azure per eseguire i cmdlet per il tenant e la sottoscrizione specificati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="12e68-128">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="12e68-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12e68-129">PARAMETERS</span></span>

### <span data-ttu-id="12e68-130">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="12e68-130">-AccessToken</span></span>
<span data-ttu-id="12e68-131">Specifica un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="12e68-131">Specifies an access token.</span></span>

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

### <span data-ttu-id="12e68-132">-AccountId</span><span class="sxs-lookup"><span data-stu-id="12e68-132">-AccountId</span></span>
<span data-ttu-id="12e68-133">ID account per il token di accesso</span><span class="sxs-lookup"><span data-stu-id="12e68-133">Account Id for access token</span></span>

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

### <span data-ttu-id="12e68-134">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="12e68-134">-ApplicationId</span></span>
<span data-ttu-id="12e68-135">SPN</span><span class="sxs-lookup"><span data-stu-id="12e68-135">SPN</span></span>

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

### <span data-ttu-id="12e68-136">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="12e68-136">-CertificateThumbprint</span></span>
<span data-ttu-id="12e68-137">Hash del certificato (identificazione personale)</span><span class="sxs-lookup"><span data-stu-id="12e68-137">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="12e68-138">-ContextName</span><span class="sxs-lookup"><span data-stu-id="12e68-138">-ContextName</span></span>
<span data-ttu-id="12e68-139">Nome del contesto predefinito da questo account di accesso.</span><span class="sxs-lookup"><span data-stu-id="12e68-139">Name of the default context from this login.</span></span>  <span data-ttu-id="12e68-140">Dopo l'accesso, sarà possibile selezionare questo contesto con questo nome.</span><span class="sxs-lookup"><span data-stu-id="12e68-140">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="12e68-141">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="12e68-141">-Credential</span></span>
<span data-ttu-id="12e68-142">Specifica un oggetto PSCredential.</span><span class="sxs-lookup"><span data-stu-id="12e68-142">Specifies a PSCredential object.</span></span>
<span data-ttu-id="12e68-143">Per altre informazioni sull'oggetto PSCredential, digitare Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="12e68-143">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="12e68-144">L'oggetto PSCredential fornisce l'ID utente e la password per le credenziali di ID organizzazione oppure l'ID applicazione e il segreto per le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="12e68-144">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="12e68-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e68-145">-DefaultProfile</span></span>
<span data-ttu-id="12e68-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12e68-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12e68-147">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="12e68-147">-Environment</span></span>
<span data-ttu-id="12e68-148">Ambiente che contiene l'account per l'accesso</span><span class="sxs-lookup"><span data-stu-id="12e68-148">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="12e68-149">-Force</span><span class="sxs-lookup"><span data-stu-id="12e68-149">-Force</span></span>
<span data-ttu-id="12e68-150">Sovrascrivere il contesto esistente con lo stesso nome, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="12e68-150">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="12e68-151">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="12e68-151">-GraphAccessToken</span></span>
<span data-ttu-id="12e68-152">AccessToken per il servizio grafico</span><span class="sxs-lookup"><span data-stu-id="12e68-152">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="12e68-153">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="12e68-153">-KeyVaultAccessToken</span></span>
<span data-ttu-id="12e68-154">AccessToken per il servizio con il Vault</span><span class="sxs-lookup"><span data-stu-id="12e68-154">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="12e68-155">-Ambito</span><span class="sxs-lookup"><span data-stu-id="12e68-155">-Scope</span></span>
<span data-ttu-id="12e68-156">Determina l'ambito delle modifiche al contesto, ad esempio le modifiche apportate a wheher si applicano solo al processo cusrrent o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="12e68-156">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="12e68-157">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="12e68-157">-ServicePrincipal</span></span>
<span data-ttu-id="12e68-158">Indica che l'account viene autenticato fornendo le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="12e68-158">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e68-159">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="12e68-159">-Subscription</span></span>
<span data-ttu-id="12e68-160">Nome dell'abbonamento o ID</span><span class="sxs-lookup"><span data-stu-id="12e68-160">Subscription Name or ID</span></span>

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

### <span data-ttu-id="12e68-161">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="12e68-161">-TenantId</span></span>
<span data-ttu-id="12e68-162">Nome del tenant o ID facoltativo</span><span class="sxs-lookup"><span data-stu-id="12e68-162">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId
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

### <span data-ttu-id="12e68-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12e68-163">-Confirm</span></span>
<span data-ttu-id="12e68-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12e68-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e68-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e68-165">-WhatIf</span></span>
<span data-ttu-id="12e68-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12e68-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12e68-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12e68-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e68-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e68-168">CommonParameters</span></span>
<span data-ttu-id="12e68-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e68-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e68-170">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e68-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e68-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12e68-171">INPUTS</span></span>

### <span data-ttu-id="12e68-172">Stringa</span><span class="sxs-lookup"><span data-stu-id="12e68-172">String</span></span>
<span data-ttu-id="12e68-173">Il parametro ' SubscriptionId ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="12e68-173">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="12e68-174">Stringa</span><span class="sxs-lookup"><span data-stu-id="12e68-174">String</span></span>
<span data-ttu-id="12e68-175">Il parametro "Subscriptionname" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="12e68-175">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="12e68-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12e68-176">OUTPUTS</span></span>

### <span data-ttu-id="12e68-177">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="12e68-177">PSAzureProfile</span></span>
<span data-ttu-id="12e68-178">Informazioni su credenziali, abbonamenti, account e tenant per l'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="12e68-178">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="12e68-179">Note</span><span class="sxs-lookup"><span data-stu-id="12e68-179">NOTES</span></span>

## <span data-ttu-id="12e68-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12e68-180">RELATED LINKS</span></span>

