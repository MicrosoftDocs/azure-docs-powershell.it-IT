---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330979"
---
# <span data-ttu-id="3637e-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="3637e-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="3637e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3637e-102">SYNOPSIS</span></span>
<span data-ttu-id="3637e-103">Ottiene le chiavi di configurazione di Access per un tenant.</span><span class="sxs-lookup"><span data-stu-id="3637e-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="3637e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3637e-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3637e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3637e-105">DESCRIPTION</span></span>
<span data-ttu-id="3637e-106">Ottiene le chiavi di configurazione di Access per un tenant.</span><span class="sxs-lookup"><span data-stu-id="3637e-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="3637e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3637e-107">EXAMPLES</span></span>

### <span data-ttu-id="3637e-108">Esempio 1: ottenere le chiavi di configurazione dell'accesso tenant</span><span class="sxs-lookup"><span data-stu-id="3637e-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="3637e-109">Questo comando ottiene le chiavi di configurazione dell'accesso del tenant per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="3637e-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="3637e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3637e-110">PARAMETERS</span></span>

### <span data-ttu-id="3637e-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3637e-111">-Context</span></span>
<span data-ttu-id="3637e-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3637e-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3637e-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3637e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3637e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3637e-114">-DefaultProfile</span></span>
<span data-ttu-id="3637e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3637e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3637e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3637e-116">CommonParameters</span></span>
<span data-ttu-id="3637e-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3637e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3637e-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3637e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3637e-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3637e-119">INPUTS</span></span>

### <span data-ttu-id="3637e-120">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3637e-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="3637e-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3637e-121">OUTPUTS</span></span>

### <span data-ttu-id="3637e-122">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="3637e-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="3637e-123">Note</span><span class="sxs-lookup"><span data-stu-id="3637e-123">NOTES</span></span>

## <span data-ttu-id="3637e-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3637e-124">RELATED LINKS</span></span>
