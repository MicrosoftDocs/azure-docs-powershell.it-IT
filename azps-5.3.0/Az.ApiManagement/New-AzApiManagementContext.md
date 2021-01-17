---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478820"
---
# <span data-ttu-id="998ca-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="998ca-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="998ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="998ca-102">SYNOPSIS</span></span>
<span data-ttu-id="998ca-103">Crea un'istanza di PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="998ca-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="998ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="998ca-104">SYNTAX</span></span>

### <span data-ttu-id="998ca-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="998ca-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="998ca-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="998ca-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="998ca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="998ca-107">DESCRIPTION</span></span>
<span data-ttu-id="998ca-108">Il cmdlet **New-AzApiManagementContext** crea un'istanza di **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="998ca-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="998ca-109">Il contesto viene usato per tutti i cmdlet del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="998ca-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="998ca-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="998ca-110">EXAMPLES</span></span>

### <span data-ttu-id="998ca-111">Esempio 1: creare un'istanza di PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="998ca-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="998ca-112">Questo comando crea un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="998ca-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="998ca-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="998ca-113">PARAMETERS</span></span>

### <span data-ttu-id="998ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="998ca-114">-DefaultProfile</span></span>
<span data-ttu-id="998ca-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="998ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="998ca-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="998ca-116">-ResourceGroupName</span></span>
<span data-ttu-id="998ca-117">Specifica il nome del gruppo di risorse in cui è distribuito un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="998ca-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="998ca-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="998ca-118">-ResourceId</span></span>
<span data-ttu-id="998ca-119">Identificatore delle risorse ARM di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="998ca-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="998ca-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="998ca-120">This parameter is required.</span></span>

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

### <span data-ttu-id="998ca-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="998ca-121">-ServiceName</span></span>
<span data-ttu-id="998ca-122">Specifica il nome del servizio di gestione API distribuito.</span><span class="sxs-lookup"><span data-stu-id="998ca-122">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="998ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998ca-123">CommonParameters</span></span>
<span data-ttu-id="998ca-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="998ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998ca-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="998ca-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998ca-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="998ca-126">INPUTS</span></span>

### <span data-ttu-id="998ca-127">System. String</span><span class="sxs-lookup"><span data-stu-id="998ca-127">System.String</span></span>

## <span data-ttu-id="998ca-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="998ca-128">OUTPUTS</span></span>

### <span data-ttu-id="998ca-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="998ca-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="998ca-130">Note</span><span class="sxs-lookup"><span data-stu-id="998ca-130">NOTES</span></span>

## <span data-ttu-id="998ca-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="998ca-131">RELATED LINKS</span></span>
