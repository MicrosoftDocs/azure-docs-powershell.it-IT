---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 30243ef1796e621d0898aae38e29ddb1dc7fd20b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520820"
---
# <span data-ttu-id="2e075-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="2e075-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="2e075-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e075-102">SYNOPSIS</span></span>
<span data-ttu-id="2e075-103">Ottiene la configurazione di Access per un tenant.</span><span class="sxs-lookup"><span data-stu-id="2e075-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e075-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e075-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e075-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e075-105">DESCRIPTION</span></span>
<span data-ttu-id="2e075-106">Il cmdlet **Get-AzureRmApiManagementTenantAccess** ottiene la configurazione di accesso del tenant per un tenant.</span><span class="sxs-lookup"><span data-stu-id="2e075-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="2e075-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e075-107">EXAMPLES</span></span>

### <span data-ttu-id="2e075-108">Esempio 1: ottenere la configurazione di accesso del tenant</span><span class="sxs-lookup"><span data-stu-id="2e075-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $ApimContext
```

<span data-ttu-id="2e075-109">Questo comando consente di ottenere la configurazione di accesso del tenant per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="2e075-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="2e075-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e075-110">PARAMETERS</span></span>

### <span data-ttu-id="2e075-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2e075-111">-Context</span></span>
<span data-ttu-id="2e075-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2e075-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2e075-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e075-113">-DefaultProfile</span></span>
<span data-ttu-id="2e075-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e075-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e075-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e075-115">CommonParameters</span></span>
<span data-ttu-id="2e075-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e075-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e075-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e075-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e075-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e075-118">INPUTS</span></span>

## <span data-ttu-id="2e075-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e075-119">OUTPUTS</span></span>

### <span data-ttu-id="2e075-120">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="2e075-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="2e075-121">Note</span><span class="sxs-lookup"><span data-stu-id="2e075-121">NOTES</span></span>

## <span data-ttu-id="2e075-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e075-122">RELATED LINKS</span></span>

[<span data-ttu-id="2e075-123">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="2e075-123">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


