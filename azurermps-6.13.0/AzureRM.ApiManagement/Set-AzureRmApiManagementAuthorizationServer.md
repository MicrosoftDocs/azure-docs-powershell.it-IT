---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 684c68b1af37ae1ae64d8ce3d9ea5b35ec008a1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517671"
---
# <span data-ttu-id="ee3f7-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ee3f7-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="ee3f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ee3f7-103">Modifica un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee3f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee3f7-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee3f7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee3f7-105">DESCRIPTION</span></span>
<span data-ttu-id="ee3f7-106">Il cmdlet **set-AzureRmApiManagementAuthorizationServer** modifica i dettagli del server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="ee3f7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee3f7-107">EXAMPLES</span></span>

### <span data-ttu-id="ee3f7-108">Esempio 1: modificare un server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="ee3f7-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="ee3f7-109">Questo comando modifica il server di autorizzazione Gestione API specificato.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="ee3f7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee3f7-110">PARAMETERS</span></span>

### <span data-ttu-id="ee3f7-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="ee3f7-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="ee3f7-112">Specifica una matrice di metodi per l'invio di un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="ee3f7-113">psdx_paramvalues AuthorizationHeader e query.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="ee3f7-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="ee3f7-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="ee3f7-115">Specifica l'endpoint di autorizzazione per autenticare i proprietari delle risorse e ottenere le autorizzazioni di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="ee3f7-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="ee3f7-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="ee3f7-117">Specifica una matrice di metodi di richiesta di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="ee3f7-118">psdx_paramvalues ottenere e pubblicare.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="ee3f7-119">Il valore predefinito è GET.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-119">The default value is GET.</span></span>

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

### <span data-ttu-id="ee3f7-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="ee3f7-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="ee3f7-121">Specifica una matrice di metodi di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="ee3f7-122">psdx_paramvalues base e corpo.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="ee3f7-123">-ClientID</span><span class="sxs-lookup"><span data-stu-id="ee3f7-123">-ClientId</span></span>
<span data-ttu-id="ee3f7-124">Specifica l'ID client della console per sviluppatori che rappresenta l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="ee3f7-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="ee3f7-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="ee3f7-126">Specifica l'endpoint di registrazione del client per registrare i client con il server di autorizzazione e ottenere le credenziali del client.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="ee3f7-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="ee3f7-127">-ClientSecret</span></span>
<span data-ttu-id="ee3f7-128">Specifica il segreto client della console per sviluppatori che rappresenta l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="ee3f7-129">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ee3f7-129">-Context</span></span>
<span data-ttu-id="ee3f7-130">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ee3f7-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee3f7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee3f7-131">-DefaultProfile</span></span>
<span data-ttu-id="ee3f7-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee3f7-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="ee3f7-133">-DefaultScope</span></span>
<span data-ttu-id="ee3f7-134">Specifica l'ambito predefinito per il server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="ee3f7-135">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee3f7-135">-Description</span></span>
<span data-ttu-id="ee3f7-136">Specifica una descrizione per un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="ee3f7-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="ee3f7-137">-GrantTypes</span></span>
<span data-ttu-id="ee3f7-138">Specifica una matrice di tipi di concessione.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="ee3f7-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="ee3f7-139">psdx_paramvalues</span></span>
- <span data-ttu-id="ee3f7-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="ee3f7-140">AuthorizationCode</span></span>
- <span data-ttu-id="ee3f7-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="ee3f7-141">ClientCredentials</span></span> 
- <span data-ttu-id="ee3f7-142">Implicito</span><span class="sxs-lookup"><span data-stu-id="ee3f7-142">Implicit</span></span> 
- <span data-ttu-id="ee3f7-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="ee3f7-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="ee3f7-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee3f7-144">-Name</span></span>
<span data-ttu-id="ee3f7-145">Specifica il nome del server di autorizzazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="ee3f7-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee3f7-146">-PassThru</span></span>
<span data-ttu-id="ee3f7-147">PassThru</span><span class="sxs-lookup"><span data-stu-id="ee3f7-147">passthru</span></span>

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

### <span data-ttu-id="ee3f7-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="ee3f7-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="ee3f7-149">Specifica la password del proprietario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="ee3f7-150">Devi specificare questo parametro se ResourceOwnerPassword è specificato dal parametro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="ee3f7-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="ee3f7-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="ee3f7-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="ee3f7-152">Specifica il nome utente del proprietario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="ee3f7-153">Devi specificare questo parametro se ResourceOwnerPassword è specificato dal parametro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="ee3f7-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="ee3f7-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="ee3f7-154">-ServerId</span></span>
<span data-ttu-id="ee3f7-155">Specifica l'ID del server di autorizzazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="ee3f7-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="ee3f7-156">-SupportState</span></span>
<span data-ttu-id="ee3f7-157">Indica se supportare il parametro di *stato* .</span><span class="sxs-lookup"><span data-stu-id="ee3f7-157">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="ee3f7-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="ee3f7-158">-TokenBodyParameters</span></span>
<span data-ttu-id="ee3f7-159">Specifica parametri body aggiuntivi usando il formato Application/x-www-form-urlencoded.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="ee3f7-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="ee3f7-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="ee3f7-161">Specifica l'endpoint del token per i client per ottenere i token di accesso in Exchange per la presentazione di concessioni di autorizzazione o di aggiornamento dei token.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="ee3f7-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee3f7-162">CommonParameters</span></span>
<span data-ttu-id="ee3f7-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee3f7-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee3f7-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee3f7-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee3f7-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee3f7-165">INPUTS</span></span>

### <span data-ttu-id="ee3f7-166">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ee3f7-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ee3f7-167">System. String</span><span class="sxs-lookup"><span data-stu-id="ee3f7-167">System.String</span></span>

### <span data-ttu-id="ee3f7-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="ee3f7-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="ee3f7-169">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="ee3f7-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="ee3f7-170">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="ee3f7-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="ee3f7-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ee3f7-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ee3f7-172">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ee3f7-172">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ee3f7-173">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="ee3f7-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="ee3f7-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ee3f7-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ee3f7-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee3f7-175">OUTPUTS</span></span>

### <span data-ttu-id="ee3f7-176">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="ee3f7-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="ee3f7-177">Note</span><span class="sxs-lookup"><span data-stu-id="ee3f7-177">NOTES</span></span>

## <span data-ttu-id="ee3f7-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee3f7-178">RELATED LINKS</span></span>

[<span data-ttu-id="ee3f7-179">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ee3f7-179">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="ee3f7-180">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ee3f7-180">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="ee3f7-181">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ee3f7-181">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)


