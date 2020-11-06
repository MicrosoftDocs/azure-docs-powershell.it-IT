---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 28b27ee7a2e24b425d5ffa93be4d1f3513a31c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514592"
---
# <span data-ttu-id="512ed-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="512ed-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="512ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="512ed-102">SYNOPSIS</span></span>
<span data-ttu-id="512ed-103">Ottiene la configurazione di accesso GIT per un tenant.</span><span class="sxs-lookup"><span data-stu-id="512ed-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="512ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="512ed-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="512ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="512ed-105">DESCRIPTION</span></span>
<span data-ttu-id="512ed-106">Il cmdlet **Get-AzureRmApiManagementTenantGitAccess** ottiene la configurazione di accesso GIT per un tenant.</span><span class="sxs-lookup"><span data-stu-id="512ed-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="512ed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="512ed-107">EXAMPLES</span></span>

### <span data-ttu-id="512ed-108">Esempio 1: ottenere la configurazione di accesso del tenant</span><span class="sxs-lookup"><span data-stu-id="512ed-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $apimContext 
```

<span data-ttu-id="512ed-109">Questo comando ottiene la configurazione di accesso GIT per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="512ed-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="512ed-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="512ed-110">PARAMETERS</span></span>

### <span data-ttu-id="512ed-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="512ed-111">-Context</span></span>
<span data-ttu-id="512ed-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="512ed-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512ed-113">-DefaultProfile</span></span>
<span data-ttu-id="512ed-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="512ed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512ed-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512ed-115">CommonParameters</span></span>
<span data-ttu-id="512ed-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="512ed-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512ed-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="512ed-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512ed-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="512ed-118">INPUTS</span></span>

### <span data-ttu-id="512ed-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="512ed-119">None</span></span>
<span data-ttu-id="512ed-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="512ed-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="512ed-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="512ed-121">OUTPUTS</span></span>

### <span data-ttu-id="512ed-122">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="512ed-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="512ed-123">Note</span><span class="sxs-lookup"><span data-stu-id="512ed-123">NOTES</span></span>

## <span data-ttu-id="512ed-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="512ed-124">RELATED LINKS</span></span>

