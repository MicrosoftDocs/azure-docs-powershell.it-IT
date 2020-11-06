---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491165"
---
# <span data-ttu-id="03302-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="03302-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="03302-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03302-102">SYNOPSIS</span></span>
<span data-ttu-id="03302-103">Ottiene i tenant autorizzati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="03302-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="03302-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03302-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="03302-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03302-105">DESCRIPTION</span></span>
<span data-ttu-id="03302-106">Il cmdlet Get-AzureRmTenant ottiene i tenant autorizzati per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="03302-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="03302-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03302-107">EXAMPLES</span></span>

### <span data-ttu-id="03302-108">Esempio 1: recupero di tutti i tenant</span><span class="sxs-lookup"><span data-stu-id="03302-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="03302-109">Questo esempio Mostra come ottenere tutti i tenant autorizzati di un account Azure.</span><span class="sxs-lookup"><span data-stu-id="03302-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="03302-110">Esempio 2: ottenere un tenant specifico</span><span class="sxs-lookup"><span data-stu-id="03302-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="03302-111">Questo esempio Mostra come ottenere uno specifico tenant autorizzato di un account Azure.</span><span class="sxs-lookup"><span data-stu-id="03302-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="03302-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03302-112">PARAMETERS</span></span>

### <span data-ttu-id="03302-113">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="03302-113">-TenantId</span></span>
<span data-ttu-id="03302-114">Specifica l'ID del tenant ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03302-114">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03302-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03302-115">CommonParameters</span></span>
<span data-ttu-id="03302-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03302-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03302-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03302-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03302-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03302-118">INPUTS</span></span>

## <span data-ttu-id="03302-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03302-119">OUTPUTS</span></span>

### <span data-ttu-id="03302-120">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="03302-120">PSAzureTenant</span></span>
<span data-ttu-id="03302-121">Questo cmdlet restituisce l'ID tenant e le informazioni sul dominio associato per i tenant autorizzati per l'account corrente.</span><span class="sxs-lookup"><span data-stu-id="03302-121">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="03302-122">Note</span><span class="sxs-lookup"><span data-stu-id="03302-122">NOTES</span></span>

## <span data-ttu-id="03302-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03302-123">RELATED LINKS</span></span>

