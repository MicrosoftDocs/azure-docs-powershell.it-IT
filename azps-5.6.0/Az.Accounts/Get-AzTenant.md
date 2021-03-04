---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 4ef371f26eeca71edda42a6aca5e7d5ad28fe753
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955037"
---
# <span data-ttu-id="8bea8-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="8bea8-101">Get-AzTenant</span></span>

## <span data-ttu-id="8bea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bea8-102">SYNOPSIS</span></span>
<span data-ttu-id="8bea8-103">Ottiene i tenant autorizzati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="8bea8-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="8bea8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bea8-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bea8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8bea8-105">DESCRIPTION</span></span>
<span data-ttu-id="8bea8-106">Il Get-AzTenant cmdlet ottiene i tenant autorizzati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="8bea8-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="8bea8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bea8-107">EXAMPLES</span></span>

### <span data-ttu-id="8bea8-108">Esempio 1: Ottenere tutti i tenant</span><span class="sxs-lookup"><span data-stu-id="8bea8-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="8bea8-109">Questo esempio mostra come ottenere tutti i tenant autorizzati di un account Azure.</span><span class="sxs-lookup"><span data-stu-id="8bea8-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="8bea8-110">Esempio 2: Ottenere un tenant specifico</span><span class="sxs-lookup"><span data-stu-id="8bea8-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="8bea8-111">Questo esempio mostra come ottenere un tenant autorizzato specifico di un account azure.</span><span class="sxs-lookup"><span data-stu-id="8bea8-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="8bea8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bea8-112">PARAMETERS</span></span>

### <span data-ttu-id="8bea8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bea8-113">-DefaultProfile</span></span>
<span data-ttu-id="8bea8-114">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8bea8-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bea8-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="8bea8-115">-TenantId</span></span>
<span data-ttu-id="8bea8-116">Specifica l'ID del tenant che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bea8-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bea8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bea8-117">CommonParameters</span></span>
<span data-ttu-id="8bea8-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bea8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bea8-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8bea8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bea8-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="8bea8-120">INPUTS</span></span>

### <span data-ttu-id="8bea8-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8bea8-121">System.String</span></span>

## <span data-ttu-id="8bea8-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bea8-122">OUTPUTS</span></span>

### <span data-ttu-id="8bea8-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="8bea8-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="8bea8-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="8bea8-124">NOTES</span></span>

## <span data-ttu-id="8bea8-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bea8-125">RELATED LINKS</span></span>
