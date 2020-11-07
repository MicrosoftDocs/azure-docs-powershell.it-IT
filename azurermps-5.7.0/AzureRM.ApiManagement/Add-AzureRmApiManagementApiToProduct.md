---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 08d6d8e5ecbcaa8b6810bd173062c5bb244ec5e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686528"
---
# <span data-ttu-id="a8568-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="a8568-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="a8568-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8568-102">SYNOPSIS</span></span>
<span data-ttu-id="a8568-103">Aggiunge un'API a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="a8568-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8568-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8568-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8568-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8568-105">DESCRIPTION</span></span>
<span data-ttu-id="a8568-106">Il cmdlet **Add-AzureRmApiManagementApiToProduct** aggiunge un'API di gestione delle API di Azure a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="a8568-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="a8568-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8568-107">EXAMPLES</span></span>

### <span data-ttu-id="a8568-108">Esempio 1: aggiungere un'API a un prodotto</span><span class="sxs-lookup"><span data-stu-id="a8568-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="a8568-109">Questo comando aggiunge l'API specificata al prodotto specificato.</span><span class="sxs-lookup"><span data-stu-id="a8568-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="a8568-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8568-110">PARAMETERS</span></span>

### <span data-ttu-id="a8568-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a8568-111">-ApiId</span></span>
<span data-ttu-id="a8568-112">Specifica l'ID di un'API da aggiungere a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="a8568-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8568-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a8568-113">-Context</span></span>
<span data-ttu-id="a8568-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a8568-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a8568-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8568-115">-DefaultProfile</span></span>
<span data-ttu-id="a8568-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8568-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8568-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8568-117">-PassThru</span></span>
<span data-ttu-id="a8568-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="a8568-118">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8568-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a8568-119">-ProductId</span></span>
<span data-ttu-id="a8568-120">Specifica l'ID del prodotto a cui aggiungere l'API.</span><span class="sxs-lookup"><span data-stu-id="a8568-120">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8568-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8568-121">CommonParameters</span></span>
<span data-ttu-id="a8568-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8568-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8568-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8568-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8568-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8568-124">INPUTS</span></span>

### <span data-ttu-id="a8568-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a8568-125">None</span></span>
<span data-ttu-id="a8568-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a8568-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8568-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8568-127">OUTPUTS</span></span>

### <span data-ttu-id="a8568-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="a8568-128">Boolean</span></span>

## <span data-ttu-id="a8568-129">Note</span><span class="sxs-lookup"><span data-stu-id="a8568-129">NOTES</span></span>

## <span data-ttu-id="a8568-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8568-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8568-131">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="a8568-131">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


