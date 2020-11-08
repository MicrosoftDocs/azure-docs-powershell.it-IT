---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 7ec3eacc32157b833095522bbebc76f3838ae2a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019913"
---
# <span data-ttu-id="e24c4-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e24c4-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="e24c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e24c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e24c4-103">Ottiene un'API.</span><span class="sxs-lookup"><span data-stu-id="e24c4-103">Gets an API.</span></span>

## <span data-ttu-id="e24c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e24c4-104">SYNTAX</span></span>

### <span data-ttu-id="e24c4-105">GetAllApis (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e24c4-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e24c4-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="e24c4-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e24c4-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="e24c4-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e24c4-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="e24c4-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e24c4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e24c4-109">DESCRIPTION</span></span>
<span data-ttu-id="e24c4-110">Il cmdlet **Get-AzApiManagementApi** ottiene una o più API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="e24c4-110">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="e24c4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e24c4-111">EXAMPLES</span></span>

### <span data-ttu-id="e24c4-112">Esempio 1: ottenere tutte le API di gestione</span><span class="sxs-lookup"><span data-stu-id="e24c4-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="e24c4-113">Questo comando consente di ottenere tutte le API per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="e24c4-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="e24c4-114">Esempio 2: ottenere un'API di gestione per ID</span><span class="sxs-lookup"><span data-stu-id="e24c4-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="e24c4-115">Questo comando consente di ottenere l'API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="e24c4-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="e24c4-116">Esempio 3: ottenere un'API di gestione per nome</span><span class="sxs-lookup"><span data-stu-id="e24c4-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="e24c4-117">Questo comando consente di ottenere l'API con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="e24c4-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="e24c4-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e24c4-118">PARAMETERS</span></span>

### <span data-ttu-id="e24c4-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e24c4-119">-ApiId</span></span>
<span data-ttu-id="e24c4-120">Specifica l'ID dell'API da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e24c4-120">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="e24c4-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e24c4-121">-ApiRevision</span></span>
<span data-ttu-id="e24c4-122">Identificatore di revisione della particolare revisione API.</span><span class="sxs-lookup"><span data-stu-id="e24c4-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="e24c4-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e24c4-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="e24c4-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e24c4-124">-Context</span></span>
<span data-ttu-id="e24c4-125">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e24c4-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e24c4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e24c4-126">-DefaultProfile</span></span>
<span data-ttu-id="e24c4-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e24c4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e24c4-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e24c4-128">-Name</span></span>
<span data-ttu-id="e24c4-129">Specifica il nome dell'API da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e24c4-129">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="e24c4-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e24c4-130">-ProductId</span></span>
<span data-ttu-id="e24c4-131">Specifica l'ID del prodotto per cui ottenere l'API.</span><span class="sxs-lookup"><span data-stu-id="e24c4-131">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="e24c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24c4-132">CommonParameters</span></span>
<span data-ttu-id="e24c4-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e24c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24c4-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e24c4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24c4-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e24c4-135">INPUTS</span></span>

### <span data-ttu-id="e24c4-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e24c4-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e24c4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e24c4-137">System.String</span></span>

## <span data-ttu-id="e24c4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e24c4-138">OUTPUTS</span></span>

### <span data-ttu-id="e24c4-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e24c4-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e24c4-140">Note</span><span class="sxs-lookup"><span data-stu-id="e24c4-140">NOTES</span></span>

## <span data-ttu-id="e24c4-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e24c4-141">RELATED LINKS</span></span>

[<span data-ttu-id="e24c4-142">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e24c4-142">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="e24c4-143">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e24c4-143">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="e24c4-144">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e24c4-144">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="e24c4-145">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e24c4-145">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="e24c4-146">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e24c4-146">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


