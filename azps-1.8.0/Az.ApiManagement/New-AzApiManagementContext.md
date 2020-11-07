---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: cec27d1f7fb83cb114cd4b9a5c508c807e8ebd5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685137"
---
# <span data-ttu-id="6ab47-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6ab47-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="6ab47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ab47-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab47-103">Crea un'istanza di PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6ab47-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="6ab47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ab47-104">SYNTAX</span></span>

```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ab47-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ab47-105">DESCRIPTION</span></span>
<span data-ttu-id="6ab47-106">Il cmdlet **New-AzApiManagementContext** crea un'istanza di **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="6ab47-106">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="6ab47-107">Il contesto viene usato per tutti i cmdlet del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="6ab47-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="6ab47-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ab47-108">EXAMPLES</span></span>

### <span data-ttu-id="6ab47-109">Esempio 1: creare un'istanza di PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6ab47-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="6ab47-110">Questo comando crea un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="6ab47-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="6ab47-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ab47-111">PARAMETERS</span></span>

### <span data-ttu-id="6ab47-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab47-112">-DefaultProfile</span></span>
<span data-ttu-id="6ab47-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab47-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ab47-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab47-114">-ResourceGroupName</span></span>
<span data-ttu-id="6ab47-115">Specifica il nome del gruppo di risorse in cui è distribuito un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="6ab47-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="6ab47-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6ab47-116">-ServiceName</span></span>
<span data-ttu-id="6ab47-117">Specifica il nome del servizio di gestione API distribuito.</span><span class="sxs-lookup"><span data-stu-id="6ab47-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="6ab47-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab47-118">CommonParameters</span></span>
<span data-ttu-id="6ab47-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab47-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab47-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ab47-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab47-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ab47-121">INPUTS</span></span>

### <span data-ttu-id="6ab47-122">System. String</span><span class="sxs-lookup"><span data-stu-id="6ab47-122">System.String</span></span>

## <span data-ttu-id="6ab47-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ab47-123">OUTPUTS</span></span>

### <span data-ttu-id="6ab47-124">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6ab47-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="6ab47-125">Note</span><span class="sxs-lookup"><span data-stu-id="6ab47-125">NOTES</span></span>

## <span data-ttu-id="6ab47-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ab47-126">RELATED LINKS</span></span>
