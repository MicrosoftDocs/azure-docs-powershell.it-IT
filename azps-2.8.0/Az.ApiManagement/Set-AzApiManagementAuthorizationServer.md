---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 696db55822242e124f006be233a9c8a8605a360d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675904"
---
# <span data-ttu-id="bef84-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bef84-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="bef84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bef84-102">SYNOPSIS</span></span>
<span data-ttu-id="bef84-103">Modifica un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="bef84-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="bef84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bef84-104">SYNTAX</span></span>

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

## <span data-ttu-id="bef84-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bef84-105">DESCRIPTION</span></span>
<span data-ttu-id="bef84-106">Il cmdlet **set-AzApiManagementAuthorizationServer** modifica i dettagli del server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="bef84-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="bef84-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bef84-107">EXAMPLES</span></span>

### <span data-ttu-id="bef84-108">Esempio 1: modificare un server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="bef84-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="bef84-109">Questo comando modifica il server di autorizzazione Gestione API specificato.</span><span class="sxs-lookup"><span data-stu-id="bef84-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="bef84-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bef84-110">PARAMETERS</span></span>

### <span data-ttu-id="bef84-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="bef84-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="bef84-112">Specifica una matrice di metodi per l'invio di un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="bef84-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="bef84-113">psdx_paramvalues AuthorizationHeader e query.</span><span class="sxs-lookup"><span data-stu-id="bef84-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="bef84-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="bef84-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="bef84-115">Specifica l'endpoint di autorizzazione per autenticare i proprietari delle risorse e ottenere le autorizzazioni di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="bef84-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="bef84-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="bef84-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="bef84-117">Specifica una matrice di metodi di richiesta di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="bef84-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="bef84-118">psdx_paramvalues ottenere e pubblicare.</span><span class="sxs-lookup"><span data-stu-id="bef84-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="bef84-119">Il valore predefinito è GET.</span><span class="sxs-lookup"><span data-stu-id="bef84-119">The default value is GET.</span></span>

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

### <span data-ttu-id="bef84-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="bef84-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="bef84-121">Specifica una matrice di metodi di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="bef84-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="bef84-122">psdx_paramvalues base e corpo.</span><span class="sxs-lookup"><span data-stu-id="bef84-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="bef84-123">-ClientID</span><span class="sxs-lookup"><span data-stu-id="bef84-123">-ClientId</span></span>
<span data-ttu-id="bef84-124">Specifica l'ID client della console per sviluppatori che rappresenta l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="bef84-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="bef84-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="bef84-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="bef84-126">Specifica l'endpoint di registrazione del client per registrare i client con il server di autorizzazione e ottenere le credenziali del client.</span><span class="sxs-lookup"><span data-stu-id="bef84-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="bef84-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="bef84-127">-ClientSecret</span></span>
<span data-ttu-id="bef84-128">Specifica il segreto client della console per sviluppatori che rappresenta l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="bef84-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="bef84-129">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bef84-129">-Context</span></span>
<span data-ttu-id="bef84-130">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="bef84-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bef84-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef84-131">-DefaultProfile</span></span>
<span data-ttu-id="bef84-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bef84-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bef84-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="bef84-133">-DefaultScope</span></span>
<span data-ttu-id="bef84-134">Specifica l'ambito predefinito per il server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="bef84-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="bef84-135">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="bef84-135">-Description</span></span>
<span data-ttu-id="bef84-136">Specifica una descrizione per un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="bef84-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="bef84-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="bef84-137">-GrantTypes</span></span>
<span data-ttu-id="bef84-138">Specifica una matrice di tipi di concessione.</span><span class="sxs-lookup"><span data-stu-id="bef84-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="bef84-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="bef84-139">psdx_paramvalues</span></span>
- <span data-ttu-id="bef84-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="bef84-140">AuthorizationCode</span></span>
- <span data-ttu-id="bef84-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="bef84-141">ClientCredentials</span></span> 
- <span data-ttu-id="bef84-142">Implicito</span><span class="sxs-lookup"><span data-stu-id="bef84-142">Implicit</span></span> 
- <span data-ttu-id="bef84-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="bef84-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="bef84-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="bef84-144">-Name</span></span>
<span data-ttu-id="bef84-145">Specifica il nome del server di autorizzazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="bef84-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="bef84-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bef84-146">-PassThru</span></span>
<span data-ttu-id="bef84-147">PassThru</span><span class="sxs-lookup"><span data-stu-id="bef84-147">passthru</span></span>

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

### <span data-ttu-id="bef84-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="bef84-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="bef84-149">Specifica la password del proprietario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bef84-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="bef84-150">Devi specificare questo parametro se ResourceOwnerPassword è specificato dal parametro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="bef84-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="bef84-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="bef84-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="bef84-152">Specifica il nome utente del proprietario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bef84-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="bef84-153">Devi specificare questo parametro se ResourceOwnerPassword è specificato dal parametro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="bef84-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="bef84-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="bef84-154">-ServerId</span></span>
<span data-ttu-id="bef84-155">Specifica l'ID del server di autorizzazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="bef84-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="bef84-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="bef84-156">-SupportState</span></span>
<span data-ttu-id="bef84-157">Indica se supportare il parametro di *stato* .</span><span class="sxs-lookup"><span data-stu-id="bef84-157">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="bef84-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="bef84-158">-TokenBodyParameters</span></span>
<span data-ttu-id="bef84-159">Specifica parametri body aggiuntivi usando il formato Application/x-www-form-urlencoded.</span><span class="sxs-lookup"><span data-stu-id="bef84-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="bef84-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="bef84-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="bef84-161">Specifica l'endpoint del token per i client per ottenere i token di accesso in Exchange per la presentazione di concessioni di autorizzazione o di aggiornamento dei token.</span><span class="sxs-lookup"><span data-stu-id="bef84-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="bef84-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef84-162">CommonParameters</span></span>
<span data-ttu-id="bef84-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef84-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef84-164">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bef84-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef84-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bef84-165">INPUTS</span></span>

### <span data-ttu-id="bef84-166">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bef84-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bef84-167">System. String</span><span class="sxs-lookup"><span data-stu-id="bef84-167">System.String</span></span>

### <span data-ttu-id="bef84-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="bef84-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="bef84-169">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="bef84-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="bef84-170">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="bef84-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="bef84-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bef84-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bef84-172">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bef84-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bef84-173">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="bef84-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="bef84-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bef84-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bef84-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bef84-175">OUTPUTS</span></span>

### <span data-ttu-id="bef84-176">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bef84-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="bef84-177">Note</span><span class="sxs-lookup"><span data-stu-id="bef84-177">NOTES</span></span>

## <span data-ttu-id="bef84-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bef84-178">RELATED LINKS</span></span>

[<span data-ttu-id="bef84-179">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bef84-179">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="bef84-180">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bef84-180">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="bef84-181">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bef84-181">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)


