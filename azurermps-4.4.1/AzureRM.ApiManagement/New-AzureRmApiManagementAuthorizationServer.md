---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: cfba050b3ec6e464465d72e5f8d236f3b253fd0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517235"
---
# <span data-ttu-id="35220-101">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="35220-101">New-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="35220-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35220-102">SYNOPSIS</span></span>
<span data-ttu-id="35220-103">Crea un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="35220-103">Creates an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35220-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35220-104">SYNTAX</span></span>

```
New-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 -Name <String> [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35220-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35220-105">DESCRIPTION</span></span>
<span data-ttu-id="35220-106">Il cmdlet **New-AzureRmApiManagementAuthorizationServer** crea un server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="35220-106">The **New-AzureRmApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="35220-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35220-107">EXAMPLES</span></span>

### <span data-ttu-id="35220-108">Esempio 1: creare un server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="35220-108">Example 1: Create an authorization server</span></span>
```
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="35220-109">Questo comando crea un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="35220-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="35220-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35220-110">PARAMETERS</span></span>

### <span data-ttu-id="35220-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="35220-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="35220-112">Specifica una matrice di metodi per l'invio di un token di accesso.</span><span class="sxs-lookup"><span data-stu-id="35220-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="35220-113">psdx_paramvalues AuthorizationHeader e query.</span><span class="sxs-lookup"><span data-stu-id="35220-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="35220-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="35220-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="35220-115">Specifica l'endpoint di autorizzazione per autenticare i proprietari delle risorse e ottenere le autorizzazioni di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="35220-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="35220-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="35220-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="35220-117">Specifica una matrice di metodi di richiesta di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="35220-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="35220-118">I valori validi sono: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="35220-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="35220-119">Il valore predefinito è GET.</span><span class="sxs-lookup"><span data-stu-id="35220-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35220-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="35220-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="35220-121">Specifica una matrice di metodi di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="35220-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="35220-122">psdx_paramvalues base e corpo.</span><span class="sxs-lookup"><span data-stu-id="35220-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="35220-123">-ClientID</span><span class="sxs-lookup"><span data-stu-id="35220-123">-ClientId</span></span>
<span data-ttu-id="35220-124">Specifica l'ID client della console per sviluppatori che rappresenta l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="35220-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="35220-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="35220-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="35220-126">Specifica l'endpoint di registrazione del client per registrare i client con il server di autorizzazione e ottenere le credenziali del client.</span><span class="sxs-lookup"><span data-stu-id="35220-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="35220-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="35220-127">-ClientSecret</span></span>
<span data-ttu-id="35220-128">Specifica il segreto client della console per sviluppatori che rappresenta l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="35220-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="35220-129">-Contesto</span><span class="sxs-lookup"><span data-stu-id="35220-129">-Context</span></span>
<span data-ttu-id="35220-130">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="35220-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="35220-131">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="35220-131">-DefaultScope</span></span>
<span data-ttu-id="35220-132">Specifica l'ambito predefinito per il server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="35220-132">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="35220-133">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="35220-133">-Description</span></span>
<span data-ttu-id="35220-134">Specifica una descrizione per un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="35220-134">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="35220-135">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="35220-135">-GrantTypes</span></span>
<span data-ttu-id="35220-136">Specifica una matrice di tipi di concessione.</span><span class="sxs-lookup"><span data-stu-id="35220-136">Specifies an array of grant types.</span></span>
<span data-ttu-id="35220-137">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="35220-137">psdx_paramvalues</span></span>

- <span data-ttu-id="35220-138">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="35220-138">AuthorizationCode</span></span>
- <span data-ttu-id="35220-139">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="35220-139">ClientCredentials</span></span> 
- <span data-ttu-id="35220-140">Implicito</span><span class="sxs-lookup"><span data-stu-id="35220-140">Implicit</span></span> 
- <span data-ttu-id="35220-141">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="35220-141">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="35220-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="35220-142">-Name</span></span>
<span data-ttu-id="35220-143">Specifica il nome del server di autorizzazione da creare.</span><span class="sxs-lookup"><span data-stu-id="35220-143">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="35220-144">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="35220-144">-ResourceOwnerPassword</span></span>
<span data-ttu-id="35220-145">Specifica la password del proprietario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35220-145">Specifies the resource owner password.</span></span>
<span data-ttu-id="35220-146">Devi specificare che questo parametro è obbligatorio se ResourceOwnerPassword è specificato dal parametro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="35220-146">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="35220-147">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="35220-147">-ResourceOwnerUsername</span></span>
<span data-ttu-id="35220-148">Specifica il nome utente del proprietario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35220-148">Specifies the resource owner user name.</span></span>
<span data-ttu-id="35220-149">Devi specificare questo parametro se ResourceOwnerPassword è specificato dal parametro *GrantTypes* .</span><span class="sxs-lookup"><span data-stu-id="35220-149">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="35220-150">-ServerId</span><span class="sxs-lookup"><span data-stu-id="35220-150">-ServerId</span></span>
<span data-ttu-id="35220-151">Specifica l'ID del server di autorizzazione da creare.</span><span class="sxs-lookup"><span data-stu-id="35220-151">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="35220-152">-SupportState</span><span class="sxs-lookup"><span data-stu-id="35220-152">-SupportState</span></span>
<span data-ttu-id="35220-153">Indica se supportare il parametro di *stato* .</span><span class="sxs-lookup"><span data-stu-id="35220-153">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="35220-154">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="35220-154">-TokenBodyParameters</span></span>
<span data-ttu-id="35220-155">Specifica parametri body aggiuntivi usando il formato **Application/x-www-form-urlencoded** .</span><span class="sxs-lookup"><span data-stu-id="35220-155">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="35220-156">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="35220-156">-TokenEndpointUrl</span></span>
<span data-ttu-id="35220-157">Specifica l'URL dell'endpoint del token usato dai client per ottenere i token di accesso in Exchange per presentare le concessioni di autorizzazione o aggiornare i token.</span><span class="sxs-lookup"><span data-stu-id="35220-157">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="35220-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35220-158">-DefaultProfile</span></span>
<span data-ttu-id="35220-159">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35220-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35220-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35220-160">CommonParameters</span></span>
<span data-ttu-id="35220-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35220-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35220-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35220-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35220-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35220-163">INPUTS</span></span>

## <span data-ttu-id="35220-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35220-164">OUTPUTS</span></span>

### <span data-ttu-id="35220-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="35220-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="35220-166">Note</span><span class="sxs-lookup"><span data-stu-id="35220-166">NOTES</span></span>

## <span data-ttu-id="35220-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35220-167">RELATED LINKS</span></span>

