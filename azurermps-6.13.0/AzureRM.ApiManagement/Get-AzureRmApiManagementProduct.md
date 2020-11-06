---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: 10b17f60ae100004c23a16f341924de6de11b0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507787"
---
# <span data-ttu-id="8da03-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8da03-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="8da03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8da03-102">SYNOPSIS</span></span>
<span data-ttu-id="8da03-103">Ottiene un elenco o un prodotto specifico.</span><span class="sxs-lookup"><span data-stu-id="8da03-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8da03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8da03-104">SYNTAX</span></span>

### <span data-ttu-id="8da03-105">GetAllProducts (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8da03-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8da03-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="8da03-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8da03-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="8da03-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8da03-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8da03-108">DESCRIPTION</span></span>
<span data-ttu-id="8da03-109">Il cmdlet **Get-AzureRmApiManagementProduct** ottiene un elenco o un determinato prodotto.</span><span class="sxs-lookup"><span data-stu-id="8da03-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="8da03-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8da03-110">EXAMPLES</span></span>

### <span data-ttu-id="8da03-111">Esempio 1: ottenere tutti i prodotti</span><span class="sxs-lookup"><span data-stu-id="8da03-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="8da03-112">Questo comando ottiene tutti i prodotti di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="8da03-112">This command get all API Management products.</span></span>

### <span data-ttu-id="8da03-113">Esempio 2: ottenere un prodotto in base all'ID</span><span class="sxs-lookup"><span data-stu-id="8da03-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="8da03-114">Questo comando ottiene un prodotto di gestione delle API per ID.</span><span class="sxs-lookup"><span data-stu-id="8da03-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="8da03-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8da03-115">PARAMETERS</span></span>

### <span data-ttu-id="8da03-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8da03-116">-Context</span></span>
<span data-ttu-id="8da03-117">Specifica un'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8da03-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8da03-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da03-118">-DefaultProfile</span></span>
<span data-ttu-id="8da03-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8da03-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8da03-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8da03-120">-ProductId</span></span>
<span data-ttu-id="8da03-121">Specifica l'identificatore del prodotto da cercare.</span><span class="sxs-lookup"><span data-stu-id="8da03-121">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="8da03-122">-Titolo</span><span class="sxs-lookup"><span data-stu-id="8da03-122">-Title</span></span>
<span data-ttu-id="8da03-123">Specifica il titolo del prodotto da cercare.</span><span class="sxs-lookup"><span data-stu-id="8da03-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="8da03-124">Se specificato, il cmdlet tenta di ottenere il prodotto per titolo.</span><span class="sxs-lookup"><span data-stu-id="8da03-124">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="8da03-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da03-125">CommonParameters</span></span>
<span data-ttu-id="8da03-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da03-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da03-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da03-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da03-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8da03-128">INPUTS</span></span>

### <span data-ttu-id="8da03-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8da03-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8da03-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8da03-130">System.String</span></span>

## <span data-ttu-id="8da03-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8da03-131">OUTPUTS</span></span>

### <span data-ttu-id="8da03-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8da03-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="8da03-133">Note</span><span class="sxs-lookup"><span data-stu-id="8da03-133">NOTES</span></span>

## <span data-ttu-id="8da03-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8da03-134">RELATED LINKS</span></span>

[<span data-ttu-id="8da03-135">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8da03-135">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="8da03-136">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8da03-136">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="8da03-137">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8da03-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


