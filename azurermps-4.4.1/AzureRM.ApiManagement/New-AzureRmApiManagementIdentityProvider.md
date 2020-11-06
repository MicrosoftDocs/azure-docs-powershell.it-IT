---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d6536c63ab3241e999c87dfb025205571c29596c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517200"
---
# <span data-ttu-id="1ae66-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1ae66-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="1ae66-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ae66-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae66-103">Crea una nuova configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="1ae66-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ae66-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ae66-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ae66-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae66-106">Crea una nuova configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="1ae66-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="1ae66-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ae66-107">EXAMPLES</span></span>

### <span data-ttu-id="1ae66-108">Esempio 1: Configura Facebook come provider di identità per gli accessi al portale per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="1ae66-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="1ae66-109">Questo comando configura l'identità di Facebook come provider di identità accettato nel portale per sviluppatori del servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1ae66-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="1ae66-110">Questo accetta come input i clienti e ClientSecret dell'app Facebook.</span><span class="sxs-lookup"><span data-stu-id="1ae66-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="1ae66-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ae66-111">PARAMETERS</span></span>

### <span data-ttu-id="1ae66-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="1ae66-112">-AllowedTenants</span></span>
<span data-ttu-id="1ae66-113">Elenco dei tenant di Azure Active Directory consentiti</span><span class="sxs-lookup"><span data-stu-id="1ae66-113">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="1ae66-114">-ClientID</span><span class="sxs-lookup"><span data-stu-id="1ae66-114">-ClientId</span></span>
<span data-ttu-id="1ae66-115">ID client dell'applicazione nel provider di identità esterna.</span><span class="sxs-lookup"><span data-stu-id="1ae66-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="1ae66-116">Si tratta di ID app per Facebook login, ID client per l'account di accesso di Google, ID app per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1ae66-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="1ae66-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="1ae66-117">-ClientSecret</span></span>
<span data-ttu-id="1ae66-118">Segreto client dell'applicazione nel provider di identità esterna, usato per autenticare la richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="1ae66-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="1ae66-119">Ad esempio, è l'app Secret per Facebook login, API Key per Google login, chiave pubblica per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1ae66-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="1ae66-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1ae66-120">-Context</span></span>
<span data-ttu-id="1ae66-121">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1ae66-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1ae66-122">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ae66-122">This parameter is required.</span></span>

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

### <span data-ttu-id="1ae66-123">-Digitare</span><span class="sxs-lookup"><span data-stu-id="1ae66-123">-Type</span></span>
<span data-ttu-id="1ae66-124">Identificatore di un provider di identità.</span><span class="sxs-lookup"><span data-stu-id="1ae66-124">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="1ae66-125">Se specificato cercherà di trovare la configurazione del provider di identità dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="1ae66-125">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="1ae66-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1ae66-126">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae66-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ae66-127">-Confirm</span></span>
<span data-ttu-id="1ae66-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ae66-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae66-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae66-129">-WhatIf</span></span>
<span data-ttu-id="1ae66-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ae66-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ae66-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ae66-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae66-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae66-132">-DefaultProfile</span></span>
<span data-ttu-id="1ae66-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae66-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ae66-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae66-134">CommonParameters</span></span>
<span data-ttu-id="1ae66-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae66-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae66-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae66-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae66-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ae66-137">INPUTS</span></span>

## <span data-ttu-id="1ae66-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ae66-138">OUTPUTS</span></span>

### <span data-ttu-id="1ae66-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1ae66-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="1ae66-140">Note</span><span class="sxs-lookup"><span data-stu-id="1ae66-140">NOTES</span></span>

## <span data-ttu-id="1ae66-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ae66-141">RELATED LINKS</span></span>

[<span data-ttu-id="1ae66-142">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1ae66-142">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="1ae66-143">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1ae66-143">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="1ae66-144">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1ae66-144">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
