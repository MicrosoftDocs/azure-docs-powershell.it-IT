---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330988"
---
# <span data-ttu-id="61ef5-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="61ef5-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="61ef5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="61ef5-103">Ottiene la configurazione di Access per un tenant.</span><span class="sxs-lookup"><span data-stu-id="61ef5-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="61ef5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61ef5-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61ef5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61ef5-105">DESCRIPTION</span></span>
<span data-ttu-id="61ef5-106">Il cmdlet **Get-AzApiManagementTenantAccess** ottiene la configurazione di accesso del tenant per un tenant.</span><span class="sxs-lookup"><span data-stu-id="61ef5-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="61ef5-107">I tasti non verranno inclusi nei dettagli dei risultati.</span><span class="sxs-lookup"><span data-stu-id="61ef5-107">Keys will not be included into result details.</span></span> <span data-ttu-id="61ef5-108">Per ottenere il segreto del client, USA **Get-AzApiManagementTenantAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="61ef5-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="61ef5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61ef5-109">EXAMPLES</span></span>

### <span data-ttu-id="61ef5-110">Esempio 1: ottenere la configurazione di accesso del tenant</span><span class="sxs-lookup"><span data-stu-id="61ef5-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="61ef5-111">Questo comando consente di ottenere la configurazione di accesso del tenant per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="61ef5-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="61ef5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61ef5-112">PARAMETERS</span></span>

### <span data-ttu-id="61ef5-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="61ef5-113">-Context</span></span>
<span data-ttu-id="61ef5-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="61ef5-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="61ef5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ef5-115">-DefaultProfile</span></span>
<span data-ttu-id="61ef5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61ef5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61ef5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ef5-117">CommonParameters</span></span>
<span data-ttu-id="61ef5-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ef5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ef5-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61ef5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ef5-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61ef5-120">INPUTS</span></span>

### <span data-ttu-id="61ef5-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="61ef5-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="61ef5-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61ef5-122">OUTPUTS</span></span>

### <span data-ttu-id="61ef5-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="61ef5-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="61ef5-124">Note</span><span class="sxs-lookup"><span data-stu-id="61ef5-124">NOTES</span></span>

## <span data-ttu-id="61ef5-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61ef5-125">RELATED LINKS</span></span>

[<span data-ttu-id="61ef5-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="61ef5-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


