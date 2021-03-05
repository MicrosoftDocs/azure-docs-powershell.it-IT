---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 5807925c302f951f9e48c89afcb62634bd774c89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014350"
---
# <span data-ttu-id="2373d-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2373d-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="2373d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2373d-102">SYNOPSIS</span></span>
<span data-ttu-id="2373d-103">Ottiene un elenco o un'operazione API specificata.</span><span class="sxs-lookup"><span data-stu-id="2373d-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="2373d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2373d-104">SYNTAX</span></span>

### <span data-ttu-id="2373d-105">GetAllApiOperations (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2373d-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2373d-106">GetById</span><span class="sxs-lookup"><span data-stu-id="2373d-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2373d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2373d-107">DESCRIPTION</span></span>
<span data-ttu-id="2373d-108">**Get-AzApiManagementOperation** ottiene un elenco o un'operazione API specificata.</span><span class="sxs-lookup"><span data-stu-id="2373d-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="2373d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2373d-109">EXAMPLES</span></span>

### <span data-ttu-id="2373d-110">Esempio 1: Ottenere tutte le operazioni di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="2373d-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="2373d-111">Questo comando recupera tutte le operazioni di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="2373d-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="2373d-112">Esempio 2: Ottenere un'operazione di gestione delle API in base all'ID operazione</span><span class="sxs-lookup"><span data-stu-id="2373d-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="2373d-113">Questo comando recupera un'operazione di gestione API in base all'ID operazione denominato Operation0003.</span><span class="sxs-lookup"><span data-stu-id="2373d-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="2373d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2373d-114">PARAMETERS</span></span>

### <span data-ttu-id="2373d-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2373d-115">-ApiId</span></span>
<span data-ttu-id="2373d-116">Specifica l'identificatore dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="2373d-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="2373d-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="2373d-117">-ApiRevision</span></span>
<span data-ttu-id="2373d-118">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="2373d-118">Identifier of API Revision.</span></span> <span data-ttu-id="2373d-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2373d-119">This parameter is optional.</span></span> <span data-ttu-id="2373d-120">Se non viene specificato, l'operazione verrà recuperata dalla revisione dell'API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="2373d-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="2373d-121">-Context</span><span class="sxs-lookup"><span data-stu-id="2373d-121">-Context</span></span>
<span data-ttu-id="2373d-122">Specifica l'istanza **dell'oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="2373d-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2373d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2373d-123">-DefaultProfile</span></span>
<span data-ttu-id="2373d-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2373d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2373d-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2373d-125">-OperationId</span></span>
<span data-ttu-id="2373d-126">Specifica l'identificatore dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2373d-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="2373d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2373d-127">CommonParameters</span></span>
<span data-ttu-id="2373d-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2373d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2373d-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2373d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2373d-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="2373d-130">INPUTS</span></span>

### <span data-ttu-id="2373d-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2373d-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2373d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2373d-132">System.String</span></span>

## <span data-ttu-id="2373d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2373d-133">OUTPUTS</span></span>

### <span data-ttu-id="2373d-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2373d-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="2373d-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="2373d-135">NOTES</span></span>

## <span data-ttu-id="2373d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2373d-136">RELATED LINKS</span></span>

[<span data-ttu-id="2373d-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2373d-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="2373d-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2373d-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="2373d-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2373d-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


