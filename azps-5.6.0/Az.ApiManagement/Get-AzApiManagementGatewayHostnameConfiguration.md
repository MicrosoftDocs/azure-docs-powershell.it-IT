---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 27e833c526dea1b8df6451671ae2fd142c00b6e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981326"
---
# <span data-ttu-id="dad6e-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="dad6e-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="dad6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad6e-102">SYNOPSIS</span></span>
<span data-ttu-id="dad6e-103">Recupera tutta la configurazione del nome host o una specifica per il Gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="dad6e-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="dad6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dad6e-104">SYNTAX</span></span>

### <span data-ttu-id="dad6e-105">GetByGatewayId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dad6e-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dad6e-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="dad6e-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dad6e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dad6e-107">DESCRIPTION</span></span>
<span data-ttu-id="dad6e-108">Il cmdlet **Get-AzApiManagementGatewayHostnameConfiguration** ottiene tutta la configurazione del nome host o specifica per il gateway esistente.</span><span class="sxs-lookup"><span data-stu-id="dad6e-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="dad6e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dad6e-109">EXAMPLES</span></span>

### <span data-ttu-id="dad6e-110">Esempio 1: Ottenere tutte le configurazioni dei nomi host per il gateway</span><span class="sxs-lookup"><span data-stu-id="dad6e-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="dad6e-111">Questo comando recupera tutte le configurazioni dei nomi host per un gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="dad6e-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="dad6e-112">Esempio 2: Ottenere una configurazione del nome host per il gateway</span><span class="sxs-lookup"><span data-stu-id="dad6e-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="dad6e-113">Questo comando ottiene la configurazione del nome host "123" per un gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="dad6e-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="dad6e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dad6e-114">PARAMETERS</span></span>

### <span data-ttu-id="dad6e-115">-Context</span><span class="sxs-lookup"><span data-stu-id="dad6e-115">-Context</span></span>
<span data-ttu-id="dad6e-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dad6e-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dad6e-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="dad6e-117">This parameter is required.</span></span>

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

### <span data-ttu-id="dad6e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad6e-118">-DefaultProfile</span></span>
<span data-ttu-id="dad6e-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dad6e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad6e-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dad6e-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="dad6e-121">Identificatore di configurazione del nome host.</span><span class="sxs-lookup"><span data-stu-id="dad6e-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="dad6e-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dad6e-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="dad6e-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="dad6e-123">-GatewayId</span></span>
<span data-ttu-id="dad6e-124">Identificatore del gateway.</span><span class="sxs-lookup"><span data-stu-id="dad6e-124">Gateway identifier.</span></span>
<span data-ttu-id="dad6e-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="dad6e-125">This parameter is required.</span></span>

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

### <span data-ttu-id="dad6e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad6e-126">CommonParameters</span></span>
<span data-ttu-id="dad6e-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad6e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad6e-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dad6e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad6e-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="dad6e-129">INPUTS</span></span>

### <span data-ttu-id="dad6e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dad6e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dad6e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="dad6e-131">System.String</span></span>

## <span data-ttu-id="dad6e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dad6e-132">OUTPUTS</span></span>

### <span data-ttu-id="dad6e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="dad6e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="dad6e-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="dad6e-134">NOTES</span></span>

## <span data-ttu-id="dad6e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dad6e-135">RELATED LINKS</span></span>
