---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75f6b7cee1517a3f9ae363a7e28df420e18d37ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200401"
---
# <span data-ttu-id="3b700-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="3b700-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="3b700-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b700-102">SYNOPSIS</span></span>
<span data-ttu-id="3b700-103">Crea una nuova configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="3b700-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="3b700-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b700-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b700-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b700-105">DESCRIPTION</span></span>
<span data-ttu-id="3b700-106">Crea una nuova configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="3b700-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="3b700-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b700-107">EXAMPLES</span></span>

### <span data-ttu-id="3b700-108">Esempio 1: Configura Facebook come provider di identità per gli accessi al portale per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="3b700-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="3b700-109">Questo comando configura l'identità di Facebook come provider di identità accettato nel portale per sviluppatori del servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3b700-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="3b700-110">Questo accetta come input i clienti e ClientSecret dell'app Facebook.</span><span class="sxs-lookup"><span data-stu-id="3b700-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="3b700-111">Esempio 2: Configura adB2C come provider di identità per gli account di accesso del portale per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="3b700-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $context -Type AadB2C -ClientId 6b1fc750-9e68-450c-97d2-ba6acd0fbc20 -ClientSecret "foobar" -AllowedTenants 'samirtestbc.onmicrosoft.com' -SignupPolicyName B2C_1_signup-policy

Type                     : AadB2C
ClientId                 : 6b1fc750-9e68-450c-97d2-ba6acd0fbc20
ClientSecret             : foobar
AllowedTenants           : {samirtestbc.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_signup-policy
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
Id                       : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-WestUS
ServiceName              : contoso
```

<span data-ttu-id="3b700-112">Questo comando configura l'identità di Facebook come provider di identità accettato nel portale per sviluppatori del servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3b700-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="3b700-113">Questo accetta come input i clienti e ClientSecret dell'app Facebook.</span><span class="sxs-lookup"><span data-stu-id="3b700-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="3b700-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b700-114">PARAMETERS</span></span>

### <span data-ttu-id="3b700-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="3b700-115">-AllowedTenants</span></span>
<span data-ttu-id="3b700-116">Elenco dei tenant di Azure Active Directory consentiti</span><span class="sxs-lookup"><span data-stu-id="3b700-116">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-117">-Authority</span><span class="sxs-lookup"><span data-stu-id="3b700-117">-Authority</span></span>
<span data-ttu-id="3b700-118">OpenID Connect Discovery endpoint hostname per AAD o AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="3b700-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="3b700-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3b700-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-120">-ClientID</span><span class="sxs-lookup"><span data-stu-id="3b700-120">-ClientId</span></span>
<span data-ttu-id="3b700-121">ID client dell'applicazione nel provider di identità esterna.</span><span class="sxs-lookup"><span data-stu-id="3b700-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="3b700-122">Si tratta di ID app per Facebook login, ID client per l'account di accesso di Google, ID app per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3b700-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="3b700-123">-ClientSecret</span></span>
<span data-ttu-id="3b700-124">Segreto client dell'applicazione nel provider di identità esterna, usato per autenticare la richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="3b700-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="3b700-125">Ad esempio, è l'app Secret per Facebook login, API Key per Google login, chiave pubblica per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3b700-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-126">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3b700-126">-Context</span></span>
<span data-ttu-id="3b700-127">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3b700-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3b700-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b700-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b700-129">-DefaultProfile</span></span>
<span data-ttu-id="3b700-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b700-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b700-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="3b700-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="3b700-132">Nome criterio reimpostare la password.</span><span class="sxs-lookup"><span data-stu-id="3b700-132">Password Reset Policy Name.</span></span> <span data-ttu-id="3b700-133">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="3b700-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="3b700-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3b700-134">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="3b700-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="3b700-136">Nome criterio di modifica del profilo.</span><span class="sxs-lookup"><span data-stu-id="3b700-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="3b700-137">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="3b700-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="3b700-138">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3b700-138">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="3b700-139">-SigninPolicyName</span></span>
<span data-ttu-id="3b700-140">Nome criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="3b700-140">Signin Policy Name.</span></span> <span data-ttu-id="3b700-141">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="3b700-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="3b700-142">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3b700-142">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="3b700-143">-SigninTenant</span></span>
<span data-ttu-id="3b700-144">Tenant di SignIn per eseguire l'override in AAD B2C al posto del `common` tenant</span><span class="sxs-lookup"><span data-stu-id="3b700-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="3b700-145">-SignupPolicyName</span></span>
<span data-ttu-id="3b700-146">Nome del criterio di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3b700-146">Signup Policy Name.</span></span> <span data-ttu-id="3b700-147">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="3b700-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="3b700-148">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3b700-148">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-149">-Digitare</span><span class="sxs-lookup"><span data-stu-id="3b700-149">-Type</span></span>
<span data-ttu-id="3b700-150">Identificatore di un provider di identità.</span><span class="sxs-lookup"><span data-stu-id="3b700-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="3b700-151">Se specificato cercherà di trovare la configurazione del provider di identità dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="3b700-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="3b700-152">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3b700-152">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b700-153">-Confirm</span></span>
<span data-ttu-id="3b700-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b700-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b700-155">-WhatIf</span></span>
<span data-ttu-id="3b700-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b700-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b700-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b700-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b700-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b700-158">CommonParameters</span></span>
<span data-ttu-id="3b700-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b700-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b700-160">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b700-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b700-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b700-161">INPUTS</span></span>

### <span data-ttu-id="3b700-162">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3b700-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3b700-163">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="3b700-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="3b700-164">System. String</span><span class="sxs-lookup"><span data-stu-id="3b700-164">System.String</span></span>

### <span data-ttu-id="3b700-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="3b700-165">System.String[]</span></span>

## <span data-ttu-id="3b700-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b700-166">OUTPUTS</span></span>

### <span data-ttu-id="3b700-167">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="3b700-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="3b700-168">Note</span><span class="sxs-lookup"><span data-stu-id="3b700-168">NOTES</span></span>

## <span data-ttu-id="3b700-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b700-169">RELATED LINKS</span></span>

[<span data-ttu-id="3b700-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="3b700-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="3b700-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="3b700-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="3b700-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="3b700-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
