---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 01767d80f0925647b2161dd26f504465d7f1d8e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033589"
---
# <span data-ttu-id="e53d2-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="e53d2-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="e53d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e53d2-102">SYNOPSIS</span></span>
<span data-ttu-id="e53d2-103">Aggiunge un'API a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="e53d2-103">Adds an API to a product.</span></span>

## <span data-ttu-id="e53d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e53d2-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e53d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e53d2-105">DESCRIPTION</span></span>
<span data-ttu-id="e53d2-106">Il cmdlet **Add-AzApiManagementApiToProduct** aggiunge un'API di gestione delle API di Azure a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="e53d2-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="e53d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e53d2-107">EXAMPLES</span></span>

### <span data-ttu-id="e53d2-108">Esempio 1: aggiungere un'API a un prodotto</span><span class="sxs-lookup"><span data-stu-id="e53d2-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="e53d2-109">Questo comando aggiunge l'API specificata al prodotto specificato.</span><span class="sxs-lookup"><span data-stu-id="e53d2-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="e53d2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e53d2-110">PARAMETERS</span></span>

### <span data-ttu-id="e53d2-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e53d2-111">-ApiId</span></span>
<span data-ttu-id="e53d2-112">Specifica l'ID di un'API da aggiungere a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="e53d2-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e53d2-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e53d2-113">-Context</span></span>
<span data-ttu-id="e53d2-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e53d2-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e53d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e53d2-115">-DefaultProfile</span></span>
<span data-ttu-id="e53d2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e53d2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e53d2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e53d2-117">-PassThru</span></span>
<span data-ttu-id="e53d2-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="e53d2-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e53d2-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e53d2-119">-ProductId</span></span>
<span data-ttu-id="e53d2-120">Specifica l'ID del prodotto a cui aggiungere l'API.</span><span class="sxs-lookup"><span data-stu-id="e53d2-120">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e53d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e53d2-121">CommonParameters</span></span>
<span data-ttu-id="e53d2-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e53d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e53d2-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e53d2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e53d2-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e53d2-124">INPUTS</span></span>

### <span data-ttu-id="e53d2-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e53d2-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e53d2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e53d2-126">System.String</span></span>

### <span data-ttu-id="e53d2-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e53d2-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e53d2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e53d2-128">OUTPUTS</span></span>

### <span data-ttu-id="e53d2-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e53d2-129">System.Boolean</span></span>

## <span data-ttu-id="e53d2-130">Note</span><span class="sxs-lookup"><span data-stu-id="e53d2-130">NOTES</span></span>

## <span data-ttu-id="e53d2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e53d2-131">RELATED LINKS</span></span>

[<span data-ttu-id="e53d2-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="e53d2-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


