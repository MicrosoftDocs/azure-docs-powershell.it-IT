---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: da9924624065937a0cb2d78160b1a12cb698a42d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514575"
---
# <span data-ttu-id="b8ead-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b8ead-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="b8ead-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8ead-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ead-103">Crea un'istanza di PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b8ead-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8ead-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8ead-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8ead-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8ead-105">DESCRIPTION</span></span>
<span data-ttu-id="b8ead-106">Il cmdlet **New-AzureRmApiManagementContext** crea un'istanza di **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="b8ead-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="b8ead-107">Il contesto viene usato per tutti i cmdlet del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b8ead-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="b8ead-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8ead-108">EXAMPLES</span></span>

### <span data-ttu-id="b8ead-109">Esempio 1: creare un'istanza di PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b8ead-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="b8ead-110">Questo comando crea un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="b8ead-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="b8ead-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8ead-111">PARAMETERS</span></span>

### <span data-ttu-id="b8ead-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ead-112">-DefaultProfile</span></span>
<span data-ttu-id="b8ead-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ead-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b8ead-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ead-114">-ResourceGroupName</span></span>
<span data-ttu-id="b8ead-115">Specifica il nome del gruppo di risorse in cui è distribuito un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b8ead-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ead-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b8ead-116">-ServiceName</span></span>
<span data-ttu-id="b8ead-117">Specifica il nome del servizio di gestione API distribuito.</span><span class="sxs-lookup"><span data-stu-id="b8ead-117">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ead-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ead-118">CommonParameters</span></span>
<span data-ttu-id="b8ead-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ead-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ead-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8ead-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ead-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8ead-121">INPUTS</span></span>

### <span data-ttu-id="b8ead-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b8ead-122">None</span></span>
<span data-ttu-id="b8ead-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b8ead-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8ead-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8ead-124">OUTPUTS</span></span>

### <span data-ttu-id="b8ead-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsAzureApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b8ead-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="b8ead-126">Note</span><span class="sxs-lookup"><span data-stu-id="b8ead-126">NOTES</span></span>

## <span data-ttu-id="b8ead-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8ead-127">RELATED LINKS</span></span>

