---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365441"
---
# <span data-ttu-id="7bc40-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bc40-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="7bc40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7bc40-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc40-103">Ottiene la configurazione di un nome host tutto o specifico per il gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="7bc40-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="7bc40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bc40-104">SYNTAX</span></span>

### <span data-ttu-id="7bc40-105">GetByGatewayId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7bc40-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bc40-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="7bc40-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bc40-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bc40-107">DESCRIPTION</span></span>
<span data-ttu-id="7bc40-108">Il cmdlet **Get-AzApiManagementGatewayHostnameConfiguration** ottiene tutta la configurazione di un hostname specifico per il gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="7bc40-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="7bc40-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bc40-109">EXAMPLES</span></span>

### <span data-ttu-id="7bc40-110">Esempio 1: ottenere tutte le configurazioni del nome host per il gateway</span><span class="sxs-lookup"><span data-stu-id="7bc40-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="7bc40-111">Questo comando consente di ottenere tutte le configurazioni hostname per un gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="7bc40-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="7bc40-112">Esempio 2: ottenere una configurazione hostname per il gateway</span><span class="sxs-lookup"><span data-stu-id="7bc40-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="7bc40-113">Questo comando ottiene la configurazione hostname "123" per un gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="7bc40-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="7bc40-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7bc40-114">PARAMETERS</span></span>

### <span data-ttu-id="7bc40-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7bc40-115">-Context</span></span>
<span data-ttu-id="7bc40-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7bc40-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7bc40-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7bc40-117">This parameter is required.</span></span>

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

### <span data-ttu-id="7bc40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc40-118">-DefaultProfile</span></span>
<span data-ttu-id="7bc40-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc40-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bc40-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7bc40-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="7bc40-121">Identificatore di configurazione hostname.</span><span class="sxs-lookup"><span data-stu-id="7bc40-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="7bc40-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7bc40-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc40-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="7bc40-123">-GatewayId</span></span>
<span data-ttu-id="7bc40-124">Identificatore gateway.</span><span class="sxs-lookup"><span data-stu-id="7bc40-124">Gateway identifier.</span></span>
<span data-ttu-id="7bc40-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7bc40-125">This parameter is required.</span></span>

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

### <span data-ttu-id="7bc40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc40-126">CommonParameters</span></span>
<span data-ttu-id="7bc40-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc40-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bc40-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc40-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7bc40-129">INPUTS</span></span>

### <span data-ttu-id="7bc40-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7bc40-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7bc40-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7bc40-131">System.String</span></span>

## <span data-ttu-id="7bc40-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bc40-132">OUTPUTS</span></span>

### <span data-ttu-id="7bc40-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bc40-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="7bc40-134">Note</span><span class="sxs-lookup"><span data-stu-id="7bc40-134">NOTES</span></span>

## <span data-ttu-id="7bc40-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bc40-135">RELATED LINKS</span></span>
