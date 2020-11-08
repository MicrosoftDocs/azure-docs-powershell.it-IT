---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199950"
---
# <span data-ttu-id="af142-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="af142-101">Get-AzTenant</span></span>

## <span data-ttu-id="af142-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af142-102">SYNOPSIS</span></span>
<span data-ttu-id="af142-103">Ottiene i tenant autorizzati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="af142-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="af142-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af142-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af142-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af142-105">DESCRIPTION</span></span>
<span data-ttu-id="af142-106">Il cmdlet Get-AzTenant ottiene i tenant autorizzati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="af142-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="af142-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af142-107">EXAMPLES</span></span>

### <span data-ttu-id="af142-108">Esempio 1: recupero di tutti i tenant</span><span class="sxs-lookup"><span data-stu-id="af142-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="af142-109">Questo esempio Mostra come ottenere tutti i tenant autorizzati di un account Azure.</span><span class="sxs-lookup"><span data-stu-id="af142-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="af142-110">Esempio 2: ottenere un tenant specifico</span><span class="sxs-lookup"><span data-stu-id="af142-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="af142-111">Questo esempio Mostra come ottenere uno specifico tenant autorizzato di un account Azure.</span><span class="sxs-lookup"><span data-stu-id="af142-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="af142-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af142-112">PARAMETERS</span></span>

### <span data-ttu-id="af142-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af142-113">-DefaultProfile</span></span>
<span data-ttu-id="af142-114">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="af142-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af142-115">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="af142-115">-TenantId</span></span>
<span data-ttu-id="af142-116">Specifica l'ID del tenant ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af142-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="af142-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af142-117">CommonParameters</span></span>
<span data-ttu-id="af142-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af142-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af142-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af142-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af142-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af142-120">INPUTS</span></span>

### <span data-ttu-id="af142-121">System. String</span><span class="sxs-lookup"><span data-stu-id="af142-121">System.String</span></span>

## <span data-ttu-id="af142-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af142-122">OUTPUTS</span></span>

### <span data-ttu-id="af142-123">Microsoft. Azure. Commands. profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="af142-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="af142-124">Note</span><span class="sxs-lookup"><span data-stu-id="af142-124">NOTES</span></span>

## <span data-ttu-id="af142-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af142-125">RELATED LINKS</span></span>
