---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 471c861e8601317daf1e12de3a292d84bfce416e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004877"
---
# <span data-ttu-id="84bf4-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="84bf4-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="84bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="84bf4-103">Ottiene le chiavi di configurazione di accesso Git per un tenant.</span><span class="sxs-lookup"><span data-stu-id="84bf4-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="84bf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84bf4-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84bf4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="84bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="84bf4-106">Ottiene le chiavi di configurazione di accesso Git per un tenant.</span><span class="sxs-lookup"><span data-stu-id="84bf4-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="84bf4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="84bf4-108">Esempio 1: Ottenere la configurazione dell'accesso tenant</span><span class="sxs-lookup"><span data-stu-id="84bf4-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="84bf4-109">Questo comando ottiene le chiavi di configurazione di accesso Git per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="84bf4-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="84bf4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84bf4-110">PARAMETERS</span></span>

### <span data-ttu-id="84bf4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="84bf4-111">-Context</span></span>
<span data-ttu-id="84bf4-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="84bf4-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="84bf4-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="84bf4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="84bf4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bf4-114">-DefaultProfile</span></span>
<span data-ttu-id="84bf4-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84bf4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84bf4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bf4-116">CommonParameters</span></span>
<span data-ttu-id="84bf4-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84bf4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bf4-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="84bf4-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bf4-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="84bf4-119">INPUTS</span></span>

### <span data-ttu-id="84bf4-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="84bf4-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="84bf4-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84bf4-121">OUTPUTS</span></span>

### <span data-ttu-id="84bf4-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="84bf4-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="84bf4-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="84bf4-123">NOTES</span></span>

## <span data-ttu-id="84bf4-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84bf4-124">RELATED LINKS</span></span>
