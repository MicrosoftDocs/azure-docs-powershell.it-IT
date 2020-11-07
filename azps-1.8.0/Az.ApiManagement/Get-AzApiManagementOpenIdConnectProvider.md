---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: b6c8c0260e1f45b55dedca4d0a9f1f5ab3fed59a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673640"
---
# <span data-ttu-id="220d5-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="220d5-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="220d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="220d5-102">SYNOPSIS</span></span>
<span data-ttu-id="220d5-103">Ottiene i provider di connessione OpenID.</span><span class="sxs-lookup"><span data-stu-id="220d5-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="220d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="220d5-104">SYNTAX</span></span>

### <span data-ttu-id="220d5-105">GetAllOpenIdConnectProviders (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="220d5-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="220d5-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="220d5-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="220d5-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="220d5-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="220d5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="220d5-108">DESCRIPTION</span></span>
<span data-ttu-id="220d5-109">Il cmdlet **Get-AzApiManagementOpenIdConnectProvider** ottiene i provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="220d5-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="220d5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="220d5-110">EXAMPLES</span></span>

### <span data-ttu-id="220d5-111">Esempio 1: ottenere tutti i provider</span><span class="sxs-lookup"><span data-stu-id="220d5-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="220d5-112">Questo comando ottiene tutti i provider di connessione OpenID per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="220d5-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="220d5-113">Esempio 2: ottenere un provider tramite un ID</span><span class="sxs-lookup"><span data-stu-id="220d5-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="220d5-114">Questo comando ottiene il provider con ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="220d5-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="220d5-115">Esempio 3: ottenere un provider usando un nome</span><span class="sxs-lookup"><span data-stu-id="220d5-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="220d5-116">Questo comando ottiene il provider denominato contoso OpenID Connect provider.</span><span class="sxs-lookup"><span data-stu-id="220d5-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="220d5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="220d5-117">PARAMETERS</span></span>

### <span data-ttu-id="220d5-118">-Contesto</span><span class="sxs-lookup"><span data-stu-id="220d5-118">-Context</span></span>
<span data-ttu-id="220d5-119">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="220d5-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="220d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220d5-120">-DefaultProfile</span></span>
<span data-ttu-id="220d5-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="220d5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="220d5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="220d5-122">-Name</span></span>
<span data-ttu-id="220d5-123">Specifica un nome descrittivo di un provider.</span><span class="sxs-lookup"><span data-stu-id="220d5-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="220d5-124">Se specifichi un nome, questo cmdlet riceve il provider.</span><span class="sxs-lookup"><span data-stu-id="220d5-124">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="220d5-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="220d5-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="220d5-126">Specifica un ID del provider rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="220d5-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="220d5-127">Se specifichi un ID, questo cmdlet riceve il provider.</span><span class="sxs-lookup"><span data-stu-id="220d5-127">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="220d5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220d5-128">CommonParameters</span></span>
<span data-ttu-id="220d5-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="220d5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220d5-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="220d5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220d5-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="220d5-131">INPUTS</span></span>

### <span data-ttu-id="220d5-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="220d5-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="220d5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="220d5-133">System.String</span></span>

## <span data-ttu-id="220d5-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="220d5-134">OUTPUTS</span></span>

### <span data-ttu-id="220d5-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="220d5-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="220d5-136">Note</span><span class="sxs-lookup"><span data-stu-id="220d5-136">NOTES</span></span>

## <span data-ttu-id="220d5-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="220d5-137">RELATED LINKS</span></span>

[<span data-ttu-id="220d5-138">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="220d5-138">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="220d5-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="220d5-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="220d5-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="220d5-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


