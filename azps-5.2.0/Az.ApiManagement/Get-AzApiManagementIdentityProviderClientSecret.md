---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365858"
---
# <span data-ttu-id="82b02-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="82b02-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="82b02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82b02-102">SYNOPSIS</span></span>
<span data-ttu-id="82b02-103">Ottenere il segreto del client del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="82b02-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="82b02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82b02-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82b02-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82b02-105">DESCRIPTION</span></span>
<span data-ttu-id="82b02-106">Ottenere il segreto del client del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="82b02-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="82b02-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82b02-107">EXAMPLES</span></span>

### <span data-ttu-id="82b02-108">Esempio 1: ottenere il segreto client del provider di identità di tipo AAD</span><span class="sxs-lookup"><span data-stu-id="82b02-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="82b02-109">Ottiene il segreto client della configurazione del provider di identità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="82b02-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="82b02-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82b02-110">PARAMETERS</span></span>

### <span data-ttu-id="82b02-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="82b02-111">-Context</span></span>
<span data-ttu-id="82b02-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="82b02-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="82b02-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="82b02-113">This parameter is required.</span></span>

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

### <span data-ttu-id="82b02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b02-114">-DefaultProfile</span></span>
<span data-ttu-id="82b02-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82b02-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b02-116">-Digitare</span><span class="sxs-lookup"><span data-stu-id="82b02-116">-Type</span></span>
<span data-ttu-id="82b02-117">Identificatore di un provider di identità.</span><span class="sxs-lookup"><span data-stu-id="82b02-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="82b02-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="82b02-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b02-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b02-119">CommonParameters</span></span>
<span data-ttu-id="82b02-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82b02-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b02-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82b02-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b02-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82b02-122">INPUTS</span></span>

### <span data-ttu-id="82b02-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="82b02-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="82b02-124">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="82b02-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="82b02-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82b02-125">OUTPUTS</span></span>

### <span data-ttu-id="82b02-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="82b02-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="82b02-127">Note</span><span class="sxs-lookup"><span data-stu-id="82b02-127">NOTES</span></span>

## <span data-ttu-id="82b02-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82b02-128">RELATED LINKS</span></span>
