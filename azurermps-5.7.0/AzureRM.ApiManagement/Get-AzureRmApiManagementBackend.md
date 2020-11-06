---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 0074ed7ec0d3aa88f813d138be71083195e6b10a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510191"
---
# <span data-ttu-id="f21fb-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f21fb-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="f21fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f21fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f21fb-103">Ottenere i dettagli del backend.</span><span class="sxs-lookup"><span data-stu-id="f21fb-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f21fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f21fb-104">SYNTAX</span></span>

### <span data-ttu-id="f21fb-105">GetAllBackends (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f21fb-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f21fb-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="f21fb-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f21fb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f21fb-107">DESCRIPTION</span></span>
<span data-ttu-id="f21fb-108">Ottenere i dettagli del backend.</span><span class="sxs-lookup"><span data-stu-id="f21fb-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="f21fb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f21fb-109">EXAMPLES</span></span>

### <span data-ttu-id="f21fb-110">Esempio 1: ottenere tutti i backend</span><span class="sxs-lookup"><span data-stu-id="f21fb-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="f21fb-111">Ottiene un elenco di tutti i backend configurati nel servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="f21fb-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="f21fb-112">Esempio 2: ottenere il backend specificato dall'identificatore 123</span><span class="sxs-lookup"><span data-stu-id="f21fb-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="f21fb-113">Ottenere i dettagli del backend specificato identificato dall'identificatore "123"</span><span class="sxs-lookup"><span data-stu-id="f21fb-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="f21fb-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f21fb-114">PARAMETERS</span></span>

### <span data-ttu-id="f21fb-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="f21fb-115">-BackendId</span></span>
<span data-ttu-id="f21fb-116">Identificatore di un backend.</span><span class="sxs-lookup"><span data-stu-id="f21fb-116">Identifier of a backend.</span></span>
<span data-ttu-id="f21fb-117">Se specificato cercherà di trovare il backend dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="f21fb-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="f21fb-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f21fb-118">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByBackendId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f21fb-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f21fb-119">-Context</span></span>
<span data-ttu-id="f21fb-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f21fb-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f21fb-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f21fb-121">This parameter is required.</span></span>

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

### <span data-ttu-id="f21fb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f21fb-122">-DefaultProfile</span></span>
<span data-ttu-id="f21fb-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f21fb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f21fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f21fb-124">CommonParameters</span></span>
<span data-ttu-id="f21fb-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f21fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f21fb-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f21fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f21fb-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f21fb-127">INPUTS</span></span>

### <span data-ttu-id="f21fb-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f21fb-128">None</span></span>
<span data-ttu-id="f21fb-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f21fb-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f21fb-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f21fb-130">OUTPUTS</span></span>

### <span data-ttu-id="f21fb-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f21fb-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>
<span data-ttu-id="f21fb-132">Dettagli del backend configurato nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="f21fb-132">The details of the Backend configured in API Management service.</span></span>

### <span data-ttu-id="f21fb-133">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend></span><span class="sxs-lookup"><span data-stu-id="f21fb-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>
<span data-ttu-id="f21fb-134">Elenco di backend configurato nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="f21fb-134">The list of Backend configured in API Management service.</span></span>

## <span data-ttu-id="f21fb-135">Note</span><span class="sxs-lookup"><span data-stu-id="f21fb-135">NOTES</span></span>

## <span data-ttu-id="f21fb-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f21fb-136">RELATED LINKS</span></span>

[<span data-ttu-id="f21fb-137">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f21fb-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="f21fb-138">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="f21fb-138">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="f21fb-139">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="f21fb-139">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="f21fb-140">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f21fb-140">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="f21fb-141">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f21fb-141">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
