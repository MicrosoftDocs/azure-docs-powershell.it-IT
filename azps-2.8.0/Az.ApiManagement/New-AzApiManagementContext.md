---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 6c8adaf7f66a676a5d623c51f299ef49407cc78b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676011"
---
# <span data-ttu-id="fad88-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fad88-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="fad88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fad88-102">SYNOPSIS</span></span>
<span data-ttu-id="fad88-103">Crea un'istanza di PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fad88-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="fad88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fad88-104">SYNTAX</span></span>

### <span data-ttu-id="fad88-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fad88-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fad88-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fad88-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fad88-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fad88-107">DESCRIPTION</span></span>
<span data-ttu-id="fad88-108">Il cmdlet **New-AzApiManagementContext** crea un'istanza di **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="fad88-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="fad88-109">Il contesto viene usato per tutti i cmdlet del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="fad88-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="fad88-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fad88-110">EXAMPLES</span></span>

### <span data-ttu-id="fad88-111">Esempio 1: creare un'istanza di PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fad88-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="fad88-112">Questo comando crea un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="fad88-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="fad88-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fad88-113">PARAMETERS</span></span>

### <span data-ttu-id="fad88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad88-114">-DefaultProfile</span></span>
<span data-ttu-id="fad88-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fad88-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fad88-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fad88-116">-ResourceGroupName</span></span>
<span data-ttu-id="fad88-117">Specifica il nome del gruppo di risorse in cui è distribuito un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="fad88-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="fad88-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fad88-118">-ResourceId</span></span>
<span data-ttu-id="fad88-119">Identificatore delle risorse ARM di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="fad88-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="fad88-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fad88-120">This parameter is required.</span></span>

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

### <span data-ttu-id="fad88-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fad88-121">-ServiceName</span></span>
<span data-ttu-id="fad88-122">Specifica il nome del servizio di gestione API distribuito.</span><span class="sxs-lookup"><span data-stu-id="fad88-122">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="fad88-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad88-123">CommonParameters</span></span>
<span data-ttu-id="fad88-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad88-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad88-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fad88-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad88-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fad88-126">INPUTS</span></span>

### <span data-ttu-id="fad88-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fad88-127">System.String</span></span>

## <span data-ttu-id="fad88-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fad88-128">OUTPUTS</span></span>

### <span data-ttu-id="fad88-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fad88-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="fad88-130">Note</span><span class="sxs-lookup"><span data-stu-id="fad88-130">NOTES</span></span>

## <span data-ttu-id="fad88-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fad88-131">RELATED LINKS</span></span>
