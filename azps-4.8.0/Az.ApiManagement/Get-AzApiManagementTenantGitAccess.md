---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 0a3d2aeb8c90377f9c7e81ef6a25cef49780e410
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032720"
---
# <span data-ttu-id="3dc55-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="3dc55-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="3dc55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dc55-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc55-103">Ottiene la configurazione di accesso GIT per un tenant.</span><span class="sxs-lookup"><span data-stu-id="3dc55-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="3dc55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dc55-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dc55-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dc55-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc55-106">Il cmdlet **Get-AzApiManagementTenantGitAccess** ottiene la configurazione di accesso GIT per un tenant.</span><span class="sxs-lookup"><span data-stu-id="3dc55-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="3dc55-107">I tasti non verranno inclusi nei dettagli dei risultati.</span><span class="sxs-lookup"><span data-stu-id="3dc55-107">Keys will not be included into result details.</span></span> <span data-ttu-id="3dc55-108">Per ottenere il segreto del client, USA **Get-AzApiManagementTenantGitAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="3dc55-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="3dc55-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dc55-109">EXAMPLES</span></span>

### <span data-ttu-id="3dc55-110">Esempio 1: ottenere la configurazione di accesso del tenant</span><span class="sxs-lookup"><span data-stu-id="3dc55-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="3dc55-111">Questo comando ottiene la configurazione di accesso GIT per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="3dc55-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="3dc55-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dc55-112">PARAMETERS</span></span>

### <span data-ttu-id="3dc55-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3dc55-113">-Context</span></span>
<span data-ttu-id="3dc55-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3dc55-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3dc55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc55-115">-DefaultProfile</span></span>
<span data-ttu-id="3dc55-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc55-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dc55-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc55-117">CommonParameters</span></span>
<span data-ttu-id="3dc55-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc55-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc55-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dc55-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc55-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dc55-120">INPUTS</span></span>

### <span data-ttu-id="3dc55-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3dc55-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="3dc55-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dc55-122">OUTPUTS</span></span>

### <span data-ttu-id="3dc55-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="3dc55-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="3dc55-124">Note</span><span class="sxs-lookup"><span data-stu-id="3dc55-124">NOTES</span></span>

## <span data-ttu-id="3dc55-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dc55-125">RELATED LINKS</span></span>
