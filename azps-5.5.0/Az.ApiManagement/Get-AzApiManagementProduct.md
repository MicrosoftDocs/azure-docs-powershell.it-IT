---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 8e59cbb9885587ee57103b78400ce8ece9aafd46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187718"
---
# <span data-ttu-id="3b0a6-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3b0a6-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="3b0a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3b0a6-103">Ottiene un elenco o un prodotto specifico.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="3b0a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b0a6-104">SYNTAX</span></span>

### <span data-ttu-id="3b0a6-105">GetAllProducts (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b0a6-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b0a6-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="3b0a6-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b0a6-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="3b0a6-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b0a6-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="3b0a6-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b0a6-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3b0a6-109">DESCRIPTION</span></span>
<span data-ttu-id="3b0a6-110">Il cmdlet **Get-AzApiManagementProduct** ottiene un elenco o un prodotto specifico.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="3b0a6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b0a6-111">EXAMPLES</span></span>

### <span data-ttu-id="3b0a6-112">Esempio 1: Ottenere tutti i prodotti</span><span class="sxs-lookup"><span data-stu-id="3b0a6-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="3b0a6-113">Questo comando consente di ottenere tutti i prodotti di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-113">This command get all API Management products.</span></span>

### <span data-ttu-id="3b0a6-114">Esempio 2: Ottenere un prodotto in base all'ID</span><span class="sxs-lookup"><span data-stu-id="3b0a6-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="3b0a6-115">Questo comando consente di ottenere un prodotto di gestione DELLE API in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="3b0a6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b0a6-116">PARAMETERS</span></span>

### <span data-ttu-id="3b0a6-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3b0a6-117">-ApiId</span></span>
<span data-ttu-id="3b0a6-118">ApiId dell'Api per trovare i prodotti correlati.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="3b0a6-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="3b0a6-120">-Context</span><span class="sxs-lookup"><span data-stu-id="3b0a6-120">-Context</span></span>
<span data-ttu-id="3b0a6-121">Specifica un'istanza di un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="3b0a6-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3b0a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b0a6-122">-DefaultProfile</span></span>
<span data-ttu-id="3b0a6-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b0a6-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="3b0a6-124">-ProductId</span></span>
<span data-ttu-id="3b0a6-125">Specifica l'identificatore del prodotto da cercare.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="3b0a6-126">-Title</span><span class="sxs-lookup"><span data-stu-id="3b0a6-126">-Title</span></span>
<span data-ttu-id="3b0a6-127">Specifica il titolo del prodotto da cercare.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="3b0a6-128">Se specificato, il cmdlet prova a ottenere il prodotto in base al titolo.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-128">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTitle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0a6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b0a6-129">CommonParameters</span></span>
<span data-ttu-id="3b0a6-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b0a6-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b0a6-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="3b0a6-132">INPUTS</span></span>

### <span data-ttu-id="3b0a6-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3b0a6-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3b0a6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3b0a6-134">System.String</span></span>

## <span data-ttu-id="3b0a6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b0a6-135">OUTPUTS</span></span>

### <span data-ttu-id="3b0a6-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3b0a6-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="3b0a6-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="3b0a6-137">NOTES</span></span>

## <span data-ttu-id="3b0a6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b0a6-138">RELATED LINKS</span></span>

[<span data-ttu-id="3b0a6-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3b0a6-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="3b0a6-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3b0a6-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="3b0a6-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3b0a6-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


