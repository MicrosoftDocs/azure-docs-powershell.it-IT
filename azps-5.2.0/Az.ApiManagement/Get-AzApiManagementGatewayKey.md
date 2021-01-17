---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365438"
---
# <span data-ttu-id="ac514-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="ac514-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="ac514-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac514-102">SYNOPSIS</span></span>
<span data-ttu-id="ac514-103">Ottiene le chiavi del gateway esistente</span><span class="sxs-lookup"><span data-stu-id="ac514-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="ac514-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac514-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac514-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac514-105">DESCRIPTION</span></span>
<span data-ttu-id="ac514-106">Il cmdlet **Get-AzApiManagementGatewayKey** ottiene le chiavi del gateway esistente</span><span class="sxs-lookup"><span data-stu-id="ac514-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="ac514-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac514-107">EXAMPLES</span></span>

### <span data-ttu-id="ac514-108">Esempio 2: ottenere un gateway tramite ID</span><span class="sxs-lookup"><span data-stu-id="ac514-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="ac514-109">Questo comando consente di ottenere le chiavi per un gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="ac514-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="ac514-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac514-110">PARAMETERS</span></span>

### <span data-ttu-id="ac514-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ac514-111">-Context</span></span>
<span data-ttu-id="ac514-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ac514-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ac514-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ac514-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ac514-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac514-114">-DefaultProfile</span></span>
<span data-ttu-id="ac514-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac514-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac514-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ac514-116">-GatewayId</span></span>
<span data-ttu-id="ac514-117">Identificatore gateway.</span><span class="sxs-lookup"><span data-stu-id="ac514-117">Gateway identifier.</span></span>
<span data-ttu-id="ac514-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ac514-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ac514-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac514-119">CommonParameters</span></span>
<span data-ttu-id="ac514-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac514-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac514-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac514-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac514-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac514-122">INPUTS</span></span>

### <span data-ttu-id="ac514-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ac514-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ac514-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ac514-124">System.String</span></span>

## <span data-ttu-id="ac514-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac514-125">OUTPUTS</span></span>

### <span data-ttu-id="ac514-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="ac514-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="ac514-127">Note</span><span class="sxs-lookup"><span data-stu-id="ac514-127">NOTES</span></span>

## <span data-ttu-id="ac514-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac514-128">RELATED LINKS</span></span>
