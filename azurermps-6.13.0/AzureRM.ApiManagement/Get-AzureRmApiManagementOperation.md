---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 469d10303f286a0feca162e628a1564826b850d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507791"
---
# <span data-ttu-id="2247b-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2247b-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="2247b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2247b-102">SYNOPSIS</span></span>
<span data-ttu-id="2247b-103">Ottiene un elenco o un'operazione API specificata.</span><span class="sxs-lookup"><span data-stu-id="2247b-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2247b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2247b-104">SYNTAX</span></span>

### <span data-ttu-id="2247b-105">GetAllApiOperations (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2247b-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2247b-106">GetById</span><span class="sxs-lookup"><span data-stu-id="2247b-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2247b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2247b-107">DESCRIPTION</span></span>
<span data-ttu-id="2247b-108">Il comando **Get-AzureRmApiManagementOperation** ottiene un elenco o un'operazione API specificata.</span><span class="sxs-lookup"><span data-stu-id="2247b-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="2247b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2247b-109">EXAMPLES</span></span>

### <span data-ttu-id="2247b-110">Esempio 1: ottenere tutte le operazioni di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="2247b-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="2247b-111">Questo comando consente di ottenere tutte le operazioni di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="2247b-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="2247b-112">Esempio 2: ottenere un'operazione di gestione delle API tramite ID operazione</span><span class="sxs-lookup"><span data-stu-id="2247b-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="2247b-113">Questo comando ottiene un'operazione di gestione delle API tramite l'ID operazione denominato Operation0003.</span><span class="sxs-lookup"><span data-stu-id="2247b-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="2247b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2247b-114">PARAMETERS</span></span>

### <span data-ttu-id="2247b-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2247b-115">-ApiId</span></span>
<span data-ttu-id="2247b-116">Specifica l'identificatore dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="2247b-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="2247b-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="2247b-117">-ApiRevision</span></span>
<span data-ttu-id="2247b-118">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="2247b-118">Identifier of API Revision.</span></span> <span data-ttu-id="2247b-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2247b-119">This parameter is optional.</span></span> <span data-ttu-id="2247b-120">Se non specificato, l'operazione verrà recuperata dalla revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="2247b-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2247b-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2247b-121">-Context</span></span>
<span data-ttu-id="2247b-122">Specifica l'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2247b-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2247b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2247b-123">-DefaultProfile</span></span>
<span data-ttu-id="2247b-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2247b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2247b-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2247b-125">-OperationId</span></span>
<span data-ttu-id="2247b-126">Specifica l'identificatore dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2247b-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2247b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2247b-127">CommonParameters</span></span>
<span data-ttu-id="2247b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2247b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2247b-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2247b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2247b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2247b-130">INPUTS</span></span>

### <span data-ttu-id="2247b-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2247b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2247b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2247b-132">System.String</span></span>

## <span data-ttu-id="2247b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2247b-133">OUTPUTS</span></span>

### <span data-ttu-id="2247b-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2247b-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="2247b-135">Note</span><span class="sxs-lookup"><span data-stu-id="2247b-135">NOTES</span></span>

## <span data-ttu-id="2247b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2247b-136">RELATED LINKS</span></span>

[<span data-ttu-id="2247b-137">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2247b-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="2247b-138">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2247b-138">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="2247b-139">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2247b-139">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


