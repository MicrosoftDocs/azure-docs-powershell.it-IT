---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 0a3d2aeb8c90377f9c7e81ef6a25cef49780e410
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187694"
---
# <span data-ttu-id="99e7c-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="99e7c-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="99e7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="99e7c-103">Ottiene la configurazione di accesso Git per un tenant.</span><span class="sxs-lookup"><span data-stu-id="99e7c-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="99e7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99e7c-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99e7c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="99e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="99e7c-106">Il cmdlet **Get-AzApiManagementTenantGitAccess** ottiene la configurazione di accesso Git per un tenant.</span><span class="sxs-lookup"><span data-stu-id="99e7c-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="99e7c-107">Le chiavi non verranno incluse nei dettagli dei risultati.</span><span class="sxs-lookup"><span data-stu-id="99e7c-107">Keys will not be included into result details.</span></span> <span data-ttu-id="99e7c-108">Per ottenere il segreto client, usare **Get-AzApiManagementTenantGitAccessSecret.**</span><span class="sxs-lookup"><span data-stu-id="99e7c-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="99e7c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="99e7c-110">Esempio 1: Ottenere la configurazione dell'accesso tenant</span><span class="sxs-lookup"><span data-stu-id="99e7c-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="99e7c-111">Questo comando ottiene la configurazione di accesso Git per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="99e7c-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="99e7c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99e7c-112">PARAMETERS</span></span>

### <span data-ttu-id="99e7c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="99e7c-113">-Context</span></span>
<span data-ttu-id="99e7c-114">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="99e7c-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="99e7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e7c-115">-DefaultProfile</span></span>
<span data-ttu-id="99e7c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99e7c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99e7c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e7c-117">CommonParameters</span></span>
<span data-ttu-id="99e7c-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e7c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e7c-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99e7c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e7c-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="99e7c-120">INPUTS</span></span>

### <span data-ttu-id="99e7c-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="99e7c-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="99e7c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99e7c-122">OUTPUTS</span></span>

### <span data-ttu-id="99e7c-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="99e7c-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="99e7c-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="99e7c-124">NOTES</span></span>

## <span data-ttu-id="99e7c-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99e7c-125">RELATED LINKS</span></span>
