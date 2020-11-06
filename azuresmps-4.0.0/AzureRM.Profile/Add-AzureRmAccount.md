---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 533982757e4ea953c1f5d07ba67ac70af2161a10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491041"
---
# <span data-ttu-id="b0922-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="b0922-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="b0922-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0922-102">SYNOPSIS</span></span>
<span data-ttu-id="b0922-103">Aggiunge un account autenticato da usare per le richieste di cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b0922-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="b0922-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0922-104">SYNTAX</span></span>

### <span data-ttu-id="b0922-105">UserWithSubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0922-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0922-106">UserWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b0922-106">UserWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0922-107">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0922-107">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0922-108">ServicePrincipalWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b0922-108">ServicePrincipalWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0922-109">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0922-109">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0922-110">ServicePrincipalCertificateWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b0922-110">ServicePrincipalCertificateWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0922-111">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0922-111">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0922-112">AccessTokenWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b0922-112">AccessTokenWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0922-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0922-113">DESCRIPTION</span></span>
<span data-ttu-id="b0922-114">Il cmdlet Add-AzureRmAcccount aggiunge un account Azure autenticato da usare per le richieste di cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b0922-114">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="b0922-115">Puoi usare questo account autenticato solo con i cmdlet di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0922-115">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="b0922-116">Per aggiungere un account autenticato da usare con i cmdlet di gestione dei servizi, usare il cmdlet Add-AzureAccount o Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="b0922-116">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="b0922-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0922-117">EXAMPLES</span></span>

### <span data-ttu-id="b0922-118">Esempio 1: aggiungere un account che richiede l'accesso interattivo</span><span class="sxs-lookup"><span data-stu-id="b0922-118">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="b0922-119">Questo comando aggiunge un account di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0922-119">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="b0922-120">Per eseguire i cmdlet di Azure Resource Manager con questo account, è necessario specificare le credenziali dell'account Microsoft o dell'ID organizzazione alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="b0922-120">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="b0922-121">Se per le credenziali è abilitata l'autenticazione a più fattori, è necessario eseguire l'accesso usando l'opzione interattiva o usare l'autenticazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="b0922-121">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="b0922-122">Esempio 2: aggiungere un account che esegue l'autenticazione con le credenziali dell'ID organizzazione</span><span class="sxs-lookup"><span data-stu-id="b0922-122">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="b0922-123">Il primo comando ottiene le credenziali utente e le archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="b0922-123">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="b0922-124">Il secondo comando aggiunge un account di gestione risorse di Azure con le credenziali in $Credential.</span><span class="sxs-lookup"><span data-stu-id="b0922-124">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="b0922-125">Questo account esegue l'autenticazione con Azure Resource Manager usando le credenziali dell'ID organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b0922-125">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="b0922-126">Non è possibile usare l'autenticazione a più fattori o le credenziali dell'account Microsoft per eseguire i cmdlet di Azure Resource Manager con questo account.</span><span class="sxs-lookup"><span data-stu-id="b0922-126">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="b0922-127">Esempio 3: aggiungere un account che esegue l'autenticazione con le credenziali dell'entità servizio</span><span class="sxs-lookup"><span data-stu-id="b0922-127">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="b0922-128">Il primo comando ottiene le credenziali utente e le archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="b0922-128">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="b0922-129">Il secondo comando aggiunge un account di gestione risorse di Azure con le credenziali archiviate in $Credential per il tenant specificato.</span><span class="sxs-lookup"><span data-stu-id="b0922-129">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="b0922-130">Il parametro ServicePrincipal switch indica che l'account viene autenticato come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="b0922-130">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="b0922-131">Esempio 4: aggiungere un account per un tenant e un abbonamento specifici</span><span class="sxs-lookup"><span data-stu-id="b0922-131">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="b0922-132">Questo comando aggiunge un account di gestione risorse di Azure per eseguire i cmdlet per il tenant e la sottoscrizione specificati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b0922-132">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="b0922-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0922-133">PARAMETERS</span></span>

### <span data-ttu-id="b0922-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="b0922-134">-AccessToken</span></span>
<span data-ttu-id="b0922-135">Specifica un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="b0922-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0922-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="b0922-136">-AccountId</span></span>
<span data-ttu-id="b0922-137">ID account per il token di accesso</span><span class="sxs-lookup"><span data-stu-id="b0922-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0922-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b0922-138">-ApplicationId</span></span>
<span data-ttu-id="b0922-139">SPN</span><span class="sxs-lookup"><span data-stu-id="b0922-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0922-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b0922-140">-CertificateThumbprint</span></span>
<span data-ttu-id="b0922-141">Hash del certificato (identificazione personale)</span><span class="sxs-lookup"><span data-stu-id="b0922-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0922-142">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="b0922-142">-Credential</span></span>
<span data-ttu-id="b0922-143">Specifica un oggetto PSCredential.</span><span class="sxs-lookup"><span data-stu-id="b0922-143">Specifies a PSCredential object.</span></span>
<span data-ttu-id="b0922-144">Per altre informazioni sull'oggetto PSCredential, digitare Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="b0922-144">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="b0922-145">L'oggetto PSCredential fornisce l'ID utente e la password per le credenziali di ID organizzazione oppure l'ID applicazione e il segreto per le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="b0922-145">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0922-146">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="b0922-146">-Environment</span></span>
<span data-ttu-id="b0922-147">Ambiente che contiene l'account per l'accesso</span><span class="sxs-lookup"><span data-stu-id="b0922-147">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="b0922-148">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b0922-148">-ServicePrincipal</span></span>
<span data-ttu-id="b0922-149">Indica che l'account viene autenticato fornendo le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="b0922-149">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0922-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0922-150">-SubscriptionId</span></span>
<span data-ttu-id="b0922-151">Specifica l'ID dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b0922-151">Specifies the ID of the subscription.</span></span>
<span data-ttu-id="b0922-152">Se non specifichi questo parametro, viene usato il primo abbonamento dall'elenco di abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="b0922-152">If you do not specify this parameter, the first subscription from the subscription list is used.</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0922-153">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="b0922-153">-SubscriptionName</span></span>
<span data-ttu-id="b0922-154">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="b0922-154">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionName, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionName, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0922-155">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="b0922-155">-TenantId</span></span>
<span data-ttu-id="b0922-156">Nome del tenant o ID facoltativo</span><span class="sxs-lookup"><span data-stu-id="b0922-156">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName, AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0922-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0922-157">-Confirm</span></span>
<span data-ttu-id="b0922-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0922-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0922-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0922-159">-WhatIf</span></span>
<span data-ttu-id="b0922-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0922-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0922-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0922-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0922-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0922-162">CommonParameters</span></span>
<span data-ttu-id="b0922-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0922-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0922-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0922-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0922-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0922-165">INPUTS</span></span>

## <span data-ttu-id="b0922-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0922-166">OUTPUTS</span></span>

### <span data-ttu-id="b0922-167">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="b0922-167">PSAzureProfile</span></span>

## <span data-ttu-id="b0922-168">Note</span><span class="sxs-lookup"><span data-stu-id="b0922-168">NOTES</span></span>

## <span data-ttu-id="b0922-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0922-169">RELATED LINKS</span></span>

