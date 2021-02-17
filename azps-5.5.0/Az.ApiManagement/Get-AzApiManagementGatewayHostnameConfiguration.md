---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205779"
---
# <span data-ttu-id="ba8b7-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba8b7-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="ba8b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8b7-103">Recupera tutta la configurazione del nome host o una specifica per il Gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="ba8b7-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="ba8b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba8b7-104">SYNTAX</span></span>

### <span data-ttu-id="ba8b7-105">GetByGatewayId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba8b7-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba8b7-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="ba8b7-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba8b7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ba8b7-107">DESCRIPTION</span></span>
<span data-ttu-id="ba8b7-108">Il cmdlet **Get-AzApiManagementGatewayHostnameConfiguration** ottiene tutta la configurazione del nome host o specifica per il gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="ba8b7-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="ba8b7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba8b7-109">EXAMPLES</span></span>

### <span data-ttu-id="ba8b7-110">Esempio 1: Ottenere tutte le configurazioni dei nomi host per il gateway</span><span class="sxs-lookup"><span data-stu-id="ba8b7-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="ba8b7-111">Questo comando recupera tutte le configurazioni dei nomi host per un gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="ba8b7-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="ba8b7-112">Esempio 2: Ottenere una configurazione del nome host per il gateway</span><span class="sxs-lookup"><span data-stu-id="ba8b7-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="ba8b7-113">Questo comando ottiene la configurazione del nome host "123" per un gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="ba8b7-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="ba8b7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba8b7-114">PARAMETERS</span></span>

### <span data-ttu-id="ba8b7-115">-Context</span><span class="sxs-lookup"><span data-stu-id="ba8b7-115">-Context</span></span>
<span data-ttu-id="ba8b7-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ba8b7-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ba8b7-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ba8b7-117">This parameter is required.</span></span>

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

### <span data-ttu-id="ba8b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8b7-118">-DefaultProfile</span></span>
<span data-ttu-id="ba8b7-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba8b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba8b7-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ba8b7-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="ba8b7-121">Identificatore di configurazione del nome host.</span><span class="sxs-lookup"><span data-stu-id="ba8b7-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="ba8b7-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ba8b7-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="ba8b7-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ba8b7-123">-GatewayId</span></span>
<span data-ttu-id="ba8b7-124">Identificatore del gateway.</span><span class="sxs-lookup"><span data-stu-id="ba8b7-124">Gateway identifier.</span></span>
<span data-ttu-id="ba8b7-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ba8b7-125">This parameter is required.</span></span>

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

### <span data-ttu-id="ba8b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8b7-126">CommonParameters</span></span>
<span data-ttu-id="ba8b7-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba8b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8b7-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba8b7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8b7-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="ba8b7-129">INPUTS</span></span>

### <span data-ttu-id="ba8b7-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ba8b7-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ba8b7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ba8b7-131">System.String</span></span>

## <span data-ttu-id="ba8b7-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba8b7-132">OUTPUTS</span></span>

### <span data-ttu-id="ba8b7-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba8b7-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="ba8b7-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="ba8b7-134">NOTES</span></span>

## <span data-ttu-id="ba8b7-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba8b7-135">RELATED LINKS</span></span>
