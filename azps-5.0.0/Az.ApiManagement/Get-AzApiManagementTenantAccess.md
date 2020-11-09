---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301632"
---
# <span data-ttu-id="bc341-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="bc341-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="bc341-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc341-102">SYNOPSIS</span></span>
<span data-ttu-id="bc341-103">Ottiene la configurazione di Access per un tenant.</span><span class="sxs-lookup"><span data-stu-id="bc341-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="bc341-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc341-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc341-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc341-105">DESCRIPTION</span></span>
<span data-ttu-id="bc341-106">Il cmdlet **Get-AzApiManagementTenantAccess** ottiene la configurazione di accesso del tenant per un tenant.</span><span class="sxs-lookup"><span data-stu-id="bc341-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="bc341-107">I tasti non verranno inclusi nei dettagli dei risultati.</span><span class="sxs-lookup"><span data-stu-id="bc341-107">Keys will not be included into result details.</span></span> <span data-ttu-id="bc341-108">Per ottenere il segreto del client, USA **Get-AzApiManagementTenantAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="bc341-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="bc341-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc341-109">EXAMPLES</span></span>

### <span data-ttu-id="bc341-110">Esempio 1: ottenere la configurazione di accesso del tenant</span><span class="sxs-lookup"><span data-stu-id="bc341-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="bc341-111">Questo comando consente di ottenere la configurazione di accesso del tenant per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="bc341-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="bc341-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc341-112">PARAMETERS</span></span>

### <span data-ttu-id="bc341-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bc341-113">-Context</span></span>
<span data-ttu-id="bc341-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="bc341-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bc341-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc341-115">-DefaultProfile</span></span>
<span data-ttu-id="bc341-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc341-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc341-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc341-117">CommonParameters</span></span>
<span data-ttu-id="bc341-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc341-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc341-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc341-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc341-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc341-120">INPUTS</span></span>

### <span data-ttu-id="bc341-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bc341-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="bc341-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc341-122">OUTPUTS</span></span>

### <span data-ttu-id="bc341-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="bc341-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="bc341-124">Note</span><span class="sxs-lookup"><span data-stu-id="bc341-124">NOTES</span></span>

## <span data-ttu-id="bc341-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc341-125">RELATED LINKS</span></span>

[<span data-ttu-id="bc341-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="bc341-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


