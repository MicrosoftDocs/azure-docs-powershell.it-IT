---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302203"
---
# <span data-ttu-id="a04bb-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a04bb-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="a04bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a04bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a04bb-103">Ottiene un elenco o un'operazione API specificata.</span><span class="sxs-lookup"><span data-stu-id="a04bb-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="a04bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a04bb-104">SYNTAX</span></span>

### <span data-ttu-id="a04bb-105">GetAllApiOperations (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a04bb-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a04bb-106">GetById</span><span class="sxs-lookup"><span data-stu-id="a04bb-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a04bb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a04bb-107">DESCRIPTION</span></span>
<span data-ttu-id="a04bb-108">Il comando **Get-AzApiManagementOperation** ottiene un elenco o un'operazione API specificata.</span><span class="sxs-lookup"><span data-stu-id="a04bb-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="a04bb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a04bb-109">EXAMPLES</span></span>

### <span data-ttu-id="a04bb-110">Esempio 1: ottenere tutte le operazioni di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="a04bb-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="a04bb-111">Questo comando consente di ottenere tutte le operazioni di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="a04bb-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="a04bb-112">Esempio 2: ottenere un'operazione di gestione delle API tramite ID operazione</span><span class="sxs-lookup"><span data-stu-id="a04bb-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="a04bb-113">Questo comando ottiene un'operazione di gestione delle API tramite l'ID operazione denominato Operation0003.</span><span class="sxs-lookup"><span data-stu-id="a04bb-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="a04bb-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a04bb-114">PARAMETERS</span></span>

### <span data-ttu-id="a04bb-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a04bb-115">-ApiId</span></span>
<span data-ttu-id="a04bb-116">Specifica l'identificatore dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="a04bb-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="a04bb-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a04bb-117">-ApiRevision</span></span>
<span data-ttu-id="a04bb-118">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="a04bb-118">Identifier of API Revision.</span></span> <span data-ttu-id="a04bb-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a04bb-119">This parameter is optional.</span></span> <span data-ttu-id="a04bb-120">Se non specificato, l'operazione verrà recuperata dalla revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="a04bb-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="a04bb-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a04bb-121">-Context</span></span>
<span data-ttu-id="a04bb-122">Specifica l'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a04bb-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a04bb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a04bb-123">-DefaultProfile</span></span>
<span data-ttu-id="a04bb-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a04bb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a04bb-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a04bb-125">-OperationId</span></span>
<span data-ttu-id="a04bb-126">Specifica l'identificatore dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a04bb-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="a04bb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a04bb-127">CommonParameters</span></span>
<span data-ttu-id="a04bb-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a04bb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a04bb-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a04bb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a04bb-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a04bb-130">INPUTS</span></span>

### <span data-ttu-id="a04bb-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a04bb-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a04bb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a04bb-132">System.String</span></span>

## <span data-ttu-id="a04bb-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a04bb-133">OUTPUTS</span></span>

### <span data-ttu-id="a04bb-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a04bb-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="a04bb-135">Note</span><span class="sxs-lookup"><span data-stu-id="a04bb-135">NOTES</span></span>

## <span data-ttu-id="a04bb-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a04bb-136">RELATED LINKS</span></span>

[<span data-ttu-id="a04bb-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a04bb-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="a04bb-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a04bb-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="a04bb-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a04bb-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


