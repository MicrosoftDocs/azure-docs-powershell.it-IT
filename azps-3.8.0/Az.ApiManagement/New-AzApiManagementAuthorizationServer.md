---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 46530ce5fd72ea01abdd258feb9f7049bf9670a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020218"
---
# <span data-ttu-id="d96ce-101">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d96ce-101">New-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="d96ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d96ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d96ce-103">Crea un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="d96ce-103">Creates an authorization server.</span></span>

## <span data-ttu-id="d96ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d96ce-104">SYNTAX</span></span>

```
New-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>] -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d96ce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d96ce-105">DESCRIPTION</span></span>
<span data-ttu-id="d96ce-106">Il cmdlet **New-AzApiManagementAuthorizationServer** crea un server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="d96ce-106">The **New-AzApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="d96ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d96ce-107">EXAMPLES</span></span>

### <span data-ttu-id="d96ce-108">Esempio 1: creare un server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="d96ce-108">Example 1: Create an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="d96ce-109">Questo comando crea un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="d96ce-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="d96ce-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d96ce-110">PARAMETERS</span></span>

### <span data-ttu-id="d96ce-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="d96ce-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="d96ce-112">Specifica una matrice di metodi per l'invio di un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="d96ce-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="d96ce-113">psdx_paramvalues AuthorizationHeader e query.</span><span class="sxs-lookup"><span data-stu-id="d96ce-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="d96ce-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="d96ce-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="d96ce-115">Specifica l'endpoint di autorizzazione per autenticare i proprietari delle risorse e ottenere le autorizzazioni di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="d96ce-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="d96ce-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="d96ce-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="d96ce-117">Specifica una matrice di metodi di richiesta di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="d96ce-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="d96ce-118">I valori validi sono: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="d96ce-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="d96ce-119">Il valore predefinito è GET.</span><span class="sxs-lookup"><span data-stu-id="d96ce-119">The default value is GET.</span></span>

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

### <span data-ttu-id="d96ce-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="d96ce-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="d96ce-121">Specifica una matrice di metodi di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="d96ce-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="d96ce-122">psdx_paramvalues base e corpo.</span><span class="sxs-lookup"><span data-stu-id="d96ce-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="d96ce-123">-ClientID</span><span class="sxs-lookup"><span data-stu-id="d96ce-123">-ClientId</span></span>
<span data-ttu-id="d96ce-124">Specifica l'ID client della console per sviluppatori che rappresenta l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="d96ce-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="d96ce-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="d96ce-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="d96ce-126">Specifica l'endpoint di registrazione del client per registrare i client con il server di autorizzazione e ottenere le credenziali del client.</span><span class="sxs-lookup"><span data-stu-id="d96ce-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="d96ce-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="d96ce-127">-ClientSecret</span></span>
<span data-ttu-id="d96ce-128">Specifica il segreto client della console per sviluppatori che rappresenta l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="d96ce-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="d96ce-129">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d96ce-129">-Context</span></span>
<span data-ttu-id="d96ce-130">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d96ce-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d96ce-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96ce-131">-DefaultProfile</span></span>
<span data-ttu-id="d96ce-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d96ce-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d96ce-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="d96ce-133">-DefaultScope</span></span>
<span data-ttu-id="d96ce-134">Specifica l'ambito predefinito per il server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="d96ce-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="d96ce-135">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d96ce-135">-Description</span></span>
<span data-ttu-id="d96ce-136">Specifica una descrizione per un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="d96ce-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="d96ce-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="d96ce-137">-GrantTypes</span></span>
<span data-ttu-id="d96ce-138">Specifica una matrice di tipi di concessione.</span><span class="sxs-lookup"><span data-stu-id="d96ce-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="d96ce-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="d96ce-139">psdx_paramvalues</span></span>
- <span data-ttu-id="d96ce-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="d96ce-140">AuthorizationCode</span></span>
- <span data-ttu-id="d96ce-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="d96ce-141">ClientCredentials</span></span> 
- <span data-ttu-id="d96ce-142">Implicito</span><span class="sxs-lookup"><span data-stu-id="d96ce-142">Implicit</span></span> 
- <span data-ttu-id="d96ce-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="d96ce-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="d96ce-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="d96ce-144">-Name</span></span>
<span data-ttu-id="d96ce-145">Specifica il nome del server di autorizzazione da creare.</span><span class="sxs-lookup"><span data-stu-id="d96ce-145">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="d96ce-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="d96ce-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="d96ce-147">Specifica la password del proprietario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d96ce-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="d96ce-148">Devi specificare che questo parametro è obbligatorio se ResourceOwnerPassword è specificato dal parametro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="d96ce-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="d96ce-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="d96ce-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="d96ce-150">Specifica il nome utente del proprietario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d96ce-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="d96ce-151">Devi specificare questo parametro se ResourceOwnerPassword è specificato dal parametro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="d96ce-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="d96ce-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="d96ce-152">-ServerId</span></span>
<span data-ttu-id="d96ce-153">Specifica l'ID del server di autorizzazione da creare.</span><span class="sxs-lookup"><span data-stu-id="d96ce-153">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="d96ce-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="d96ce-154">-SupportState</span></span>
<span data-ttu-id="d96ce-155">Indica se supportare il parametro di *stato* .</span><span class="sxs-lookup"><span data-stu-id="d96ce-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="d96ce-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="d96ce-156">-TokenBodyParameters</span></span>
<span data-ttu-id="d96ce-157">Specifica parametri body aggiuntivi usando il formato **Application/x-www-form-urlencoded** .</span><span class="sxs-lookup"><span data-stu-id="d96ce-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="d96ce-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="d96ce-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="d96ce-159">Specifica l'URL dell'endpoint del token usato dai client per ottenere i token di accesso in Exchange per presentare le concessioni di autorizzazione o aggiornare i token.</span><span class="sxs-lookup"><span data-stu-id="d96ce-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="d96ce-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96ce-160">CommonParameters</span></span>
<span data-ttu-id="d96ce-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96ce-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96ce-162">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d96ce-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96ce-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d96ce-163">INPUTS</span></span>

### <span data-ttu-id="d96ce-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d96ce-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d96ce-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d96ce-165">System.String</span></span>

### <span data-ttu-id="d96ce-166">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="d96ce-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="d96ce-167">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="d96ce-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="d96ce-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="d96ce-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="d96ce-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d96ce-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d96ce-170">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d96ce-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d96ce-171">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="d96ce-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

## <span data-ttu-id="d96ce-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d96ce-172">OUTPUTS</span></span>

### <span data-ttu-id="d96ce-173">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d96ce-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="d96ce-174">Note</span><span class="sxs-lookup"><span data-stu-id="d96ce-174">NOTES</span></span>

## <span data-ttu-id="d96ce-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d96ce-175">RELATED LINKS</span></span>
