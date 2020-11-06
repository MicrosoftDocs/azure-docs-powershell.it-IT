---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: 7bf97454fd7dc4a2debc8861766981f6428f0b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517208"
---
# <span data-ttu-id="b034c-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b034c-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="b034c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b034c-102">SYNOPSIS</span></span>
<span data-ttu-id="b034c-103">Crea un'istanza di PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b034c-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b034c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b034c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b034c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b034c-105">DESCRIPTION</span></span>
<span data-ttu-id="b034c-106">Il cmdlet **New-AzureRmApiManagementContext** crea un'istanza di **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="b034c-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="b034c-107">Il contesto viene usato per tutti i cmdlet del servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b034c-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="b034c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b034c-108">EXAMPLES</span></span>

### <span data-ttu-id="b034c-109">Esempio 1: creare un'istanza di PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b034c-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="b034c-110">Questo comando crea un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="b034c-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="b034c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b034c-111">PARAMETERS</span></span>

### <span data-ttu-id="b034c-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b034c-112">-ResourceGroupName</span></span>
<span data-ttu-id="b034c-113">Specifica il nome del gruppo di risorse in cui è distribuito un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b034c-113">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="b034c-114">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b034c-114">-ServiceName</span></span>
<span data-ttu-id="b034c-115">Specifica il nome del servizio di gestione API distribuito.</span><span class="sxs-lookup"><span data-stu-id="b034c-115">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="b034c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b034c-116">-DefaultProfile</span></span>
<span data-ttu-id="b034c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b034c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b034c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b034c-118">CommonParameters</span></span>
<span data-ttu-id="b034c-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b034c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b034c-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b034c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b034c-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b034c-121">INPUTS</span></span>

## <span data-ttu-id="b034c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b034c-122">OUTPUTS</span></span>

### <span data-ttu-id="b034c-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsAzureApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b034c-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="b034c-124">Note</span><span class="sxs-lookup"><span data-stu-id="b034c-124">NOTES</span></span>

## <span data-ttu-id="b034c-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b034c-125">RELATED LINKS</span></span>

