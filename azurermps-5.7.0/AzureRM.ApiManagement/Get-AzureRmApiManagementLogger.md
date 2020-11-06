---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: bcfcd052d2278fa39bc310a5c1927457a1b0fcd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519476"
---
# <span data-ttu-id="33d7d-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="33d7d-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="33d7d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="33d7d-103">Ottiene gli oggetti logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="33d7d-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33d7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33d7d-104">SYNTAX</span></span>

### <span data-ttu-id="33d7d-105">GetAllLoggers (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33d7d-105">GetAllLoggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33d7d-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="33d7d-106">GetByLoggerId</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33d7d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33d7d-107">DESCRIPTION</span></span>
<span data-ttu-id="33d7d-108">Il cmdlet **Get-AzureRmApiManagementLogger** ottiene un **logger** di gestione delle API di Azure o tutti i logger.</span><span class="sxs-lookup"><span data-stu-id="33d7d-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="33d7d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33d7d-109">EXAMPLES</span></span>

### <span data-ttu-id="33d7d-110">Esempio 1: ottenere tutti i logger</span><span class="sxs-lookup"><span data-stu-id="33d7d-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext
```

<span data-ttu-id="33d7d-111">Questo comando ottiene tutti i logger per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="33d7d-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="33d7d-112">Esempio 2: ottenere un logger specifico</span><span class="sxs-lookup"><span data-stu-id="33d7d-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="33d7d-113">Questo comando rimuove un logger con ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="33d7d-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="33d7d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33d7d-114">PARAMETERS</span></span>

### <span data-ttu-id="33d7d-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="33d7d-115">-Context</span></span>
<span data-ttu-id="33d7d-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="33d7d-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33d7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d7d-117">-DefaultProfile</span></span>
<span data-ttu-id="33d7d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33d7d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="33d7d-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="33d7d-119">-LoggerId</span></span>
<span data-ttu-id="33d7d-120">Specifica l'ID del logger specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="33d7d-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByLoggerId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33d7d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d7d-121">CommonParameters</span></span>
<span data-ttu-id="33d7d-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d7d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d7d-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d7d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d7d-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33d7d-124">INPUTS</span></span>

### <span data-ttu-id="33d7d-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="33d7d-125">None</span></span>
<span data-ttu-id="33d7d-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="33d7d-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33d7d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33d7d-127">OUTPUTS</span></span>

### <span data-ttu-id="33d7d-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="33d7d-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>
<span data-ttu-id="33d7d-129">Il dettaglio del logger configurato nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="33d7d-129">The detail of the Logger configured in API Management service.</span></span>

### <span data-ttu-id="33d7d-130">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger></span><span class="sxs-lookup"><span data-stu-id="33d7d-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>
<span data-ttu-id="33d7d-131">Elenco di logger configurati nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="33d7d-131">The list of Loggers configured in API Management service.</span></span>

## <span data-ttu-id="33d7d-132">Note</span><span class="sxs-lookup"><span data-stu-id="33d7d-132">NOTES</span></span>

## <span data-ttu-id="33d7d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33d7d-133">RELATED LINKS</span></span>

[<span data-ttu-id="33d7d-134">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="33d7d-134">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="33d7d-135">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="33d7d-135">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="33d7d-136">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="33d7d-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


