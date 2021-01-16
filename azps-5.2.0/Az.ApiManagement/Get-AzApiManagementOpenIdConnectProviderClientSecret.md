---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322582"
---
# <span data-ttu-id="7c0d4-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="7c0d4-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="7c0d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0d4-103">Ottiene il segreto client OpenID Connect provider.</span><span class="sxs-lookup"><span data-stu-id="7c0d4-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="7c0d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c0d4-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c0d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c0d4-105">DESCRIPTION</span></span>
<span data-ttu-id="7c0d4-106">Ottiene il segreto client OpenID Connect provider.</span><span class="sxs-lookup"><span data-stu-id="7c0d4-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="7c0d4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c0d4-107">EXAMPLES</span></span>

### <span data-ttu-id="7c0d4-108">Esempio 1: ottenere un segreto del client del provider utilizzando un ID</span><span class="sxs-lookup"><span data-stu-id="7c0d4-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="7c0d4-109">Questo comando ottiene un segreto client del provider con ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="7c0d4-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="7c0d4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c0d4-110">PARAMETERS</span></span>

### <span data-ttu-id="7c0d4-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7c0d4-111">-Context</span></span>
<span data-ttu-id="7c0d4-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7c0d4-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7c0d4-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c0d4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7c0d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c0d4-114">-DefaultProfile</span></span>
<span data-ttu-id="7c0d4-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c0d4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c0d4-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="7c0d4-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="7c0d4-117">Identificatore di un provider di connessione OpenID.</span><span class="sxs-lookup"><span data-stu-id="7c0d4-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="7c0d4-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c0d4-118">This parameter is required.</span></span>

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

### <span data-ttu-id="7c0d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0d4-119">CommonParameters</span></span>
<span data-ttu-id="7c0d4-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c0d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0d4-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c0d4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0d4-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c0d4-122">INPUTS</span></span>

### <span data-ttu-id="7c0d4-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7c0d4-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7c0d4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7c0d4-124">System.String</span></span>

## <span data-ttu-id="7c0d4-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c0d4-125">OUTPUTS</span></span>

### <span data-ttu-id="7c0d4-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="7c0d4-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="7c0d4-127">Note</span><span class="sxs-lookup"><span data-stu-id="7c0d4-127">NOTES</span></span>

## <span data-ttu-id="7c0d4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c0d4-128">RELATED LINKS</span></span>
