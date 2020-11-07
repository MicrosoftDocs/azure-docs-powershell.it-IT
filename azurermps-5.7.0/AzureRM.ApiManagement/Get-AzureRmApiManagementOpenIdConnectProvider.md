---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c26fb8991acc47ab655cb47c44194ca209423a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687055"
---
# <span data-ttu-id="d58ac-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d58ac-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="d58ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d58ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d58ac-103">Ottiene i provider di connessione OpenID.</span><span class="sxs-lookup"><span data-stu-id="d58ac-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d58ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d58ac-104">SYNTAX</span></span>

### <span data-ttu-id="d58ac-105">GetAllOpenIdConnectProviders (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d58ac-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d58ac-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="d58ac-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d58ac-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="d58ac-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d58ac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d58ac-108">DESCRIPTION</span></span>
<span data-ttu-id="d58ac-109">Il cmdlet **Get-AzureRmApiManagementOpenIdConnectProvider** ottiene i provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="d58ac-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="d58ac-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d58ac-110">EXAMPLES</span></span>

### <span data-ttu-id="d58ac-111">Esempio 1: ottenere tutti i provider</span><span class="sxs-lookup"><span data-stu-id="d58ac-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="d58ac-112">Questo comando ottiene tutti i provider di connessione OpenID per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="d58ac-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="d58ac-113">Esempio 2: ottenere un provider tramite un ID</span><span class="sxs-lookup"><span data-stu-id="d58ac-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="d58ac-114">Questo comando ottiene il provider con ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="d58ac-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="d58ac-115">Esempio 3: ottenere un provider usando un nome</span><span class="sxs-lookup"><span data-stu-id="d58ac-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="d58ac-116">Questo comando ottiene il provider denominato contoso OpenID Connect provider.</span><span class="sxs-lookup"><span data-stu-id="d58ac-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="d58ac-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d58ac-117">PARAMETERS</span></span>

### <span data-ttu-id="d58ac-118">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d58ac-118">-Context</span></span>
<span data-ttu-id="d58ac-119">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d58ac-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d58ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58ac-120">-DefaultProfile</span></span>
<span data-ttu-id="d58ac-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d58ac-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d58ac-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d58ac-122">-Name</span></span>
<span data-ttu-id="d58ac-123">Specifica un nome descrittivo di un provider.</span><span class="sxs-lookup"><span data-stu-id="d58ac-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="d58ac-124">Se specifichi un nome, questo cmdlet riceve il provider.</span><span class="sxs-lookup"><span data-stu-id="d58ac-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58ac-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="d58ac-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="d58ac-126">Specifica un ID del provider rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58ac-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="d58ac-127">Se specifichi un ID, questo cmdlet riceve il provider.</span><span class="sxs-lookup"><span data-stu-id="d58ac-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58ac-128">CommonParameters</span></span>
<span data-ttu-id="d58ac-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58ac-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d58ac-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58ac-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d58ac-131">INPUTS</span></span>

### <span data-ttu-id="d58ac-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d58ac-132">None</span></span>
<span data-ttu-id="d58ac-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d58ac-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d58ac-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d58ac-134">OUTPUTS</span></span>

### <span data-ttu-id="d58ac-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d58ac-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>
<span data-ttu-id="d58ac-136">Il dettaglio del provider OpenId Connect configurato nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="d58ac-136">The detail of the OpenId connect Provider configured in API Management service.</span></span>

### <span data-ttu-id="d58ac-137">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="d58ac-137">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>
<span data-ttu-id="d58ac-138">Elenco dei provider di connessione OpenId configurati nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="d58ac-138">The list of OpenId Connect Providers configured in API Management service.</span></span>

## <span data-ttu-id="d58ac-139">Note</span><span class="sxs-lookup"><span data-stu-id="d58ac-139">NOTES</span></span>

## <span data-ttu-id="d58ac-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d58ac-140">RELATED LINKS</span></span>

[<span data-ttu-id="d58ac-141">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d58ac-141">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d58ac-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d58ac-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d58ac-143">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d58ac-143">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


