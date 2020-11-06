---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 76ee402fee2e18d426875340d4eaadda2cc63042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518439"
---
# <span data-ttu-id="73932-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="73932-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="73932-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73932-102">SYNOPSIS</span></span>
<span data-ttu-id="73932-103">Aggiorna la configurazione di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="73932-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73932-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73932-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73932-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73932-105">DESCRIPTION</span></span>
<span data-ttu-id="73932-106">Aggiorna la configurazione di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="73932-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="73932-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73932-107">EXAMPLES</span></span>

### <span data-ttu-id="73932-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="73932-108">Example 1</span></span>
```
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimcontext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="73932-109">Il cmdlet aggiorna il segreto client del provider di identità di Facebook;</span><span class="sxs-lookup"><span data-stu-id="73932-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="73932-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73932-110">PARAMETERS</span></span>

### <span data-ttu-id="73932-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="73932-111">-AllowedTenants</span></span>
<span data-ttu-id="73932-112">Elenco dei tenant di Azure Active Directory consentiti.</span><span class="sxs-lookup"><span data-stu-id="73932-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="73932-113">-ClientID</span><span class="sxs-lookup"><span data-stu-id="73932-113">-ClientId</span></span>
<span data-ttu-id="73932-114">ID client dell'applicazione nel provider di identità esterna.</span><span class="sxs-lookup"><span data-stu-id="73932-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="73932-115">Si tratta di ID app per Facebook login, ID client per l'account di accesso di Google, ID app per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="73932-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="73932-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="73932-116">-ClientSecret</span></span>
<span data-ttu-id="73932-117">Segreto client dell'applicazione nel provider di identità esterna, usato per autenticare la richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="73932-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="73932-118">Ad esempio, è l'app Secret per Facebook login, API Key per Google login, chiave pubblica per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="73932-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="73932-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="73932-119">-Context</span></span>
<span data-ttu-id="73932-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="73932-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="73932-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="73932-121">This parameter is required.</span></span>

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

### <span data-ttu-id="73932-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73932-122">-PassThru</span></span>
<span data-ttu-id="73932-123">Indica che questo cmdlet restituisce il  **PsApiManagementIdentityProvider** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73932-123">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


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

### <span data-ttu-id="73932-124">-Digitare</span><span class="sxs-lookup"><span data-stu-id="73932-124">-Type</span></span>
<span data-ttu-id="73932-125">Identificatore di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="73932-125">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="73932-126">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="73932-126">This parameter is required.</span></span>

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

### <span data-ttu-id="73932-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="73932-127">-Confirm</span></span>
<span data-ttu-id="73932-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73932-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73932-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73932-129">-WhatIf</span></span>
<span data-ttu-id="73932-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73932-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73932-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73932-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73932-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73932-132">-DefaultProfile</span></span>
<span data-ttu-id="73932-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73932-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73932-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73932-134">CommonParameters</span></span>
<span data-ttu-id="73932-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73932-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73932-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73932-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73932-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73932-137">INPUTS</span></span>

## <span data-ttu-id="73932-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73932-138">OUTPUTS</span></span>

### <span data-ttu-id="73932-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="73932-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="73932-140">Note</span><span class="sxs-lookup"><span data-stu-id="73932-140">NOTES</span></span>

## <span data-ttu-id="73932-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73932-141">RELATED LINKS</span></span>

[<span data-ttu-id="73932-142">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="73932-142">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="73932-143">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="73932-143">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="73932-144">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="73932-144">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
