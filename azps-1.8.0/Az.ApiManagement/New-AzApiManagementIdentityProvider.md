---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: c0730053dce60dbf556ef00f522aa463ffb26601
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685133"
---
# <span data-ttu-id="a7fe4-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a7fe4-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="a7fe4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="a7fe4-103">Crea una nuova configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="a7fe4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7fe4-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7fe4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="a7fe4-106">Crea una nuova configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="a7fe4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7fe4-107">EXAMPLES</span></span>

### <span data-ttu-id="a7fe4-108">Esempio 1: Configura Facebook come provider di identità per gli accessi al portale per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="a7fe4-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="a7fe4-109">Questo comando configura l'identità di Facebook come provider di identità accettato nel portale per sviluppatori del servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="a7fe4-110">Questo accetta come input i clienti e ClientSecret dell'app Facebook.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="a7fe4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7fe4-111">PARAMETERS</span></span>

### <span data-ttu-id="a7fe4-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="a7fe4-112">-AllowedTenants</span></span>
<span data-ttu-id="a7fe4-113">Elenco dei tenant di Azure Active Directory consentiti</span><span class="sxs-lookup"><span data-stu-id="a7fe4-113">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="a7fe4-114">-ClientID</span><span class="sxs-lookup"><span data-stu-id="a7fe4-114">-ClientId</span></span>
<span data-ttu-id="a7fe4-115">ID client dell'applicazione nel provider di identità esterna.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="a7fe4-116">Si tratta di ID app per Facebook login, ID client per l'account di accesso di Google, ID app per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="a7fe4-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="a7fe4-117">-ClientSecret</span></span>
<span data-ttu-id="a7fe4-118">Segreto client dell'applicazione nel provider di identità esterna, usato per autenticare la richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="a7fe4-119">Ad esempio, è l'app Secret per Facebook login, API Key per Google login, chiave pubblica per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="a7fe4-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a7fe4-120">-Context</span></span>
<span data-ttu-id="a7fe4-121">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a7fe4-122">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-122">This parameter is required.</span></span>

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

### <span data-ttu-id="a7fe4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7fe4-123">-DefaultProfile</span></span>
<span data-ttu-id="a7fe4-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7fe4-125">-Digitare</span><span class="sxs-lookup"><span data-stu-id="a7fe4-125">-Type</span></span>
<span data-ttu-id="a7fe4-126">Identificatore di un provider di identità.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="a7fe4-127">Se specificato cercherà di trovare la configurazione del provider di identità dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="a7fe4-128">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="a7fe4-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a7fe4-129">-Confirm</span></span>
<span data-ttu-id="a7fe4-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7fe4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7fe4-131">-WhatIf</span></span>
<span data-ttu-id="a7fe4-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7fe4-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7fe4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7fe4-134">CommonParameters</span></span>
<span data-ttu-id="a7fe4-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7fe4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7fe4-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7fe4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7fe4-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7fe4-137">INPUTS</span></span>

### <span data-ttu-id="a7fe4-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a7fe4-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a7fe4-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="a7fe4-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="a7fe4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a7fe4-140">System.String</span></span>

### <span data-ttu-id="a7fe4-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="a7fe4-141">System.String[]</span></span>

## <span data-ttu-id="a7fe4-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7fe4-142">OUTPUTS</span></span>

### <span data-ttu-id="a7fe4-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a7fe4-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="a7fe4-144">Note</span><span class="sxs-lookup"><span data-stu-id="a7fe4-144">NOTES</span></span>

## <span data-ttu-id="a7fe4-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7fe4-145">RELATED LINKS</span></span>

[<span data-ttu-id="a7fe4-146">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a7fe4-146">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="a7fe4-147">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a7fe4-147">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="a7fe4-148">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="a7fe4-148">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
