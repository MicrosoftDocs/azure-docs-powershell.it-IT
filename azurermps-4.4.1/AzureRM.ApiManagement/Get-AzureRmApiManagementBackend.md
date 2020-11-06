---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518443"
---
# <span data-ttu-id="b66ec-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b66ec-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="b66ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b66ec-102">SYNOPSIS</span></span>
<span data-ttu-id="b66ec-103">Ottenere i dettagli del backend.</span><span class="sxs-lookup"><span data-stu-id="b66ec-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b66ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b66ec-104">SYNTAX</span></span>

### <span data-ttu-id="b66ec-105">Ottenere tutti i backend (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b66ec-105">Get all backends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b66ec-106">Ottieni per ID backend</span><span class="sxs-lookup"><span data-stu-id="b66ec-106">Get by backend ID</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b66ec-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b66ec-107">DESCRIPTION</span></span>
<span data-ttu-id="b66ec-108">Ottenere i dettagli del backend.</span><span class="sxs-lookup"><span data-stu-id="b66ec-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="b66ec-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b66ec-109">EXAMPLES</span></span>

### <span data-ttu-id="b66ec-110">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b66ec-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="b66ec-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b66ec-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="b66ec-112">Ottiene un elenco di tutti i backend configurati nel servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b66ec-112">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="b66ec-113">--------------------------Esempio 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b66ec-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="b66ec-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b66ec-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="b66ec-115">Ottenere i dettagli del backend specificato identificato dall'identificatore "123"</span><span class="sxs-lookup"><span data-stu-id="b66ec-115">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="b66ec-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b66ec-116">PARAMETERS</span></span>

### <span data-ttu-id="b66ec-117">-BackendId</span><span class="sxs-lookup"><span data-stu-id="b66ec-117">-BackendId</span></span>
<span data-ttu-id="b66ec-118">Identificatore di un backend.</span><span class="sxs-lookup"><span data-stu-id="b66ec-118">Identifier of a backend.</span></span>
<span data-ttu-id="b66ec-119">Se specificato cercherà di trovare il backend dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="b66ec-119">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="b66ec-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b66ec-120">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b66ec-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b66ec-121">-Context</span></span>
<span data-ttu-id="b66ec-122">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b66ec-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b66ec-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b66ec-123">This parameter is required.</span></span>

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

### <span data-ttu-id="b66ec-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b66ec-124">-DefaultProfile</span></span>
<span data-ttu-id="b66ec-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b66ec-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b66ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b66ec-126">CommonParameters</span></span>
<span data-ttu-id="b66ec-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b66ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b66ec-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b66ec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b66ec-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b66ec-129">INPUTS</span></span>

## <span data-ttu-id="b66ec-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b66ec-130">OUTPUTS</span></span>

### <span data-ttu-id="b66ec-131">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend></span><span class="sxs-lookup"><span data-stu-id="b66ec-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>

### <span data-ttu-id="b66ec-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b66ec-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger.PsApiManagementBackend</span></span>

## <span data-ttu-id="b66ec-133">Note</span><span class="sxs-lookup"><span data-stu-id="b66ec-133">NOTES</span></span>

## <span data-ttu-id="b66ec-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b66ec-134">RELATED LINKS</span></span>

[<span data-ttu-id="b66ec-135">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b66ec-135">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="b66ec-136">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b66ec-136">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="b66ec-137">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b66ec-137">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="b66ec-138">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b66ec-138">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="b66ec-139">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b66ec-139">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
