---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 95784b084f6d106413c65b840dd73f313a47799e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687749"
---
# <span data-ttu-id="57eb5-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="57eb5-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="57eb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="57eb5-103">Ottiene un'API.</span><span class="sxs-lookup"><span data-stu-id="57eb5-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57eb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57eb5-104">SYNTAX</span></span>

### <span data-ttu-id="57eb5-105">Tutte le API (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57eb5-105">All APIs (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57eb5-106">Trova per ID</span><span class="sxs-lookup"><span data-stu-id="57eb5-106">Find by ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57eb5-107">Ricerca per nome</span><span class="sxs-lookup"><span data-stu-id="57eb5-107">Find by Name</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57eb5-108">Trovare per ID prodotto</span><span class="sxs-lookup"><span data-stu-id="57eb5-108">Find by product ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57eb5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57eb5-109">DESCRIPTION</span></span>
<span data-ttu-id="57eb5-110">Il cmdlet **Get-AzureRmApiManagementApi** ottiene una o più API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="57eb5-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="57eb5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57eb5-111">EXAMPLES</span></span>

### <span data-ttu-id="57eb5-112">Esempio 1: ottenere tutte le API di gestione</span><span class="sxs-lookup"><span data-stu-id="57eb5-112">Example 1: Get all management APIs</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="57eb5-113">Questo comando consente di ottenere tutte le API per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="57eb5-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="57eb5-114">Esempio 2: ottenere un'API di gestione per ID</span><span class="sxs-lookup"><span data-stu-id="57eb5-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="57eb5-115">Questo comando consente di ottenere l'API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="57eb5-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="57eb5-116">Esempio 3: ottenere un'API di gestione per nome</span><span class="sxs-lookup"><span data-stu-id="57eb5-116">Example 3: Get a management API by name</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="57eb5-117">Questo comando consente di ottenere l'API con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="57eb5-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="57eb5-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57eb5-118">PARAMETERS</span></span>

### <span data-ttu-id="57eb5-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="57eb5-119">-ApiId</span></span>
<span data-ttu-id="57eb5-120">Specifica l'ID dell'API da ottenere.</span><span class="sxs-lookup"><span data-stu-id="57eb5-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57eb5-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="57eb5-121">-Context</span></span>
<span data-ttu-id="57eb5-122">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="57eb5-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="57eb5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="57eb5-123">-Name</span></span>
<span data-ttu-id="57eb5-124">Specifica il nome dell'API da ottenere.</span><span class="sxs-lookup"><span data-stu-id="57eb5-124">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by Name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57eb5-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="57eb5-125">-ProductId</span></span>
<span data-ttu-id="57eb5-126">Specifica l'ID del prodotto per cui ottenere l'API.</span><span class="sxs-lookup"><span data-stu-id="57eb5-126">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by product ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57eb5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57eb5-127">-DefaultProfile</span></span>
<span data-ttu-id="57eb5-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57eb5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57eb5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57eb5-129">CommonParameters</span></span>
<span data-ttu-id="57eb5-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57eb5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57eb5-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57eb5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57eb5-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57eb5-132">INPUTS</span></span>

## <span data-ttu-id="57eb5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57eb5-133">OUTPUTS</span></span>

### <span data-ttu-id="57eb5-134">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi></span><span class="sxs-lookup"><span data-stu-id="57eb5-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>

## <span data-ttu-id="57eb5-135">Note</span><span class="sxs-lookup"><span data-stu-id="57eb5-135">NOTES</span></span>

## <span data-ttu-id="57eb5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57eb5-136">RELATED LINKS</span></span>

[<span data-ttu-id="57eb5-137">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="57eb5-137">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="57eb5-138">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="57eb5-138">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="57eb5-139">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="57eb5-139">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="57eb5-140">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="57eb5-140">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="57eb5-141">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="57eb5-141">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


