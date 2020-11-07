---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 2fe14349b179634bf93050840271d4d4b6905b3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673622"
---
# <span data-ttu-id="903b2-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="903b2-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="903b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="903b2-102">SYNOPSIS</span></span>
<span data-ttu-id="903b2-103">Ottiene la configurazione di accesso GIT per un tenant.</span><span class="sxs-lookup"><span data-stu-id="903b2-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="903b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="903b2-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="903b2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="903b2-105">DESCRIPTION</span></span>
<span data-ttu-id="903b2-106">Il cmdlet **Get-AzApiManagementTenantGitAccess** ottiene la configurazione di accesso GIT per un tenant.</span><span class="sxs-lookup"><span data-stu-id="903b2-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="903b2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="903b2-107">EXAMPLES</span></span>

### <span data-ttu-id="903b2-108">Esempio 1: ottenere la configurazione di accesso del tenant</span><span class="sxs-lookup"><span data-stu-id="903b2-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

<span data-ttu-id="903b2-109">Questo comando ottiene la configurazione di accesso GIT per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="903b2-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="903b2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="903b2-110">PARAMETERS</span></span>

### <span data-ttu-id="903b2-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="903b2-111">-Context</span></span>
<span data-ttu-id="903b2-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="903b2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="903b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903b2-113">-DefaultProfile</span></span>
<span data-ttu-id="903b2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="903b2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="903b2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903b2-115">CommonParameters</span></span>
<span data-ttu-id="903b2-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="903b2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903b2-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="903b2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903b2-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="903b2-118">INPUTS</span></span>

### <span data-ttu-id="903b2-119">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="903b2-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="903b2-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="903b2-120">OUTPUTS</span></span>

### <span data-ttu-id="903b2-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="903b2-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="903b2-122">Note</span><span class="sxs-lookup"><span data-stu-id="903b2-122">NOTES</span></span>

## <span data-ttu-id="903b2-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="903b2-123">RELATED LINKS</span></span>
