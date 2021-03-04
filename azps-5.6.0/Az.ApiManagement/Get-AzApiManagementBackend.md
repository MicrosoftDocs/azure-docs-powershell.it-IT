---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: ea9975038f1c738461f8c3bbda4cba70bafe8ad9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956509"
---
# <span data-ttu-id="dd233-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd233-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="dd233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd233-102">SYNOPSIS</span></span>
<span data-ttu-id="dd233-103">Ottenere i dettagli del back-end.</span><span class="sxs-lookup"><span data-stu-id="dd233-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="dd233-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd233-104">SYNTAX</span></span>

### <span data-ttu-id="dd233-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd233-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd233-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd233-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd233-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dd233-107">DESCRIPTION</span></span>
<span data-ttu-id="dd233-108">Ottenere i dettagli del back-end.</span><span class="sxs-lookup"><span data-stu-id="dd233-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="dd233-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd233-109">EXAMPLES</span></span>

### <span data-ttu-id="dd233-110">Esempio 1: Ottenere tutti i back-end</span><span class="sxs-lookup"><span data-stu-id="dd233-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="dd233-111">Ottiene un elenco di tutti i back-end configurati nel servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="dd233-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="dd233-112">Esempio 2: Ottenere il back-end specificato dall'identificatore 123</span><span class="sxs-lookup"><span data-stu-id="dd233-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="dd233-113">Ottenere i dettagli del Backend specificato identificato dall'identificatore '123'</span><span class="sxs-lookup"><span data-stu-id="dd233-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="dd233-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd233-114">PARAMETERS</span></span>

### <span data-ttu-id="dd233-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="dd233-115">-BackendId</span></span>
<span data-ttu-id="dd233-116">Identificatore di un back-end.</span><span class="sxs-lookup"><span data-stu-id="dd233-116">Identifier of a backend.</span></span>
<span data-ttu-id="dd233-117">Se specificato, tenterà di trovare il back-end in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="dd233-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="dd233-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dd233-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="dd233-119">-Context</span><span class="sxs-lookup"><span data-stu-id="dd233-119">-Context</span></span>
<span data-ttu-id="dd233-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dd233-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dd233-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="dd233-121">This parameter is required.</span></span>

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

### <span data-ttu-id="dd233-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd233-122">-DefaultProfile</span></span>
<span data-ttu-id="dd233-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd233-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd233-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd233-124">-ResourceId</span></span>
<span data-ttu-id="dd233-125">Arm Resource Identifier del back-end.</span><span class="sxs-lookup"><span data-stu-id="dd233-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="dd233-126">Se specificato, tenterà di trovare il back-end in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="dd233-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="dd233-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="dd233-127">This parameter is required.</span></span>

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

### <span data-ttu-id="dd233-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd233-128">CommonParameters</span></span>
<span data-ttu-id="dd233-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd233-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd233-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dd233-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd233-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="dd233-131">INPUTS</span></span>

### <span data-ttu-id="dd233-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd233-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dd233-133">System.String</span><span class="sxs-lookup"><span data-stu-id="dd233-133">System.String</span></span>

## <span data-ttu-id="dd233-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd233-134">OUTPUTS</span></span>

### <span data-ttu-id="dd233-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd233-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="dd233-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="dd233-136">NOTES</span></span>

## <span data-ttu-id="dd233-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd233-137">RELATED LINKS</span></span>

[<span data-ttu-id="dd233-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd233-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="dd233-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="dd233-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="dd233-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="dd233-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="dd233-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd233-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="dd233-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd233-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
