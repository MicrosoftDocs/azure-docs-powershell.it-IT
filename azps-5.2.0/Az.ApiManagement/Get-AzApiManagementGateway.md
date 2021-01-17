---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324545"
---
# <span data-ttu-id="5eb19-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="5eb19-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="5eb19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5eb19-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb19-103">Ottiene tutto o un gateway di gestione API specifico.</span><span class="sxs-lookup"><span data-stu-id="5eb19-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="5eb19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5eb19-104">SYNTAX</span></span>

### <span data-ttu-id="5eb19-105">GetAllGateways (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5eb19-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5eb19-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="5eb19-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eb19-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eb19-107">DESCRIPTION</span></span>
<span data-ttu-id="5eb19-108">Il cmdlet **Get-AzApiManagementGateway** ottiene tutti o un gateway di gestione API specifico.</span><span class="sxs-lookup"><span data-stu-id="5eb19-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="5eb19-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5eb19-109">EXAMPLES</span></span>

### <span data-ttu-id="5eb19-110">Esempio 1: ottenere tutti i gateway</span><span class="sxs-lookup"><span data-stu-id="5eb19-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="5eb19-111">Questo comando consente di ottenere tutti i gateway.</span><span class="sxs-lookup"><span data-stu-id="5eb19-111">This command gets all gateways.</span></span>

### <span data-ttu-id="5eb19-112">Esempio 2: ottenere un gateway tramite ID</span><span class="sxs-lookup"><span data-stu-id="5eb19-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="5eb19-113">Questo comando ottiene il gateway 0123456789.</span><span class="sxs-lookup"><span data-stu-id="5eb19-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="5eb19-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5eb19-114">PARAMETERS</span></span>

### <span data-ttu-id="5eb19-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5eb19-115">-Context</span></span>
<span data-ttu-id="5eb19-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5eb19-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5eb19-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5eb19-117">This parameter is required.</span></span>

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

### <span data-ttu-id="5eb19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb19-118">-DefaultProfile</span></span>
<span data-ttu-id="5eb19-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb19-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eb19-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="5eb19-120">-GatewayId</span></span>
<span data-ttu-id="5eb19-121">Identificatore di un gateway.</span><span class="sxs-lookup"><span data-stu-id="5eb19-121">Identifier of a gateway.</span></span>
<span data-ttu-id="5eb19-122">Se specificato cercherà di trovare il gateway dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="5eb19-122">If specified will try to find gateway by the identifier.</span></span>

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

### <span data-ttu-id="5eb19-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb19-123">CommonParameters</span></span>
<span data-ttu-id="5eb19-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb19-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb19-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5eb19-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb19-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5eb19-126">INPUTS</span></span>

### <span data-ttu-id="5eb19-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5eb19-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5eb19-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5eb19-128">System.String</span></span>

## <span data-ttu-id="5eb19-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5eb19-129">OUTPUTS</span></span>

### <span data-ttu-id="5eb19-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="5eb19-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="5eb19-131">Note</span><span class="sxs-lookup"><span data-stu-id="5eb19-131">NOTES</span></span>

## <span data-ttu-id="5eb19-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5eb19-132">RELATED LINKS</span></span>
