---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 088b88bcaa7f0d493552060c150e9d76a4b16c7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508447"
---
# <span data-ttu-id="f1b59-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f1b59-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f1b59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1b59-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b59-103">Crea un provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="f1b59-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1b59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1b59-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1b59-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1b59-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b59-106">Il cmdlet **New-AzureRmApiManagementOpenIdConnectProvider** crea un provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b59-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="f1b59-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1b59-107">EXAMPLES</span></span>

### <span data-ttu-id="f1b59-108">Esempio 1: creare un provider</span><span class="sxs-lookup"><span data-stu-id="f1b59-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="f1b59-109">Questo comando crea un **provider** OpenID Connect denominato provider contoso OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="f1b59-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="f1b59-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1b59-110">PARAMETERS</span></span>

### <span data-ttu-id="f1b59-111">-ClientID</span><span class="sxs-lookup"><span data-stu-id="f1b59-111">-ClientId</span></span>
<span data-ttu-id="f1b59-112">Specifica l'ID client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="f1b59-112">Specifies the client ID of the developer console.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b59-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f1b59-113">-ClientSecret</span></span>
<span data-ttu-id="f1b59-114">Specifica il segreto client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="f1b59-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="f1b59-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f1b59-115">-Context</span></span>
<span data-ttu-id="f1b59-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f1b59-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f1b59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b59-117">-DefaultProfile</span></span>
<span data-ttu-id="f1b59-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b59-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f1b59-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1b59-119">-Description</span></span>
<span data-ttu-id="f1b59-120">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="f1b59-120">Specifies a description.</span></span>

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

### <span data-ttu-id="f1b59-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="f1b59-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="f1b59-122">Specifica un URI di endpoint dei metadati del provider.</span><span class="sxs-lookup"><span data-stu-id="f1b59-122">Specifies a metadata endpoint URI of the provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b59-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1b59-123">-Name</span></span>
<span data-ttu-id="f1b59-124">Specifica un nome descrittivo per il provider.</span><span class="sxs-lookup"><span data-stu-id="f1b59-124">Specifies a friendly name for the provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b59-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="f1b59-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="f1b59-126">Specifica un ID per il provider.</span><span class="sxs-lookup"><span data-stu-id="f1b59-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="f1b59-127">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="f1b59-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="f1b59-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b59-128">CommonParameters</span></span>
<span data-ttu-id="f1b59-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b59-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b59-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b59-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b59-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1b59-131">INPUTS</span></span>

### <span data-ttu-id="f1b59-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f1b59-132">None</span></span>
<span data-ttu-id="f1b59-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f1b59-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1b59-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1b59-134">OUTPUTS</span></span>

### <span data-ttu-id="f1b59-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f1b59-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f1b59-136">Note</span><span class="sxs-lookup"><span data-stu-id="f1b59-136">NOTES</span></span>

## <span data-ttu-id="f1b59-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1b59-137">RELATED LINKS</span></span>

[<span data-ttu-id="f1b59-138">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f1b59-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f1b59-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f1b59-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f1b59-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f1b59-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)

