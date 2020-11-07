---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 9ad3c6b149e58bcd81ec8ce9c15ddc27fff85878
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676057"
---
# <span data-ttu-id="3add7-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3add7-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="3add7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3add7-102">SYNOPSIS</span></span>
<span data-ttu-id="3add7-103">Ottiene un elenco o un prodotto specifico.</span><span class="sxs-lookup"><span data-stu-id="3add7-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="3add7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3add7-104">SYNTAX</span></span>

### <span data-ttu-id="3add7-105">GetAllProducts (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3add7-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3add7-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="3add7-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3add7-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="3add7-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3add7-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="3add7-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3add7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3add7-109">DESCRIPTION</span></span>
<span data-ttu-id="3add7-110">Il cmdlet **Get-AzApiManagementProduct** ottiene un elenco o un determinato prodotto.</span><span class="sxs-lookup"><span data-stu-id="3add7-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="3add7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3add7-111">EXAMPLES</span></span>

### <span data-ttu-id="3add7-112">Esempio 1: ottenere tutti i prodotti</span><span class="sxs-lookup"><span data-stu-id="3add7-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="3add7-113">Questo comando ottiene tutti i prodotti di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="3add7-113">This command get all API Management products.</span></span>

### <span data-ttu-id="3add7-114">Esempio 2: ottenere un prodotto in base all'ID</span><span class="sxs-lookup"><span data-stu-id="3add7-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="3add7-115">Questo comando ottiene un prodotto di gestione delle API per ID.</span><span class="sxs-lookup"><span data-stu-id="3add7-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="3add7-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3add7-116">PARAMETERS</span></span>

### <span data-ttu-id="3add7-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3add7-117">-ApiId</span></span>
<span data-ttu-id="3add7-118">ApiId dell'API per trovare i prodotti correlati.</span><span class="sxs-lookup"><span data-stu-id="3add7-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="3add7-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3add7-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="3add7-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3add7-120">-Context</span></span>
<span data-ttu-id="3add7-121">Specifica un'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3add7-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3add7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3add7-122">-DefaultProfile</span></span>
<span data-ttu-id="3add7-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3add7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3add7-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="3add7-124">-ProductId</span></span>
<span data-ttu-id="3add7-125">Specifica l'identificatore del prodotto da cercare.</span><span class="sxs-lookup"><span data-stu-id="3add7-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="3add7-126">-Titolo</span><span class="sxs-lookup"><span data-stu-id="3add7-126">-Title</span></span>
<span data-ttu-id="3add7-127">Specifica il titolo del prodotto da cercare.</span><span class="sxs-lookup"><span data-stu-id="3add7-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="3add7-128">Se specificato, il cmdlet tenta di ottenere il prodotto per titolo.</span><span class="sxs-lookup"><span data-stu-id="3add7-128">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="3add7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3add7-129">CommonParameters</span></span>
<span data-ttu-id="3add7-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3add7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3add7-131">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3add7-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3add7-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3add7-132">INPUTS</span></span>

### <span data-ttu-id="3add7-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3add7-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3add7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3add7-134">System.String</span></span>

## <span data-ttu-id="3add7-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3add7-135">OUTPUTS</span></span>

### <span data-ttu-id="3add7-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3add7-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="3add7-137">Note</span><span class="sxs-lookup"><span data-stu-id="3add7-137">NOTES</span></span>

## <span data-ttu-id="3add7-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3add7-138">RELATED LINKS</span></span>

[<span data-ttu-id="3add7-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3add7-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="3add7-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3add7-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="3add7-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3add7-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


