---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 37144ab119eba4f19c3b34b2b32dfd28ff305677
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020181"
---
# <span data-ttu-id="d960c-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d960c-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="d960c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d960c-102">SYNOPSIS</span></span>
<span data-ttu-id="d960c-103">Crea un provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="d960c-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="d960c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d960c-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d960c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d960c-105">DESCRIPTION</span></span>
<span data-ttu-id="d960c-106">Il cmdlet **New-AzApiManagementOpenIdConnectProvider** crea un provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="d960c-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="d960c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d960c-107">EXAMPLES</span></span>

### <span data-ttu-id="d960c-108">Esempio 1: creare un provider</span><span class="sxs-lookup"><span data-stu-id="d960c-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="d960c-109">Questo comando crea un **provider** OpenID Connect denominato provider contoso OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="d960c-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="d960c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d960c-110">PARAMETERS</span></span>

### <span data-ttu-id="d960c-111">-ClientID</span><span class="sxs-lookup"><span data-stu-id="d960c-111">-ClientId</span></span>
<span data-ttu-id="d960c-112">Specifica l'ID client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="d960c-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="d960c-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="d960c-113">-ClientSecret</span></span>
<span data-ttu-id="d960c-114">Specifica il segreto client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="d960c-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="d960c-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d960c-115">-Context</span></span>
<span data-ttu-id="d960c-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d960c-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d960c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d960c-117">-DefaultProfile</span></span>
<span data-ttu-id="d960c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d960c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d960c-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d960c-119">-Description</span></span>
<span data-ttu-id="d960c-120">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="d960c-120">Specifies a description.</span></span>

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

### <span data-ttu-id="d960c-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="d960c-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="d960c-122">Specifica un URI di endpoint dei metadati del provider.</span><span class="sxs-lookup"><span data-stu-id="d960c-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="d960c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d960c-123">-Name</span></span>
<span data-ttu-id="d960c-124">Specifica un nome descrittivo per il provider.</span><span class="sxs-lookup"><span data-stu-id="d960c-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="d960c-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="d960c-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="d960c-126">Specifica un ID per il provider.</span><span class="sxs-lookup"><span data-stu-id="d960c-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="d960c-127">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="d960c-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="d960c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d960c-128">CommonParameters</span></span>
<span data-ttu-id="d960c-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d960c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d960c-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d960c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d960c-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d960c-131">INPUTS</span></span>

### <span data-ttu-id="d960c-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d960c-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d960c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d960c-133">System.String</span></span>

## <span data-ttu-id="d960c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d960c-134">OUTPUTS</span></span>

### <span data-ttu-id="d960c-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d960c-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="d960c-136">Note</span><span class="sxs-lookup"><span data-stu-id="d960c-136">NOTES</span></span>

## <span data-ttu-id="d960c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d960c-137">RELATED LINKS</span></span>

[<span data-ttu-id="d960c-138">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d960c-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d960c-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d960c-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d960c-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d960c-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


