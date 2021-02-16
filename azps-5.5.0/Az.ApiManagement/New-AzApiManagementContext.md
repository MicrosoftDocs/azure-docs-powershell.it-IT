---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195414"
---
# <span data-ttu-id="170e2-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="170e2-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="170e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="170e2-102">SYNOPSIS</span></span>
<span data-ttu-id="170e2-103">Crea un'istanza di PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="170e2-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="170e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="170e2-104">SYNTAX</span></span>

### <span data-ttu-id="170e2-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="170e2-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="170e2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="170e2-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="170e2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="170e2-107">DESCRIPTION</span></span>
<span data-ttu-id="170e2-108">Il cmdlet **New-AzApiManagementContext** crea un'istanza **di PsAzureApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="170e2-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="170e2-109">Il contesto viene usato per tutti i cmdlet del servizio di gestione DELLE API.</span><span class="sxs-lookup"><span data-stu-id="170e2-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="170e2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="170e2-110">EXAMPLES</span></span>

### <span data-ttu-id="170e2-111">Esempio 1: Creare un'istanza di PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="170e2-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="170e2-112">Questo comando crea un'istanza **di PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="170e2-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="170e2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="170e2-113">PARAMETERS</span></span>

### <span data-ttu-id="170e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170e2-114">-DefaultProfile</span></span>
<span data-ttu-id="170e2-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="170e2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="170e2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170e2-116">-ResourceGroupName</span></span>
<span data-ttu-id="170e2-117">Specifica il nome del gruppo di risorse in cui viene distribuito un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="170e2-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170e2-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="170e2-118">-ResourceId</span></span>
<span data-ttu-id="170e2-119">Identificatore di risorsa Arm di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="170e2-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="170e2-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="170e2-120">This parameter is required.</span></span>

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

### <span data-ttu-id="170e2-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="170e2-121">-ServiceName</span></span>
<span data-ttu-id="170e2-122">Specifica il nome del servizio di gestione API distribuito.</span><span class="sxs-lookup"><span data-stu-id="170e2-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170e2-123">CommonParameters</span></span>
<span data-ttu-id="170e2-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170e2-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="170e2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170e2-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="170e2-126">INPUTS</span></span>

### <span data-ttu-id="170e2-127">System.String</span><span class="sxs-lookup"><span data-stu-id="170e2-127">System.String</span></span>

## <span data-ttu-id="170e2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="170e2-128">OUTPUTS</span></span>

### <span data-ttu-id="170e2-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="170e2-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="170e2-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="170e2-130">NOTES</span></span>

## <span data-ttu-id="170e2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="170e2-131">RELATED LINKS</span></span>
