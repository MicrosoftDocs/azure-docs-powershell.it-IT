---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c338cd8b2ea3ce2a464a7975ecac959bc1e52140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686654"
---
# <span data-ttu-id="b21e2-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b21e2-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b21e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b21e2-102">SYNOPSIS</span></span>
<span data-ttu-id="b21e2-103">Crea un provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="b21e2-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b21e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b21e2-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b21e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b21e2-105">DESCRIPTION</span></span>
<span data-ttu-id="b21e2-106">Il cmdlet **New-AzureRmApiManagementOpenIdConnectProvider** crea un provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="b21e2-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="b21e2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b21e2-107">EXAMPLES</span></span>

### <span data-ttu-id="b21e2-108">Esempio 1: creare un provider</span><span class="sxs-lookup"><span data-stu-id="b21e2-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="b21e2-109">Questo comando crea un **provider** OpenID Connect denominato provider contoso OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="b21e2-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="b21e2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b21e2-110">PARAMETERS</span></span>

### <span data-ttu-id="b21e2-111">-ClientID</span><span class="sxs-lookup"><span data-stu-id="b21e2-111">-ClientId</span></span>
<span data-ttu-id="b21e2-112">Specifica l'ID client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="b21e2-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="b21e2-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="b21e2-113">-ClientSecret</span></span>
<span data-ttu-id="b21e2-114">Specifica il segreto client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="b21e2-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="b21e2-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b21e2-115">-Context</span></span>
<span data-ttu-id="b21e2-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b21e2-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b21e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b21e2-117">-DefaultProfile</span></span>
<span data-ttu-id="b21e2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b21e2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b21e2-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b21e2-119">-Description</span></span>
<span data-ttu-id="b21e2-120">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="b21e2-120">Specifies a description.</span></span>

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

### <span data-ttu-id="b21e2-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="b21e2-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="b21e2-122">Specifica un URI di endpoint dei metadati del provider.</span><span class="sxs-lookup"><span data-stu-id="b21e2-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="b21e2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b21e2-123">-Name</span></span>
<span data-ttu-id="b21e2-124">Specifica un nome descrittivo per il provider.</span><span class="sxs-lookup"><span data-stu-id="b21e2-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="b21e2-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b21e2-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="b21e2-126">Specifica un ID per il provider.</span><span class="sxs-lookup"><span data-stu-id="b21e2-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="b21e2-127">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="b21e2-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="b21e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21e2-128">CommonParameters</span></span>
<span data-ttu-id="b21e2-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b21e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21e2-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b21e2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21e2-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b21e2-131">INPUTS</span></span>

### <span data-ttu-id="b21e2-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b21e2-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b21e2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b21e2-133">System.String</span></span>

## <span data-ttu-id="b21e2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b21e2-134">OUTPUTS</span></span>

### <span data-ttu-id="b21e2-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b21e2-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b21e2-136">Note</span><span class="sxs-lookup"><span data-stu-id="b21e2-136">NOTES</span></span>

## <span data-ttu-id="b21e2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b21e2-137">RELATED LINKS</span></span>

[<span data-ttu-id="b21e2-138">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b21e2-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b21e2-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b21e2-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b21e2-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b21e2-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


