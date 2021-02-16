---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178110"
---
# <span data-ttu-id="ed6d5-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="ed6d5-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="ed6d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6d5-103">Ottiene le chiavi di configurazione di accesso Git per un tenant.</span><span class="sxs-lookup"><span data-stu-id="ed6d5-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="ed6d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed6d5-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed6d5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ed6d5-105">DESCRIPTION</span></span>
<span data-ttu-id="ed6d5-106">Ottiene le chiavi di configurazione di accesso Git per un tenant.</span><span class="sxs-lookup"><span data-stu-id="ed6d5-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="ed6d5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed6d5-107">EXAMPLES</span></span>

### <span data-ttu-id="ed6d5-108">Esempio 1: Ottenere la configurazione dell'accesso tenant</span><span class="sxs-lookup"><span data-stu-id="ed6d5-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="ed6d5-109">Questo comando ottiene le chiavi di configurazione di accesso Git per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="ed6d5-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="ed6d5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed6d5-110">PARAMETERS</span></span>

### <span data-ttu-id="ed6d5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ed6d5-111">-Context</span></span>
<span data-ttu-id="ed6d5-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ed6d5-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ed6d5-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed6d5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ed6d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6d5-114">-DefaultProfile</span></span>
<span data-ttu-id="ed6d5-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed6d5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed6d5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6d5-116">CommonParameters</span></span>
<span data-ttu-id="ed6d5-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed6d5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6d5-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ed6d5-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6d5-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="ed6d5-119">INPUTS</span></span>

### <span data-ttu-id="ed6d5-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ed6d5-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="ed6d5-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed6d5-121">OUTPUTS</span></span>

### <span data-ttu-id="ed6d5-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="ed6d5-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="ed6d5-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="ed6d5-123">NOTES</span></span>

## <span data-ttu-id="ed6d5-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed6d5-124">RELATED LINKS</span></span>
