---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 5e1cbec98e2b501a71f022766f7248c3209d590f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991744"
---
# <span data-ttu-id="e4762-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4762-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="e4762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4762-102">SYNOPSIS</span></span>
<span data-ttu-id="e4762-103">Ottiene un'API.</span><span class="sxs-lookup"><span data-stu-id="e4762-103">Gets an API.</span></span>

## <span data-ttu-id="e4762-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4762-104">SYNTAX</span></span>

### <span data-ttu-id="e4762-105">GetAllApis (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4762-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4762-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="e4762-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4762-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="e4762-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4762-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="e4762-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4762-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="e4762-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4762-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4762-110">DESCRIPTION</span></span>
<span data-ttu-id="e4762-111">Il **cmdlet Get-AzApiManagementApi** ottiene una o più API Di gestione API Di Azure.</span><span class="sxs-lookup"><span data-stu-id="e4762-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="e4762-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4762-112">EXAMPLES</span></span>

### <span data-ttu-id="e4762-113">Esempio 1: Ottenere tutte le API di gestione</span><span class="sxs-lookup"><span data-stu-id="e4762-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="e4762-114">Questo comando recupera tutte le API per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="e4762-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="e4762-115">Esempio 2: Ottenere un'API di gestione in base all'ID</span><span class="sxs-lookup"><span data-stu-id="e4762-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="e4762-116">Questo comando ottiene l'API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="e4762-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="e4762-117">Esempio 3: Ottenere un'API di gestione in base al nome</span><span class="sxs-lookup"><span data-stu-id="e4762-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="e4762-118">Questo comando ottiene l'API con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="e4762-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="e4762-119">Esempio 4: Ottenere un'API di gestione per GatewayId</span><span class="sxs-lookup"><span data-stu-id="e4762-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="e4762-120">Questo comando ottiene l'API per il valore GatewayId specificato.</span><span class="sxs-lookup"><span data-stu-id="e4762-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="e4762-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4762-121">PARAMETERS</span></span>

### <span data-ttu-id="e4762-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e4762-122">-ApiId</span></span>
<span data-ttu-id="e4762-123">Specifica l'ID dell'API da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e4762-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="e4762-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e4762-124">-ApiRevision</span></span>
<span data-ttu-id="e4762-125">Identificatore di revisione della specifica revisione api.</span><span class="sxs-lookup"><span data-stu-id="e4762-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="e4762-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e4762-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="e4762-127">-Context</span><span class="sxs-lookup"><span data-stu-id="e4762-127">-Context</span></span>
<span data-ttu-id="e4762-128">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="e4762-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e4762-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4762-129">-DefaultProfile</span></span>
<span data-ttu-id="e4762-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4762-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4762-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e4762-131">-GatewayId</span></span>
<span data-ttu-id="e4762-132">Se specificato, tenterà di ottenere tutte le API gateway.</span><span class="sxs-lookup"><span data-stu-id="e4762-132">If specified will try to get all Gateway APIs.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4762-133">-Name</span><span class="sxs-lookup"><span data-stu-id="e4762-133">-Name</span></span>
<span data-ttu-id="e4762-134">Specifica il nome dell'API da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e4762-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="e4762-135">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e4762-135">-ProductId</span></span>
<span data-ttu-id="e4762-136">Specifica l'ID del prodotto per cui ottenere l'API.</span><span class="sxs-lookup"><span data-stu-id="e4762-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="e4762-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4762-137">CommonParameters</span></span>
<span data-ttu-id="e4762-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4762-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4762-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e4762-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4762-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4762-140">INPUTS</span></span>

### <span data-ttu-id="e4762-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e4762-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e4762-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e4762-142">System.String</span></span>

## <span data-ttu-id="e4762-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4762-143">OUTPUTS</span></span>

### <span data-ttu-id="e4762-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4762-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e4762-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4762-145">NOTES</span></span>

## <span data-ttu-id="e4762-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4762-146">RELATED LINKS</span></span>

[<span data-ttu-id="e4762-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4762-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="e4762-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4762-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="e4762-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4762-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="e4762-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4762-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="e4762-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4762-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


