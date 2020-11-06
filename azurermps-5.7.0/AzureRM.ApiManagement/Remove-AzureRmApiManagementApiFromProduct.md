---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 413d03723ee2acdc162c1f1f5501d90156e16069
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521478"
---
# <span data-ttu-id="629bb-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="629bb-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="629bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="629bb-102">SYNOPSIS</span></span>
<span data-ttu-id="629bb-103">Rimuove un'API da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="629bb-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="629bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="629bb-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="629bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="629bb-105">DESCRIPTION</span></span>
<span data-ttu-id="629bb-106">Il cmdlet **Remove-AzureRmApiManagementApiFromProduct** rimuove un'API di gestione delle API di Azure da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="629bb-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="629bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="629bb-107">EXAMPLES</span></span>

### <span data-ttu-id="629bb-108">Esempio 1: rimuovere un'API da un prodotto</span><span class="sxs-lookup"><span data-stu-id="629bb-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="629bb-109">Questo commnd rimuove l'API specificata da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="629bb-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="629bb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="629bb-110">PARAMETERS</span></span>

### <span data-ttu-id="629bb-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="629bb-111">-ApiId</span></span>
<span data-ttu-id="629bb-112">Specifica l'ID dell'API da rimuovere dal prodotto.</span><span class="sxs-lookup"><span data-stu-id="629bb-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="629bb-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="629bb-113">-Context</span></span>
<span data-ttu-id="629bb-114">Specifica un **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="629bb-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="629bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="629bb-115">-DefaultProfile</span></span>
<span data-ttu-id="629bb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="629bb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="629bb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="629bb-117">-PassThru</span></span>
<span data-ttu-id="629bb-118">Indica che questo cmdlet restituisce un valore di $True se riesce o $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="629bb-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="629bb-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="629bb-119">-ProductId</span></span>
<span data-ttu-id="629bb-120">Specifica l'ID del prodotto da cui rimuovere l'API.</span><span class="sxs-lookup"><span data-stu-id="629bb-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="629bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="629bb-121">CommonParameters</span></span>
<span data-ttu-id="629bb-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="629bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="629bb-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="629bb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="629bb-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="629bb-124">INPUTS</span></span>

### <span data-ttu-id="629bb-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="629bb-125">None</span></span>
<span data-ttu-id="629bb-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="629bb-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="629bb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="629bb-127">OUTPUTS</span></span>

### <span data-ttu-id="629bb-128">bool</span><span class="sxs-lookup"><span data-stu-id="629bb-128">bool</span></span>

## <span data-ttu-id="629bb-129">Note</span><span class="sxs-lookup"><span data-stu-id="629bb-129">NOTES</span></span>

## <span data-ttu-id="629bb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="629bb-130">RELATED LINKS</span></span>

[<span data-ttu-id="629bb-131">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="629bb-131">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


