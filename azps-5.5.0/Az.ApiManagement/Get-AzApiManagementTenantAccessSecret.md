---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187703"
---
# <span data-ttu-id="c065d-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="c065d-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="c065d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c065d-102">SYNOPSIS</span></span>
<span data-ttu-id="c065d-103">Ottiene le chiavi di configurazione di accesso per un tenant.</span><span class="sxs-lookup"><span data-stu-id="c065d-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="c065d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c065d-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c065d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c065d-105">DESCRIPTION</span></span>
<span data-ttu-id="c065d-106">Ottiene le chiavi di configurazione di accesso per un tenant.</span><span class="sxs-lookup"><span data-stu-id="c065d-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="c065d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c065d-107">EXAMPLES</span></span>

### <span data-ttu-id="c065d-108">Esempio 1: Ottenere le chiavi di configurazione dell'accesso tenant</span><span class="sxs-lookup"><span data-stu-id="c065d-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="c065d-109">Questo comando recupera le chiavi di configurazione dell'accesso tenant per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="c065d-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="c065d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c065d-110">PARAMETERS</span></span>

### <span data-ttu-id="c065d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c065d-111">-Context</span></span>
<span data-ttu-id="c065d-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c065d-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c065d-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c065d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c065d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c065d-114">-DefaultProfile</span></span>
<span data-ttu-id="c065d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c065d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c065d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c065d-116">CommonParameters</span></span>
<span data-ttu-id="c065d-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c065d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c065d-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c065d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c065d-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="c065d-119">INPUTS</span></span>

### <span data-ttu-id="c065d-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c065d-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="c065d-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c065d-121">OUTPUTS</span></span>

### <span data-ttu-id="c065d-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="c065d-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="c065d-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="c065d-123">NOTES</span></span>

## <span data-ttu-id="c065d-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c065d-124">RELATED LINKS</span></span>
