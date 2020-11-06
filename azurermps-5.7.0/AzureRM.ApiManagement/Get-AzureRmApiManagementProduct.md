---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: a4bbc330b5cd4d7eaeec1d2e68252ceb5dd261f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514607"
---
# <span data-ttu-id="fa2c0-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fa2c0-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="fa2c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2c0-103">Ottiene un elenco o un prodotto specifico.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa2c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa2c0-104">SYNTAX</span></span>

### <span data-ttu-id="fa2c0-105">GetAllProducts (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa2c0-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa2c0-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="fa2c0-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa2c0-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="fa2c0-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa2c0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa2c0-108">DESCRIPTION</span></span>
<span data-ttu-id="fa2c0-109">Il cmdlet **Get-AzureRmApiManagementProduct** ottiene un elenco o un determinato prodotto.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="fa2c0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa2c0-110">EXAMPLES</span></span>

### <span data-ttu-id="fa2c0-111">Esempio 1: ottenere tutti i prodotti</span><span class="sxs-lookup"><span data-stu-id="fa2c0-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="fa2c0-112">Questo comando ottiene tutti i prodotti di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-112">This command get all API Management products.</span></span>

### <span data-ttu-id="fa2c0-113">Esempio 2: ottenere un prodotto in base all'ID</span><span class="sxs-lookup"><span data-stu-id="fa2c0-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="fa2c0-114">Questo comando ottiene un prodotto di gestione delle API per ID.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="fa2c0-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa2c0-115">PARAMETERS</span></span>

### <span data-ttu-id="fa2c0-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="fa2c0-116">-Context</span></span>
<span data-ttu-id="fa2c0-117">Specifica un'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="fa2c0-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2c0-118">-DefaultProfile</span></span>
<span data-ttu-id="fa2c0-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2c0-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="fa2c0-120">-ProductId</span></span>
<span data-ttu-id="fa2c0-121">Specifica l'identificatore del prodotto da cercare.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-121">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2c0-122">-Titolo</span><span class="sxs-lookup"><span data-stu-id="fa2c0-122">-Title</span></span>
<span data-ttu-id="fa2c0-123">Specifica il titolo del prodotto da cercare.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="fa2c0-124">Se specificato, il cmdlet tenta di ottenere il prodotto per titolo.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-124">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: String
Parameter Sets: GetByTitle
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2c0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2c0-125">CommonParameters</span></span>
<span data-ttu-id="fa2c0-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2c0-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa2c0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2c0-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa2c0-128">INPUTS</span></span>

### <span data-ttu-id="fa2c0-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fa2c0-129">None</span></span>
<span data-ttu-id="fa2c0-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa2c0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa2c0-131">OUTPUTS</span></span>

### <span data-ttu-id="fa2c0-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fa2c0-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>
<span data-ttu-id="fa2c0-133">Dettagli del prodotto nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-133">The details of the Product in API Management service.</span></span>

### <span data-ttu-id="fa2c0-134">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="fa2c0-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>
<span data-ttu-id="fa2c0-135">Elenco di prodotti nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="fa2c0-135">The list of Product in API Management service.</span></span>

## <span data-ttu-id="fa2c0-136">Note</span><span class="sxs-lookup"><span data-stu-id="fa2c0-136">NOTES</span></span>

## <span data-ttu-id="fa2c0-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa2c0-137">RELATED LINKS</span></span>

[<span data-ttu-id="fa2c0-138">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fa2c0-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="fa2c0-139">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fa2c0-139">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="fa2c0-140">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fa2c0-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


