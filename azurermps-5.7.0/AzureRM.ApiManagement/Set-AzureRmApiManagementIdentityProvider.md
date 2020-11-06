---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e45ec5a3d49bf82ab945a3ef3b41362a1e1e2bd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521470"
---
# <span data-ttu-id="d2c9c-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d2c9c-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="d2c9c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c9c-103">Aggiorna la configurazione di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2c9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2c9c-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2c9c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c9c-106">Aggiorna la configurazione di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="d2c9c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2c9c-107">EXAMPLES</span></span>

### <span data-ttu-id="d2c9c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d2c9c-108">Example 1</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="d2c9c-109">Il cmdlet aggiorna il segreto client del provider di identità di Facebook;</span><span class="sxs-lookup"><span data-stu-id="d2c9c-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="d2c9c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2c9c-110">PARAMETERS</span></span>

### <span data-ttu-id="d2c9c-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="d2c9c-111">-AllowedTenants</span></span>
<span data-ttu-id="d2c9c-112">Elenco dei tenant di Azure Active Directory consentiti.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-112">List of allowed Azure Active Directory Tenants.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9c-113">-ClientID</span><span class="sxs-lookup"><span data-stu-id="d2c9c-113">-ClientId</span></span>
<span data-ttu-id="d2c9c-114">ID client dell'applicazione nel provider di identità esterna.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="d2c9c-115">Si tratta di ID app per Facebook login, ID client per l'account di accesso di Google, ID app per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9c-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="d2c9c-116">-ClientSecret</span></span>
<span data-ttu-id="d2c9c-117">Segreto client dell'applicazione nel provider di identità esterna, usato per autenticare la richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="d2c9c-118">Ad esempio, è l'app Secret per Facebook login, API Key per Google login, chiave pubblica per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9c-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d2c9c-119">-Context</span></span>
<span data-ttu-id="d2c9c-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d2c9c-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-121">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c9c-122">-DefaultProfile</span></span>
<span data-ttu-id="d2c9c-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2c9c-124">-PassThru</span></span>
<span data-ttu-id="d2c9c-125">Indica che questo cmdlet restituisce il  **PsApiManagementIdentityProvider** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9c-126">-Digitare</span><span class="sxs-lookup"><span data-stu-id="d2c9c-126">-Type</span></span>
<span data-ttu-id="d2c9c-127">Identificatore di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="d2c9c-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-128">This parameter is required.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9c-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2c9c-129">-Confirm</span></span>
<span data-ttu-id="d2c9c-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c9c-131">-WhatIf</span></span>
<span data-ttu-id="d2c9c-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2c9c-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c9c-134">CommonParameters</span></span>
<span data-ttu-id="d2c9c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c9c-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c9c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c9c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2c9c-137">INPUTS</span></span>

### <span data-ttu-id="d2c9c-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d2c9c-138">None</span></span>
<span data-ttu-id="d2c9c-139">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d2c9c-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2c9c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2c9c-140">OUTPUTS</span></span>

### <span data-ttu-id="d2c9c-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d2c9c-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="d2c9c-142">Note</span><span class="sxs-lookup"><span data-stu-id="d2c9c-142">NOTES</span></span>

## <span data-ttu-id="d2c9c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2c9c-143">RELATED LINKS</span></span>

[<span data-ttu-id="d2c9c-144">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d2c9c-144">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="d2c9c-145">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d2c9c-145">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="d2c9c-146">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d2c9c-146">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
