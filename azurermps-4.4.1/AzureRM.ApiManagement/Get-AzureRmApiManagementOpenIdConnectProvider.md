---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508840"
---
# <span data-ttu-id="a6814-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a6814-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="a6814-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6814-102">SYNOPSIS</span></span>
<span data-ttu-id="a6814-103">Ottiene i provider di connessione OpenID.</span><span class="sxs-lookup"><span data-stu-id="a6814-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6814-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6814-104">SYNTAX</span></span>

### <span data-ttu-id="a6814-105">Ottenere tutti i provider di connessione OpenID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6814-105">Get all OpenID Connect Providers (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6814-106">Ottieni da OpenID Connect provider ID</span><span class="sxs-lookup"><span data-stu-id="a6814-106">Get by OpenID Connect Provider ID</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6814-107">Trovare il nome descrittivo di OpenID Connect provider</span><span class="sxs-lookup"><span data-stu-id="a6814-107">Find by OpenID Connect Provider friendly Name</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6814-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6814-108">DESCRIPTION</span></span>
<span data-ttu-id="a6814-109">Il cmdlet **Get-AzureRmApiManagementOpenIdConnectProvider** ottiene i provider di connessione OpenID in gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6814-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="a6814-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6814-110">EXAMPLES</span></span>

### <span data-ttu-id="a6814-111">Esempio 1: ottenere tutti i provider</span><span class="sxs-lookup"><span data-stu-id="a6814-111">Example 1: Get all providers</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

<span data-ttu-id="a6814-112">Questo comando ottiene tutti i provider di connessione OpenID per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="a6814-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="a6814-113">Esempio 2: ottenere un provider tramite un ID</span><span class="sxs-lookup"><span data-stu-id="a6814-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="a6814-114">Questo comando ottiene il provider con ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="a6814-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="a6814-115">Esempio 3: ottenere un provider usando un nome</span><span class="sxs-lookup"><span data-stu-id="a6814-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="a6814-116">Questo comando ottiene il provider denominato contoso OpenID Connect provider.</span><span class="sxs-lookup"><span data-stu-id="a6814-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="a6814-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6814-117">PARAMETERS</span></span>

### <span data-ttu-id="a6814-118">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a6814-118">-Context</span></span>
<span data-ttu-id="a6814-119">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a6814-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a6814-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6814-120">-Name</span></span>
<span data-ttu-id="a6814-121">Specifica un nome descrittivo di un provider.</span><span class="sxs-lookup"><span data-stu-id="a6814-121">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="a6814-122">Se specifichi un nome, questo cmdlet riceve il provider.</span><span class="sxs-lookup"><span data-stu-id="a6814-122">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6814-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="a6814-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="a6814-124">Specifica un ID del provider rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6814-124">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="a6814-125">Se specifichi un ID, questo cmdlet riceve il provider.</span><span class="sxs-lookup"><span data-stu-id="a6814-125">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6814-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6814-126">-DefaultProfile</span></span>
<span data-ttu-id="a6814-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6814-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6814-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6814-128">CommonParameters</span></span>
<span data-ttu-id="a6814-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6814-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6814-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6814-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6814-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6814-131">INPUTS</span></span>

## <span data-ttu-id="a6814-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6814-132">OUTPUTS</span></span>

### <span data-ttu-id="a6814-133">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="a6814-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>

## <span data-ttu-id="a6814-134">Note</span><span class="sxs-lookup"><span data-stu-id="a6814-134">NOTES</span></span>

## <span data-ttu-id="a6814-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6814-135">RELATED LINKS</span></span>

[<span data-ttu-id="a6814-136">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a6814-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a6814-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a6814-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a6814-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a6814-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


