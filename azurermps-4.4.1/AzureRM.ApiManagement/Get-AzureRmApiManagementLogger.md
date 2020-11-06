---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: 48033c250286c59e2cadfadc1a5b5d28f869a66c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519651"
---
# <span data-ttu-id="438e0-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="438e0-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="438e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="438e0-102">SYNOPSIS</span></span>
<span data-ttu-id="438e0-103">Ottiene gli oggetti logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="438e0-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="438e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="438e0-104">SYNTAX</span></span>

### <span data-ttu-id="438e0-105">Ottenere tutti i logger (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="438e0-105">Get all loggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="438e0-106">Ottieni per ID logger</span><span class="sxs-lookup"><span data-stu-id="438e0-106">Get by logger ID</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="438e0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="438e0-107">DESCRIPTION</span></span>
<span data-ttu-id="438e0-108">Il cmdlet **Get-AzureRmApiManagementLogger** ottiene un **logger** di gestione delle API di Azure o tutti i logger.</span><span class="sxs-lookup"><span data-stu-id="438e0-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="438e0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="438e0-109">EXAMPLES</span></span>

### <span data-ttu-id="438e0-110">Esempio 1: ottenere tutti i logger</span><span class="sxs-lookup"><span data-stu-id="438e0-110">Example 1: Get all loggers</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext
```

<span data-ttu-id="438e0-111">Questo comando ottiene tutti i logger per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="438e0-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="438e0-112">Esempio 2: ottenere un logger specifico</span><span class="sxs-lookup"><span data-stu-id="438e0-112">Example 2: Get a specific logger</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123"
```

<span data-ttu-id="438e0-113">Questo comando rimuove un logger con ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="438e0-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="438e0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="438e0-114">PARAMETERS</span></span>

### <span data-ttu-id="438e0-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="438e0-115">-Context</span></span>
<span data-ttu-id="438e0-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="438e0-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="438e0-117">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="438e0-117">-LoggerId</span></span>
<span data-ttu-id="438e0-118">Specifica l'ID del logger specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="438e0-118">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by logger ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="438e0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="438e0-119">-DefaultProfile</span></span>
<span data-ttu-id="438e0-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="438e0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="438e0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="438e0-121">CommonParameters</span></span>
<span data-ttu-id="438e0-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="438e0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="438e0-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="438e0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="438e0-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="438e0-124">INPUTS</span></span>

## <span data-ttu-id="438e0-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="438e0-125">OUTPUTS</span></span>

### <span data-ttu-id="438e0-126">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger></span><span class="sxs-lookup"><span data-stu-id="438e0-126">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>

## <span data-ttu-id="438e0-127">Note</span><span class="sxs-lookup"><span data-stu-id="438e0-127">NOTES</span></span>

## <span data-ttu-id="438e0-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="438e0-128">RELATED LINKS</span></span>

[<span data-ttu-id="438e0-129">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="438e0-129">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="438e0-130">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="438e0-130">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="438e0-131">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="438e0-131">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


