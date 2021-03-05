---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 980adceb2e5a76532c9b3175c015d5f4e3a6b2e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999023"
---
# <span data-ttu-id="1895c-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1895c-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="1895c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1895c-102">SYNOPSIS</span></span>
<span data-ttu-id="1895c-103">Recupera un Gateway di gestione API o uno specifico.</span><span class="sxs-lookup"><span data-stu-id="1895c-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="1895c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1895c-104">SYNTAX</span></span>

### <span data-ttu-id="1895c-105">GetAllGateways (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1895c-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1895c-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="1895c-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1895c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1895c-107">DESCRIPTION</span></span>
<span data-ttu-id="1895c-108">Il **cmdlet Get-AzApiManagementGateway** ottiene un Gateway di gestione DELLE API o uno specifico.</span><span class="sxs-lookup"><span data-stu-id="1895c-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="1895c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1895c-109">EXAMPLES</span></span>

### <span data-ttu-id="1895c-110">Esempio 1: Ottenere tutti i gateway</span><span class="sxs-lookup"><span data-stu-id="1895c-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="1895c-111">Questo comando recupera tutti i gateway.</span><span class="sxs-lookup"><span data-stu-id="1895c-111">This command gets all gateways.</span></span>

### <span data-ttu-id="1895c-112">Esempio 2: Ottenere un gateway in base all'ID</span><span class="sxs-lookup"><span data-stu-id="1895c-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="1895c-113">Questo comando recupera il gateway 0123456789.</span><span class="sxs-lookup"><span data-stu-id="1895c-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="1895c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1895c-114">PARAMETERS</span></span>

### <span data-ttu-id="1895c-115">-Context</span><span class="sxs-lookup"><span data-stu-id="1895c-115">-Context</span></span>
<span data-ttu-id="1895c-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1895c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1895c-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1895c-117">This parameter is required.</span></span>

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

### <span data-ttu-id="1895c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1895c-118">-DefaultProfile</span></span>
<span data-ttu-id="1895c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1895c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1895c-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="1895c-120">-GatewayId</span></span>
<span data-ttu-id="1895c-121">Identificatore di un gateway.</span><span class="sxs-lookup"><span data-stu-id="1895c-121">Identifier of a gateway.</span></span>
<span data-ttu-id="1895c-122">Se specificato, cercherà di trovare il gateway in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="1895c-122">If specified will try to find gateway by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1895c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1895c-123">CommonParameters</span></span>
<span data-ttu-id="1895c-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1895c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1895c-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1895c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1895c-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="1895c-126">INPUTS</span></span>

### <span data-ttu-id="1895c-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1895c-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1895c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1895c-128">System.String</span></span>

## <span data-ttu-id="1895c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1895c-129">OUTPUTS</span></span>

### <span data-ttu-id="1895c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1895c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="1895c-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="1895c-131">NOTES</span></span>

## <span data-ttu-id="1895c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1895c-132">RELATED LINKS</span></span>
