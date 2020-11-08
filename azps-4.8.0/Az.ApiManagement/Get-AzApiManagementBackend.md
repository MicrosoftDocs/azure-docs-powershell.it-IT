---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032721"
---
# <span data-ttu-id="272f7-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="272f7-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="272f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="272f7-102">SYNOPSIS</span></span>
<span data-ttu-id="272f7-103">Ottenere i dettagli del backend.</span><span class="sxs-lookup"><span data-stu-id="272f7-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="272f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="272f7-104">SYNTAX</span></span>

### <span data-ttu-id="272f7-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="272f7-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="272f7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="272f7-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="272f7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="272f7-107">DESCRIPTION</span></span>
<span data-ttu-id="272f7-108">Ottenere i dettagli del backend.</span><span class="sxs-lookup"><span data-stu-id="272f7-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="272f7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="272f7-109">EXAMPLES</span></span>

### <span data-ttu-id="272f7-110">Esempio 1: ottenere tutti i backend</span><span class="sxs-lookup"><span data-stu-id="272f7-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="272f7-111">Ottiene un elenco di tutti i backend configurati nel servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="272f7-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="272f7-112">Esempio 2: ottenere il backend specificato dall'identificatore 123</span><span class="sxs-lookup"><span data-stu-id="272f7-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="272f7-113">Ottenere i dettagli del backend specificato identificato dall'identificatore "123"</span><span class="sxs-lookup"><span data-stu-id="272f7-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="272f7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="272f7-114">PARAMETERS</span></span>

### <span data-ttu-id="272f7-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="272f7-115">-BackendId</span></span>
<span data-ttu-id="272f7-116">Identificatore di un backend.</span><span class="sxs-lookup"><span data-stu-id="272f7-116">Identifier of a backend.</span></span>
<span data-ttu-id="272f7-117">Se specificato cercherà di trovare il backend dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="272f7-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="272f7-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="272f7-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272f7-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="272f7-119">-Context</span></span>
<span data-ttu-id="272f7-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="272f7-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="272f7-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="272f7-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="272f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272f7-122">-DefaultProfile</span></span>
<span data-ttu-id="272f7-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="272f7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="272f7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="272f7-124">-ResourceId</span></span>
<span data-ttu-id="272f7-125">Identificatore delle risorse ARM del backend.</span><span class="sxs-lookup"><span data-stu-id="272f7-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="272f7-126">Se specificato cercherà di trovare il backend dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="272f7-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="272f7-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="272f7-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272f7-128">CommonParameters</span></span>
<span data-ttu-id="272f7-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="272f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272f7-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="272f7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272f7-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="272f7-131">INPUTS</span></span>

### <span data-ttu-id="272f7-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="272f7-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="272f7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="272f7-133">System.String</span></span>

## <span data-ttu-id="272f7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="272f7-134">OUTPUTS</span></span>

### <span data-ttu-id="272f7-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="272f7-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="272f7-136">Note</span><span class="sxs-lookup"><span data-stu-id="272f7-136">NOTES</span></span>

## <span data-ttu-id="272f7-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="272f7-137">RELATED LINKS</span></span>

[<span data-ttu-id="272f7-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="272f7-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="272f7-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="272f7-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="272f7-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="272f7-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="272f7-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="272f7-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="272f7-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="272f7-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
