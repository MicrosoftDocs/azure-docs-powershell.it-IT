---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192518"
---
# <span data-ttu-id="dabf3-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dabf3-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="dabf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dabf3-102">SYNOPSIS</span></span>
<span data-ttu-id="dabf3-103">Ottiene provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="dabf3-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="dabf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dabf3-104">SYNTAX</span></span>

### <span data-ttu-id="dabf3-105">GetAllOpenIdConnectProviders (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dabf3-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dabf3-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="dabf3-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dabf3-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="dabf3-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dabf3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dabf3-108">DESCRIPTION</span></span>
<span data-ttu-id="dabf3-109">Il cmdlet **Get-AzApiManagementOpenIdConnectProvider** ottiene i provider OpenID Connect in Gestione API Azure.</span><span class="sxs-lookup"><span data-stu-id="dabf3-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="dabf3-110">ClientSecret non verrà incluso nei dettagli dei risultati.</span><span class="sxs-lookup"><span data-stu-id="dabf3-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="dabf3-111">Per ottenere il segreto client, usare **Get-AzApiManagementOpenIdConnectProviderClientSecret.**</span><span class="sxs-lookup"><span data-stu-id="dabf3-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="dabf3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dabf3-112">EXAMPLES</span></span>

### <span data-ttu-id="dabf3-113">Esempio 1: Ottenere tutti i provider</span><span class="sxs-lookup"><span data-stu-id="dabf3-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="dabf3-114">Questo comando recupera tutti i provider OpenID Connect per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="dabf3-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="dabf3-115">Esempio 2: Ottenere un provider usando un ID</span><span class="sxs-lookup"><span data-stu-id="dabf3-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="dabf3-116">Questo comando ottiene il provider con ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="dabf3-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="dabf3-117">Esempio 3: Ottenere un provider usando un nome</span><span class="sxs-lookup"><span data-stu-id="dabf3-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="dabf3-118">Questo comando ottiene il provider denominato Contoso OpenID Connect Provider.</span><span class="sxs-lookup"><span data-stu-id="dabf3-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="dabf3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dabf3-119">PARAMETERS</span></span>

### <span data-ttu-id="dabf3-120">-Context</span><span class="sxs-lookup"><span data-stu-id="dabf3-120">-Context</span></span>
<span data-ttu-id="dabf3-121">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="dabf3-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dabf3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabf3-122">-DefaultProfile</span></span>
<span data-ttu-id="dabf3-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dabf3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dabf3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dabf3-124">-Name</span></span>
<span data-ttu-id="dabf3-125">Specifica un nome descrittivo di un provider.</span><span class="sxs-lookup"><span data-stu-id="dabf3-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="dabf3-126">Se si specifica un nome, questo cmdlet ottiene tale provider.</span><span class="sxs-lookup"><span data-stu-id="dabf3-126">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabf3-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="dabf3-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="dabf3-128">Specifica un ID del provider rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dabf3-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="dabf3-129">Se si specifica un ID, questo cmdlet ottiene tale provider.</span><span class="sxs-lookup"><span data-stu-id="dabf3-129">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabf3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabf3-130">CommonParameters</span></span>
<span data-ttu-id="dabf3-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dabf3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabf3-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dabf3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabf3-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="dabf3-133">INPUTS</span></span>

### <span data-ttu-id="dabf3-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dabf3-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dabf3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="dabf3-135">System.String</span></span>

## <span data-ttu-id="dabf3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dabf3-136">OUTPUTS</span></span>

### <span data-ttu-id="dabf3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dabf3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="dabf3-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="dabf3-138">NOTES</span></span>

## <span data-ttu-id="dabf3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dabf3-139">RELATED LINKS</span></span>

[<span data-ttu-id="dabf3-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dabf3-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="dabf3-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dabf3-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="dabf3-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dabf3-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


