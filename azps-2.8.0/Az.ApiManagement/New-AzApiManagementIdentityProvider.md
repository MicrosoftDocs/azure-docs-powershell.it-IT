---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: fc033eb1989838d8ed8e20d568f92ef20f8275e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675999"
---
# <span data-ttu-id="e6bb6-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e6bb6-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="e6bb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bb6-103">Crea una nuova configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="e6bb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6bb6-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6bb6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6bb6-105">DESCRIPTION</span></span>
<span data-ttu-id="e6bb6-106">Crea una nuova configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="e6bb6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6bb6-107">EXAMPLES</span></span>

### <span data-ttu-id="e6bb6-108">Esempio 1: Configura Facebook come provider di identità per gli accessi al portale per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="e6bb6-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="e6bb6-109">Questo comando configura l'identità di Facebook come provider di identità accettato nel portale per sviluppatori del servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="e6bb6-110">Questo accetta come input i clienti e ClientSecret dell'app Facebook.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="e6bb6-111">Esempio 2: Configura adB2C come provider di identità per gli account di accesso del portale per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="e6bb6-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
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

<span data-ttu-id="e6bb6-112">Questo comando configura l'identità di Facebook come provider di identità accettato nel portale per sviluppatori del servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="e6bb6-113">Questo accetta come input i clienti e ClientSecret dell'app Facebook.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="e6bb6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6bb6-114">PARAMETERS</span></span>

### <span data-ttu-id="e6bb6-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="e6bb6-115">-AllowedTenants</span></span>
<span data-ttu-id="e6bb6-116">Elenco dei tenant di Azure Active Directory consentiti</span><span class="sxs-lookup"><span data-stu-id="e6bb6-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="e6bb6-117">-Authority</span><span class="sxs-lookup"><span data-stu-id="e6bb6-117">-Authority</span></span>
<span data-ttu-id="e6bb6-118">OpenID Connect Discovery endpoint hostname per AAD o AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="e6bb6-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6bb6-120">-ClientID</span><span class="sxs-lookup"><span data-stu-id="e6bb6-120">-ClientId</span></span>
<span data-ttu-id="e6bb6-121">ID client dell'applicazione nel provider di identità esterna.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="e6bb6-122">Si tratta di ID app per Facebook login, ID client per l'account di accesso di Google, ID app per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="e6bb6-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="e6bb6-123">-ClientSecret</span></span>
<span data-ttu-id="e6bb6-124">Segreto client dell'applicazione nel provider di identità esterna, usato per autenticare la richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="e6bb6-125">Ad esempio, è l'app Secret per Facebook login, API Key per Google login, chiave pubblica per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="e6bb6-126">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e6bb6-126">-Context</span></span>
<span data-ttu-id="e6bb6-127">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e6bb6-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-128">This parameter is required.</span></span>

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

### <span data-ttu-id="e6bb6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6bb6-129">-DefaultProfile</span></span>
<span data-ttu-id="e6bb6-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6bb6-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="e6bb6-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="e6bb6-132">Nome criterio reimpostare la password.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-132">Password Reset Policy Name.</span></span> <span data-ttu-id="e6bb6-133">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="e6bb6-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6bb6-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="e6bb6-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="e6bb6-136">Nome criterio di modifica del profilo.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="e6bb6-137">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="e6bb6-138">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6bb6-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="e6bb6-139">-SigninPolicyName</span></span>
<span data-ttu-id="e6bb6-140">Nome criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-140">Signin Policy Name.</span></span> <span data-ttu-id="e6bb6-141">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="e6bb6-142">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6bb6-143">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="e6bb6-143">-SignupPolicyName</span></span>
<span data-ttu-id="e6bb6-144">Nome del criterio di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-144">Signup Policy Name.</span></span> <span data-ttu-id="e6bb6-145">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-145">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="e6bb6-146">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6bb6-147">-Digitare</span><span class="sxs-lookup"><span data-stu-id="e6bb6-147">-Type</span></span>
<span data-ttu-id="e6bb6-148">Identificatore di un provider di identità.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-148">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="e6bb6-149">Se specificato cercherà di trovare la configurazione del provider di identità dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-149">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="e6bb6-150">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6bb6-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6bb6-151">-Confirm</span></span>
<span data-ttu-id="e6bb6-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6bb6-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6bb6-153">-WhatIf</span></span>
<span data-ttu-id="e6bb6-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6bb6-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6bb6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bb6-156">CommonParameters</span></span>
<span data-ttu-id="e6bb6-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6bb6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bb6-158">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6bb6-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bb6-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6bb6-159">INPUTS</span></span>

### <span data-ttu-id="e6bb6-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e6bb6-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e6bb6-161">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="e6bb6-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="e6bb6-162">System. String</span><span class="sxs-lookup"><span data-stu-id="e6bb6-162">System.String</span></span>

### <span data-ttu-id="e6bb6-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="e6bb6-163">System.String[]</span></span>

## <span data-ttu-id="e6bb6-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6bb6-164">OUTPUTS</span></span>

### <span data-ttu-id="e6bb6-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e6bb6-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="e6bb6-166">Note</span><span class="sxs-lookup"><span data-stu-id="e6bb6-166">NOTES</span></span>

## <span data-ttu-id="e6bb6-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6bb6-167">RELATED LINKS</span></span>

[<span data-ttu-id="e6bb6-168">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e6bb6-168">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="e6bb6-169">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e6bb6-169">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="e6bb6-170">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e6bb6-170">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)