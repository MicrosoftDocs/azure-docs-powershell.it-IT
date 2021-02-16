---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201318"
---
# <span data-ttu-id="7dfb6-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="7dfb6-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="7dfb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dfb6-102">SYNOPSIS</span></span>
<span data-ttu-id="7dfb6-103">Recupera il segreto client del provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="7dfb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7dfb6-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dfb6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7dfb6-105">DESCRIPTION</span></span>
<span data-ttu-id="7dfb6-106">Recupera il segreto client del provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="7dfb6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7dfb6-107">EXAMPLES</span></span>

### <span data-ttu-id="7dfb6-108">Esempio 1: Ottenere un segreto client del provider usando un ID</span><span class="sxs-lookup"><span data-stu-id="7dfb6-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="7dfb6-109">Questo comando ottiene un segreto client del provider con ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="7dfb6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dfb6-110">PARAMETERS</span></span>

### <span data-ttu-id="7dfb6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7dfb6-111">-Context</span></span>
<span data-ttu-id="7dfb6-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7dfb6-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7dfb6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dfb6-114">-DefaultProfile</span></span>
<span data-ttu-id="7dfb6-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dfb6-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="7dfb6-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="7dfb6-117">Identificatore di un provider di connessione OpenID.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="7dfb6-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-118">This parameter is required.</span></span>

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

### <span data-ttu-id="7dfb6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dfb6-119">CommonParameters</span></span>
<span data-ttu-id="7dfb6-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dfb6-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7dfb6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dfb6-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="7dfb6-122">INPUTS</span></span>

### <span data-ttu-id="7dfb6-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7dfb6-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7dfb6-124">System.String</span><span class="sxs-lookup"><span data-stu-id="7dfb6-124">System.String</span></span>

## <span data-ttu-id="7dfb6-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7dfb6-125">OUTPUTS</span></span>

### <span data-ttu-id="7dfb6-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="7dfb6-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="7dfb6-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="7dfb6-127">NOTES</span></span>

## <span data-ttu-id="7dfb6-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7dfb6-128">RELATED LINKS</span></span>
