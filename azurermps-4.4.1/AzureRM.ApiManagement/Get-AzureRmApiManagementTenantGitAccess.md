---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 69f643f4d2e66f0b5af61a6362e59386b2f79078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520817"
---
# <span data-ttu-id="edeb1-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="edeb1-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="edeb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="edeb1-102">SYNOPSIS</span></span>
<span data-ttu-id="edeb1-103">Ottiene la configurazione di accesso GIT per un tenant.</span><span class="sxs-lookup"><span data-stu-id="edeb1-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edeb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edeb1-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edeb1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edeb1-105">DESCRIPTION</span></span>
<span data-ttu-id="edeb1-106">Il cmdlet **Get-AzureRmApiManagementTenantGitAccess** ottiene la configurazione di accesso GIT per un tenant.</span><span class="sxs-lookup"><span data-stu-id="edeb1-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="edeb1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edeb1-107">EXAMPLES</span></span>

### <span data-ttu-id="edeb1-108">Esempio 1: ottenere la configurazione di accesso del tenant</span><span class="sxs-lookup"><span data-stu-id="edeb1-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $ApimContext
```

<span data-ttu-id="edeb1-109">Questo comando ottiene la configurazione di accesso GIT per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="edeb1-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="edeb1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="edeb1-110">PARAMETERS</span></span>

### <span data-ttu-id="edeb1-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="edeb1-111">-Context</span></span>
<span data-ttu-id="edeb1-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="edeb1-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edeb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edeb1-113">-DefaultProfile</span></span>
<span data-ttu-id="edeb1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="edeb1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edeb1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edeb1-115">CommonParameters</span></span>
<span data-ttu-id="edeb1-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edeb1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edeb1-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edeb1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edeb1-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="edeb1-118">INPUTS</span></span>

## <span data-ttu-id="edeb1-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edeb1-119">OUTPUTS</span></span>

### <span data-ttu-id="edeb1-120">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="edeb1-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="edeb1-121">Note</span><span class="sxs-lookup"><span data-stu-id="edeb1-121">NOTES</span></span>

## <span data-ttu-id="edeb1-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edeb1-122">RELATED LINKS</span></span>

