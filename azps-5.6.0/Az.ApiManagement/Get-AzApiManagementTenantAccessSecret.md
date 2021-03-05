---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: 56246de86606aeb07dd8ccdbcfbf2dc35b32a5a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004894"
---
# <span data-ttu-id="84fe7-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="84fe7-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="84fe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="84fe7-103">Ottiene le chiavi di configurazione di accesso per un tenant.</span><span class="sxs-lookup"><span data-stu-id="84fe7-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="84fe7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84fe7-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84fe7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="84fe7-105">DESCRIPTION</span></span>
<span data-ttu-id="84fe7-106">Ottiene le chiavi di configurazione di accesso per un tenant.</span><span class="sxs-lookup"><span data-stu-id="84fe7-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="84fe7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84fe7-107">EXAMPLES</span></span>

### <span data-ttu-id="84fe7-108">Esempio 1: Ottenere le chiavi di configurazione dell'accesso tenant</span><span class="sxs-lookup"><span data-stu-id="84fe7-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="84fe7-109">Questo comando recupera le chiavi di configurazione dell'accesso tenant per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="84fe7-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="84fe7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84fe7-110">PARAMETERS</span></span>

### <span data-ttu-id="84fe7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="84fe7-111">-Context</span></span>
<span data-ttu-id="84fe7-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="84fe7-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="84fe7-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="84fe7-113">This parameter is required.</span></span>

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

### <span data-ttu-id="84fe7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84fe7-114">-DefaultProfile</span></span>
<span data-ttu-id="84fe7-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84fe7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84fe7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84fe7-116">CommonParameters</span></span>
<span data-ttu-id="84fe7-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84fe7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84fe7-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="84fe7-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84fe7-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="84fe7-119">INPUTS</span></span>

### <span data-ttu-id="84fe7-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="84fe7-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="84fe7-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84fe7-121">OUTPUTS</span></span>

### <span data-ttu-id="84fe7-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="84fe7-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="84fe7-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="84fe7-123">NOTES</span></span>

## <span data-ttu-id="84fe7-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84fe7-124">RELATED LINKS</span></span>
