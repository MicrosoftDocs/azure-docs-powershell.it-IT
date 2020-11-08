---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 2f03d0599a7bfaf2b083b4a6c335b1de98b3fa73
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030426"
---
# <span data-ttu-id="4431c-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4431c-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="4431c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4431c-102">SYNOPSIS</span></span>
<span data-ttu-id="4431c-103">Ottenere un elenco di tutte le reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="4431c-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="4431c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4431c-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4431c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4431c-105">DESCRIPTION</span></span>
<span data-ttu-id="4431c-106">Ottenere un elenco di tutte le reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="4431c-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="4431c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4431c-107">EXAMPLES</span></span>

### <span data-ttu-id="4431c-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4431c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsVirtualNetwork
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
```

<span data-ttu-id="4431c-109">Restituisce un elenco di reti virtuali per l'indicatore dello stack di Azure.</span><span class="sxs-lookup"><span data-stu-id="4431c-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="4431c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4431c-110">PARAMETERS</span></span>

### <span data-ttu-id="4431c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4431c-111">-DefaultProfile</span></span>
<span data-ttu-id="4431c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4431c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4431c-113">-Filtro</span><span class="sxs-lookup"><span data-stu-id="4431c-113">-Filter</span></span>
<span data-ttu-id="4431c-114">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="4431c-114">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4431c-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="4431c-115">-InlineCount</span></span>
<span data-ttu-id="4431c-116">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="4431c-116">OData inline count parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4431c-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="4431c-117">-OrderBy</span></span>
<span data-ttu-id="4431c-118">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="4431c-118">OData orderBy parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4431c-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="4431c-119">-Skip</span></span>
<span data-ttu-id="4431c-120">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="4431c-120">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4431c-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4431c-121">-SubscriptionId</span></span>
<span data-ttu-id="4431c-122">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4431c-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4431c-123">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="4431c-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4431c-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="4431c-124">-Top</span></span>
<span data-ttu-id="4431c-125">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="4431c-125">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4431c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4431c-126">CommonParameters</span></span>
<span data-ttu-id="4431c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4431c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4431c-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4431c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4431c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4431c-129">INPUTS</span></span>

## <span data-ttu-id="4431c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4431c-130">OUTPUTS</span></span>

### <span data-ttu-id="4431c-131">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4431c-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IVirtualNetwork</span></span>



## <span data-ttu-id="4431c-132">Note</span><span class="sxs-lookup"><span data-stu-id="4431c-132">NOTES</span></span>

## <span data-ttu-id="4431c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4431c-133">RELATED LINKS</span></span>

