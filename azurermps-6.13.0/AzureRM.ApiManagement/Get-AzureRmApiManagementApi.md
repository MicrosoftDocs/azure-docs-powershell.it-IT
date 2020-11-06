---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: d84efcf68885e6d2e39ae15944c5f60298044ab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509448"
---
# <span data-ttu-id="861fb-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="861fb-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="861fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="861fb-102">SYNOPSIS</span></span>
<span data-ttu-id="861fb-103">Ottiene un'API.</span><span class="sxs-lookup"><span data-stu-id="861fb-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="861fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="861fb-104">SYNTAX</span></span>

### <span data-ttu-id="861fb-105">GetAllApis (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="861fb-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="861fb-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="861fb-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="861fb-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="861fb-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="861fb-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="861fb-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="861fb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="861fb-109">DESCRIPTION</span></span>
<span data-ttu-id="861fb-110">Il cmdlet **Get-AzureRmApiManagementApi** ottiene una o più API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="861fb-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="861fb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="861fb-111">EXAMPLES</span></span>

### <span data-ttu-id="861fb-112">Esempio 1: ottenere tutte le API di gestione</span><span class="sxs-lookup"><span data-stu-id="861fb-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="861fb-113">Questo comando consente di ottenere tutte le API per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="861fb-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="861fb-114">Esempio 2: ottenere un'API di gestione per ID</span><span class="sxs-lookup"><span data-stu-id="861fb-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="861fb-115">Questo comando consente di ottenere l'API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="861fb-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="861fb-116">Esempio 3: ottenere un'API di gestione per nome</span><span class="sxs-lookup"><span data-stu-id="861fb-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="861fb-117">Questo comando consente di ottenere l'API con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="861fb-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="861fb-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="861fb-118">PARAMETERS</span></span>

### <span data-ttu-id="861fb-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="861fb-119">-ApiId</span></span>
<span data-ttu-id="861fb-120">Specifica l'ID dell'API da ottenere.</span><span class="sxs-lookup"><span data-stu-id="861fb-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861fb-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="861fb-121">-ApiRevision</span></span>
<span data-ttu-id="861fb-122">Identificatore di revisione della particolare revisione API.</span><span class="sxs-lookup"><span data-stu-id="861fb-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="861fb-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="861fb-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861fb-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="861fb-124">-Context</span></span>
<span data-ttu-id="861fb-125">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="861fb-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="861fb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="861fb-126">-DefaultProfile</span></span>
<span data-ttu-id="861fb-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="861fb-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="861fb-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="861fb-128">-Name</span></span>
<span data-ttu-id="861fb-129">Specifica il nome dell'API da ottenere.</span><span class="sxs-lookup"><span data-stu-id="861fb-129">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861fb-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="861fb-130">-ProductId</span></span>
<span data-ttu-id="861fb-131">Specifica l'ID del prodotto per cui ottenere l'API.</span><span class="sxs-lookup"><span data-stu-id="861fb-131">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861fb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="861fb-132">CommonParameters</span></span>
<span data-ttu-id="861fb-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="861fb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="861fb-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="861fb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="861fb-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="861fb-135">INPUTS</span></span>

### <span data-ttu-id="861fb-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="861fb-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="861fb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="861fb-137">System.String</span></span>

## <span data-ttu-id="861fb-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="861fb-138">OUTPUTS</span></span>

### <span data-ttu-id="861fb-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="861fb-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="861fb-140">Note</span><span class="sxs-lookup"><span data-stu-id="861fb-140">NOTES</span></span>

## <span data-ttu-id="861fb-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="861fb-141">RELATED LINKS</span></span>

[<span data-ttu-id="861fb-142">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="861fb-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="861fb-143">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="861fb-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="861fb-144">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="861fb-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="861fb-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="861fb-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="861fb-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="861fb-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


