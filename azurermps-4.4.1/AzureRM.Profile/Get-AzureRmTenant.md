---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 8ac36dd86abb996a934b59d064980233c931d214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516112"
---
# <span data-ttu-id="ad416-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="ad416-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="ad416-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad416-102">SYNOPSIS</span></span>
<span data-ttu-id="ad416-103">Ottiene i tenant autorizzati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="ad416-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad416-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad416-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad416-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad416-105">DESCRIPTION</span></span>
<span data-ttu-id="ad416-106">Il cmdlet Get-AzureRmTenant ottiene i tenant autorizzati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="ad416-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="ad416-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad416-107">EXAMPLES</span></span>

### <span data-ttu-id="ad416-108">Esempio 1: recupero di tutti i tenant</span><span class="sxs-lookup"><span data-stu-id="ad416-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="ad416-109">Questo esempio Mostra come ottenere tutti i tenant autorizzati di un account Azure.</span><span class="sxs-lookup"><span data-stu-id="ad416-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="ad416-110">Esempio 2: ottenere un tenant specifico</span><span class="sxs-lookup"><span data-stu-id="ad416-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="ad416-111">Questo esempio Mostra come ottenere uno specifico tenant autorizzato di un account Azure.</span><span class="sxs-lookup"><span data-stu-id="ad416-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="ad416-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad416-112">PARAMETERS</span></span>

### <span data-ttu-id="ad416-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad416-113">-DefaultProfile</span></span>
<span data-ttu-id="ad416-114">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ad416-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad416-115">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="ad416-115">-TenantId</span></span>
<span data-ttu-id="ad416-116">Specifica l'ID del tenant ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad416-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ad416-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad416-117">CommonParameters</span></span>
<span data-ttu-id="ad416-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad416-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad416-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad416-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad416-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad416-120">INPUTS</span></span>

## <span data-ttu-id="ad416-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad416-121">OUTPUTS</span></span>

### <span data-ttu-id="ad416-122">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="ad416-122">PSAzureTenant</span></span>
<span data-ttu-id="ad416-123">Questo cmdlet restituisce l'ID tenant e le informazioni sul dominio associato per i tenant autorizzati per l'account corrente.</span><span class="sxs-lookup"><span data-stu-id="ad416-123">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="ad416-124">Note</span><span class="sxs-lookup"><span data-stu-id="ad416-124">NOTES</span></span>

## <span data-ttu-id="ad416-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad416-125">RELATED LINKS</span></span>

