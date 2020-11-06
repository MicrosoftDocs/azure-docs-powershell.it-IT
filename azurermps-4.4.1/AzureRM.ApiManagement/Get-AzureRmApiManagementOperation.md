---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: b2c623d46dcc2d84e2c90ae5f3d94cfb54f7224a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517264"
---
# <span data-ttu-id="ff34a-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ff34a-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="ff34a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff34a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff34a-103">Ottiene un elenco o un'operazione API specificata.</span><span class="sxs-lookup"><span data-stu-id="ff34a-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff34a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff34a-104">SYNTAX</span></span>

### <span data-ttu-id="ff34a-105">Tutte le operazioni API (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff34a-105">All API Operations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff34a-106">Trova per ID</span><span class="sxs-lookup"><span data-stu-id="ff34a-106">Find by ID</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff34a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff34a-107">DESCRIPTION</span></span>
<span data-ttu-id="ff34a-108">Il comando **Get-AzureRmApiManagementOperation** ottiene un elenco o un'operazione API specificata.</span><span class="sxs-lookup"><span data-stu-id="ff34a-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="ff34a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff34a-109">EXAMPLES</span></span>

### <span data-ttu-id="ff34a-110">Esempio 1: ottenere tutte le operazioni di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="ff34a-110">Example 1: Get all API management operations</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId
```

<span data-ttu-id="ff34a-111">Questo comando consente di ottenere tutte le operazioni di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="ff34a-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="ff34a-112">Esempio 2: ottenere un'operazione di gestione delle API tramite ID operazione</span><span class="sxs-lookup"><span data-stu-id="ff34a-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="ff34a-113">Questo comando ottiene un'operazione di gestione delle API tramite l'ID operazione denominato Operation0003.</span><span class="sxs-lookup"><span data-stu-id="ff34a-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="ff34a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff34a-114">PARAMETERS</span></span>

### <span data-ttu-id="ff34a-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ff34a-115">-ApiId</span></span>
<span data-ttu-id="ff34a-116">Specifica l'identificatore dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="ff34a-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="ff34a-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ff34a-117">-Context</span></span>
<span data-ttu-id="ff34a-118">Specifica l'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ff34a-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ff34a-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ff34a-119">-OperationId</span></span>
<span data-ttu-id="ff34a-120">Specifica l'identificatore dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ff34a-120">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="ff34a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff34a-121">-DefaultProfile</span></span>
<span data-ttu-id="ff34a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff34a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff34a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff34a-123">CommonParameters</span></span>
<span data-ttu-id="ff34a-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff34a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff34a-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff34a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff34a-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff34a-126">INPUTS</span></span>

## <span data-ttu-id="ff34a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff34a-127">OUTPUTS</span></span>

### <span data-ttu-id="ff34a-128">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="ff34a-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>

## <span data-ttu-id="ff34a-129">Note</span><span class="sxs-lookup"><span data-stu-id="ff34a-129">NOTES</span></span>

## <span data-ttu-id="ff34a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff34a-130">RELATED LINKS</span></span>

[<span data-ttu-id="ff34a-131">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ff34a-131">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ff34a-132">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ff34a-132">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ff34a-133">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ff34a-133">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


