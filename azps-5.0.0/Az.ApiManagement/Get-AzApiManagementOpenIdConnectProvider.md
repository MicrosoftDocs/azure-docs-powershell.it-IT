---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311629"
---
# <span data-ttu-id="c09ec-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c09ec-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="c09ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c09ec-102">SYNOPSIS</span></span>
<span data-ttu-id="c09ec-103">Ottiene i provider di connessione OpenID.</span><span class="sxs-lookup"><span data-stu-id="c09ec-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="c09ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c09ec-104">SYNTAX</span></span>

### <span data-ttu-id="c09ec-105">GetAllOpenIdConnectProviders (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c09ec-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c09ec-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="c09ec-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c09ec-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="c09ec-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c09ec-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c09ec-108">DESCRIPTION</span></span>
<span data-ttu-id="c09ec-109">Il cmdlet **Get-AzApiManagementOpenIdConnectProvider** ottiene i provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="c09ec-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="c09ec-110">ClientSecret non verrà incluso nei dettagli dei risultati.</span><span class="sxs-lookup"><span data-stu-id="c09ec-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="c09ec-111">Per ottenere il segreto del client, USA **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="c09ec-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="c09ec-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c09ec-112">EXAMPLES</span></span>

### <span data-ttu-id="c09ec-113">Esempio 1: ottenere tutti i provider</span><span class="sxs-lookup"><span data-stu-id="c09ec-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="c09ec-114">Questo comando ottiene tutti i provider di connessione OpenID per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="c09ec-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="c09ec-115">Esempio 2: ottenere un provider tramite un ID</span><span class="sxs-lookup"><span data-stu-id="c09ec-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="c09ec-116">Questo comando ottiene il provider con ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="c09ec-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="c09ec-117">Esempio 3: ottenere un provider usando un nome</span><span class="sxs-lookup"><span data-stu-id="c09ec-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="c09ec-118">Questo comando ottiene il provider denominato contoso OpenID Connect provider.</span><span class="sxs-lookup"><span data-stu-id="c09ec-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="c09ec-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c09ec-119">PARAMETERS</span></span>

### <span data-ttu-id="c09ec-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c09ec-120">-Context</span></span>
<span data-ttu-id="c09ec-121">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c09ec-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c09ec-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c09ec-122">-DefaultProfile</span></span>
<span data-ttu-id="c09ec-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c09ec-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c09ec-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c09ec-124">-Name</span></span>
<span data-ttu-id="c09ec-125">Specifica un nome descrittivo di un provider.</span><span class="sxs-lookup"><span data-stu-id="c09ec-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="c09ec-126">Se specifichi un nome, questo cmdlet riceve il provider.</span><span class="sxs-lookup"><span data-stu-id="c09ec-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="c09ec-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="c09ec-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="c09ec-128">Specifica un ID del provider rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c09ec-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="c09ec-129">Se specifichi un ID, questo cmdlet riceve il provider.</span><span class="sxs-lookup"><span data-stu-id="c09ec-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="c09ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c09ec-130">CommonParameters</span></span>
<span data-ttu-id="c09ec-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c09ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c09ec-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c09ec-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c09ec-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c09ec-133">INPUTS</span></span>

### <span data-ttu-id="c09ec-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c09ec-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c09ec-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c09ec-135">System.String</span></span>

## <span data-ttu-id="c09ec-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c09ec-136">OUTPUTS</span></span>

### <span data-ttu-id="c09ec-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c09ec-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="c09ec-138">Note</span><span class="sxs-lookup"><span data-stu-id="c09ec-138">NOTES</span></span>

## <span data-ttu-id="c09ec-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c09ec-139">RELATED LINKS</span></span>

[<span data-ttu-id="c09ec-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c09ec-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="c09ec-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c09ec-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="c09ec-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c09ec-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


