---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 88a48edf3ae7e576aa78e989a5fda7515499a7f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673645"
---
# <span data-ttu-id="51fea-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="51fea-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="51fea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51fea-102">SYNOPSIS</span></span>
<span data-ttu-id="51fea-103">Ottenere i dettagli del backend.</span><span class="sxs-lookup"><span data-stu-id="51fea-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="51fea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51fea-104">SYNTAX</span></span>

### <span data-ttu-id="51fea-105">GetAllBackends (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51fea-105">GetAllBackends (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51fea-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="51fea-106">GetByBackendId</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51fea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51fea-107">DESCRIPTION</span></span>
<span data-ttu-id="51fea-108">Ottenere i dettagli del backend.</span><span class="sxs-lookup"><span data-stu-id="51fea-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="51fea-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51fea-109">EXAMPLES</span></span>

### <span data-ttu-id="51fea-110">Esempio 1: ottenere tutti i backend</span><span class="sxs-lookup"><span data-stu-id="51fea-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="51fea-111">Ottiene un elenco di tutti i backend configurati nel servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="51fea-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="51fea-112">Esempio 2: ottenere il backend specificato dall'identificatore 123</span><span class="sxs-lookup"><span data-stu-id="51fea-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="51fea-113">Ottenere i dettagli del backend specificato identificato dall'identificatore "123"</span><span class="sxs-lookup"><span data-stu-id="51fea-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="51fea-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51fea-114">PARAMETERS</span></span>

### <span data-ttu-id="51fea-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="51fea-115">-BackendId</span></span>
<span data-ttu-id="51fea-116">Identificatore di un backend.</span><span class="sxs-lookup"><span data-stu-id="51fea-116">Identifier of a backend.</span></span>
<span data-ttu-id="51fea-117">Se specificato cercherà di trovare il backend dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="51fea-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="51fea-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="51fea-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="51fea-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="51fea-119">-Context</span></span>
<span data-ttu-id="51fea-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="51fea-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="51fea-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="51fea-121">This parameter is required.</span></span>

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

### <span data-ttu-id="51fea-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51fea-122">-DefaultProfile</span></span>
<span data-ttu-id="51fea-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51fea-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51fea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fea-124">CommonParameters</span></span>
<span data-ttu-id="51fea-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51fea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fea-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51fea-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fea-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51fea-127">INPUTS</span></span>

### <span data-ttu-id="51fea-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="51fea-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="51fea-129">System. String</span><span class="sxs-lookup"><span data-stu-id="51fea-129">System.String</span></span>

## <span data-ttu-id="51fea-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51fea-130">OUTPUTS</span></span>

### <span data-ttu-id="51fea-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="51fea-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="51fea-132">Note</span><span class="sxs-lookup"><span data-stu-id="51fea-132">NOTES</span></span>

## <span data-ttu-id="51fea-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51fea-133">RELATED LINKS</span></span>

[<span data-ttu-id="51fea-134">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="51fea-134">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="51fea-135">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="51fea-135">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="51fea-136">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="51fea-136">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="51fea-137">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="51fea-137">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="51fea-138">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="51fea-138">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
