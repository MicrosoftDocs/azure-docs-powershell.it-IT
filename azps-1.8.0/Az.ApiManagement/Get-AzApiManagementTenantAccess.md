---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 2418ec3f5e9570046c37c76bdaef8f853ff819b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673623"
---
# <span data-ttu-id="46a07-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="46a07-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="46a07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46a07-102">SYNOPSIS</span></span>
<span data-ttu-id="46a07-103">Ottiene la configurazione di Access per un tenant.</span><span class="sxs-lookup"><span data-stu-id="46a07-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="46a07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46a07-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46a07-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46a07-105">DESCRIPTION</span></span>
<span data-ttu-id="46a07-106">Il cmdlet **Get-AzApiManagementTenantAccess** ottiene la configurazione di accesso del tenant per un tenant.</span><span class="sxs-lookup"><span data-stu-id="46a07-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="46a07-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46a07-107">EXAMPLES</span></span>

### <span data-ttu-id="46a07-108">Esempio 1: ottenere la configurazione di accesso del tenant</span><span class="sxs-lookup"><span data-stu-id="46a07-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="46a07-109">Questo comando consente di ottenere la configurazione di accesso del tenant per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="46a07-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="46a07-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46a07-110">PARAMETERS</span></span>

### <span data-ttu-id="46a07-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="46a07-111">-Context</span></span>
<span data-ttu-id="46a07-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="46a07-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="46a07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a07-113">-DefaultProfile</span></span>
<span data-ttu-id="46a07-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46a07-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46a07-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a07-115">CommonParameters</span></span>
<span data-ttu-id="46a07-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a07-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a07-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a07-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a07-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46a07-118">INPUTS</span></span>

### <span data-ttu-id="46a07-119">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="46a07-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="46a07-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46a07-120">OUTPUTS</span></span>

### <span data-ttu-id="46a07-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="46a07-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="46a07-122">Note</span><span class="sxs-lookup"><span data-stu-id="46a07-122">NOTES</span></span>

## <span data-ttu-id="46a07-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46a07-123">RELATED LINKS</span></span>

[<span data-ttu-id="46a07-124">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="46a07-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


