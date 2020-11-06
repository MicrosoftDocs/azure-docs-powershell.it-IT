---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 11d832bc74aca4ac274ee17ff0b38de06b77e377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512068"
---
# <span data-ttu-id="521c9-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="521c9-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="521c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="521c9-102">SYNOPSIS</span></span>
<span data-ttu-id="521c9-103">Ottenere i dettagli del backend.</span><span class="sxs-lookup"><span data-stu-id="521c9-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="521c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="521c9-104">SYNTAX</span></span>

### <span data-ttu-id="521c9-105">GetAllBackends (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="521c9-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="521c9-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="521c9-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="521c9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="521c9-107">DESCRIPTION</span></span>
<span data-ttu-id="521c9-108">Ottenere i dettagli del backend.</span><span class="sxs-lookup"><span data-stu-id="521c9-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="521c9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="521c9-109">EXAMPLES</span></span>

### <span data-ttu-id="521c9-110">Esempio 1: ottenere tutti i backend</span><span class="sxs-lookup"><span data-stu-id="521c9-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="521c9-111">Ottiene un elenco di tutti i backend configurati nel servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="521c9-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="521c9-112">Esempio 2: ottenere il backend specificato dall'identificatore 123</span><span class="sxs-lookup"><span data-stu-id="521c9-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="521c9-113">Ottenere i dettagli del backend specificato identificato dall'identificatore "123"</span><span class="sxs-lookup"><span data-stu-id="521c9-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="521c9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="521c9-114">PARAMETERS</span></span>

### <span data-ttu-id="521c9-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="521c9-115">-BackendId</span></span>
<span data-ttu-id="521c9-116">Identificatore di un backend.</span><span class="sxs-lookup"><span data-stu-id="521c9-116">Identifier of a backend.</span></span>
<span data-ttu-id="521c9-117">Se specificato cercherà di trovare il backend dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="521c9-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="521c9-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="521c9-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByBackendId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521c9-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="521c9-119">-Context</span></span>
<span data-ttu-id="521c9-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="521c9-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="521c9-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="521c9-121">This parameter is required.</span></span>

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

### <span data-ttu-id="521c9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521c9-122">-DefaultProfile</span></span>
<span data-ttu-id="521c9-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="521c9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="521c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521c9-124">CommonParameters</span></span>
<span data-ttu-id="521c9-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="521c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521c9-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="521c9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521c9-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="521c9-127">INPUTS</span></span>

### <span data-ttu-id="521c9-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="521c9-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="521c9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="521c9-129">System.String</span></span>

## <span data-ttu-id="521c9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="521c9-130">OUTPUTS</span></span>

### <span data-ttu-id="521c9-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="521c9-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="521c9-132">Note</span><span class="sxs-lookup"><span data-stu-id="521c9-132">NOTES</span></span>

## <span data-ttu-id="521c9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="521c9-133">RELATED LINKS</span></span>

[<span data-ttu-id="521c9-134">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="521c9-134">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="521c9-135">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="521c9-135">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="521c9-136">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="521c9-136">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="521c9-137">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="521c9-137">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="521c9-138">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="521c9-138">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
