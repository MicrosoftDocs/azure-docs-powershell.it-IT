---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 2b66f8cbd82a1ea30554653aaaa61cabcbb589f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675998"
---
# <span data-ttu-id="ae557-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ae557-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="ae557-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae557-102">SYNOPSIS</span></span>
<span data-ttu-id="ae557-103">Crea un provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="ae557-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="ae557-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae557-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae557-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae557-105">DESCRIPTION</span></span>
<span data-ttu-id="ae557-106">Il cmdlet **New-AzApiManagementOpenIdConnectProvider** crea un provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="ae557-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="ae557-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae557-107">EXAMPLES</span></span>

### <span data-ttu-id="ae557-108">Esempio 1: creare un provider</span><span class="sxs-lookup"><span data-stu-id="ae557-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="ae557-109">Questo comando crea un **provider** OpenID Connect denominato provider contoso OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="ae557-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="ae557-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae557-110">PARAMETERS</span></span>

### <span data-ttu-id="ae557-111">-ClientID</span><span class="sxs-lookup"><span data-stu-id="ae557-111">-ClientId</span></span>
<span data-ttu-id="ae557-112">Specifica l'ID client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="ae557-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="ae557-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="ae557-113">-ClientSecret</span></span>
<span data-ttu-id="ae557-114">Specifica il segreto client della console per sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="ae557-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="ae557-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ae557-115">-Context</span></span>
<span data-ttu-id="ae557-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ae557-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ae557-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae557-117">-DefaultProfile</span></span>
<span data-ttu-id="ae557-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae557-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae557-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae557-119">-Description</span></span>
<span data-ttu-id="ae557-120">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="ae557-120">Specifies a description.</span></span>

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

### <span data-ttu-id="ae557-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="ae557-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="ae557-122">Specifica un URI di endpoint dei metadati del provider.</span><span class="sxs-lookup"><span data-stu-id="ae557-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="ae557-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae557-123">-Name</span></span>
<span data-ttu-id="ae557-124">Specifica un nome descrittivo per il provider.</span><span class="sxs-lookup"><span data-stu-id="ae557-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="ae557-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="ae557-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="ae557-126">Specifica un ID per il provider.</span><span class="sxs-lookup"><span data-stu-id="ae557-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="ae557-127">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="ae557-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="ae557-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae557-128">CommonParameters</span></span>
<span data-ttu-id="ae557-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae557-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae557-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae557-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae557-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae557-131">INPUTS</span></span>

### <span data-ttu-id="ae557-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ae557-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ae557-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ae557-133">System.String</span></span>

## <span data-ttu-id="ae557-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae557-134">OUTPUTS</span></span>

### <span data-ttu-id="ae557-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ae557-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="ae557-136">Note</span><span class="sxs-lookup"><span data-stu-id="ae557-136">NOTES</span></span>

## <span data-ttu-id="ae557-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae557-137">RELATED LINKS</span></span>

[<span data-ttu-id="ae557-138">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ae557-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="ae557-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ae557-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="ae557-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ae557-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


