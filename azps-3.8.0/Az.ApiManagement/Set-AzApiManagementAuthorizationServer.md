---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: c8ce26ba354f25066d7139318f5e6a5ec3e23c49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021816"
---
# <span data-ttu-id="2e89d-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2e89d-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="2e89d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e89d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e89d-103">Modifica un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2e89d-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="2e89d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e89d-104">SYNTAX</span></span>

```
Set-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e89d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e89d-105">DESCRIPTION</span></span>
<span data-ttu-id="2e89d-106">Il cmdlet **set-AzApiManagementAuthorizationServer** modifica i dettagli del server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e89d-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="2e89d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e89d-107">EXAMPLES</span></span>

### <span data-ttu-id="2e89d-108">Esempio 1: modificare un server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="2e89d-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="2e89d-109">Questo comando modifica il server di autorizzazione Gestione API specificato.</span><span class="sxs-lookup"><span data-stu-id="2e89d-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="2e89d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e89d-110">PARAMETERS</span></span>

### <span data-ttu-id="2e89d-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="2e89d-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="2e89d-112">Specifica una matrice di metodi per l'invio di un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="2e89d-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="2e89d-113">psdx_paramvalues AuthorizationHeader e query.</span><span class="sxs-lookup"><span data-stu-id="2e89d-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e89d-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="2e89d-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="2e89d-115">Specifica l'endpoint di autorizzazione per autenticare i proprietari delle risorse e ottenere le autorizzazioni di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2e89d-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="2e89d-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="2e89d-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="2e89d-117">Specifica una matrice di metodi di richiesta di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2e89d-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="2e89d-118">psdx_paramvalues ottenere e pubblicare.</span><span class="sxs-lookup"><span data-stu-id="2e89d-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="2e89d-119">Il valore predefinito è GET.</span><span class="sxs-lookup"><span data-stu-id="2e89d-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Get, Post, Head, Options, Trace, Put, Patch, Delete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e89d-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="2e89d-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="2e89d-121">Specifica una matrice di metodi di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="2e89d-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="2e89d-122">psdx_paramvalues base e corpo.</span><span class="sxs-lookup"><span data-stu-id="2e89d-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e89d-123">-ClientID</span><span class="sxs-lookup"><span data-stu-id="2e89d-123">-ClientId</span></span>
<span data-ttu-id="2e89d-124">Specifica l'ID client della console per sviluppatori che rappresenta l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="2e89d-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="2e89d-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="2e89d-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="2e89d-126">Specifica l'endpoint di registrazione del client per registrare i client con il server di autorizzazione e ottenere le credenziali del client.</span><span class="sxs-lookup"><span data-stu-id="2e89d-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="2e89d-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="2e89d-127">-ClientSecret</span></span>
<span data-ttu-id="2e89d-128">Specifica il segreto client della console per sviluppatori che rappresenta l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="2e89d-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="2e89d-129">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2e89d-129">-Context</span></span>
<span data-ttu-id="2e89d-130">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2e89d-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2e89d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e89d-131">-DefaultProfile</span></span>
<span data-ttu-id="2e89d-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e89d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e89d-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="2e89d-133">-DefaultScope</span></span>
<span data-ttu-id="2e89d-134">Specifica l'ambito predefinito per il server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2e89d-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="2e89d-135">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e89d-135">-Description</span></span>
<span data-ttu-id="2e89d-136">Specifica una descrizione per un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2e89d-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="2e89d-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="2e89d-137">-GrantTypes</span></span>
<span data-ttu-id="2e89d-138">Specifica una matrice di tipi di concessione.</span><span class="sxs-lookup"><span data-stu-id="2e89d-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="2e89d-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="2e89d-139">psdx_paramvalues</span></span>
- <span data-ttu-id="2e89d-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="2e89d-140">AuthorizationCode</span></span>
- <span data-ttu-id="2e89d-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="2e89d-141">ClientCredentials</span></span> 
- <span data-ttu-id="2e89d-142">Implicito</span><span class="sxs-lookup"><span data-stu-id="2e89d-142">Implicit</span></span> 
- <span data-ttu-id="2e89d-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="2e89d-143">ResourceOwnerPassword</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e89d-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e89d-144">-Name</span></span>
<span data-ttu-id="2e89d-145">Specifica il nome del server di autorizzazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="2e89d-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="2e89d-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e89d-146">-PassThru</span></span>
<span data-ttu-id="2e89d-147">PassThru</span><span class="sxs-lookup"><span data-stu-id="2e89d-147">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e89d-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="2e89d-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="2e89d-149">Specifica la password del proprietario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2e89d-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="2e89d-150">Devi specificare questo parametro se ResourceOwnerPassword è specificato dal parametro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="2e89d-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="2e89d-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="2e89d-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="2e89d-152">Specifica il nome utente del proprietario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2e89d-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="2e89d-153">Devi specificare questo parametro se ResourceOwnerPassword è specificato dal parametro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="2e89d-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="2e89d-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="2e89d-154">-ServerId</span></span>
<span data-ttu-id="2e89d-155">Specifica l'ID del server di autorizzazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="2e89d-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="2e89d-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="2e89d-156">-SupportState</span></span>
<span data-ttu-id="2e89d-157">Indica se supportare il parametro di *stato* .</span><span class="sxs-lookup"><span data-stu-id="2e89d-157">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e89d-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="2e89d-158">-TokenBodyParameters</span></span>
<span data-ttu-id="2e89d-159">Specifica parametri body aggiuntivi usando il formato Application/x-www-form-urlencoded.</span><span class="sxs-lookup"><span data-stu-id="2e89d-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e89d-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="2e89d-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="2e89d-161">Specifica l'endpoint del token per i client per ottenere i token di accesso in Exchange per la presentazione di concessioni di autorizzazione o di aggiornamento dei token.</span><span class="sxs-lookup"><span data-stu-id="2e89d-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="2e89d-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e89d-162">CommonParameters</span></span>
<span data-ttu-id="2e89d-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e89d-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e89d-164">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e89d-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e89d-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e89d-165">INPUTS</span></span>

### <span data-ttu-id="2e89d-166">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e89d-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e89d-167">System. String</span><span class="sxs-lookup"><span data-stu-id="2e89d-167">System.String</span></span>

### <span data-ttu-id="2e89d-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="2e89d-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="2e89d-169">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="2e89d-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="2e89d-170">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="2e89d-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="2e89d-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e89d-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2e89d-172">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2e89d-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2e89d-173">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="2e89d-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="2e89d-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e89d-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2e89d-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e89d-175">OUTPUTS</span></span>

### <span data-ttu-id="2e89d-176">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2e89d-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="2e89d-177">Note</span><span class="sxs-lookup"><span data-stu-id="2e89d-177">NOTES</span></span>

## <span data-ttu-id="2e89d-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e89d-178">RELATED LINKS</span></span>

[<span data-ttu-id="2e89d-179">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2e89d-179">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="2e89d-180">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2e89d-180">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="2e89d-181">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2e89d-181">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)


