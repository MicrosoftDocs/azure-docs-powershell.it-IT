---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 2f03d0599a7bfaf2b083b4a6c335b1de98b3fa73
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023221"
---
# <span data-ttu-id="6302a-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6302a-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="6302a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6302a-102">SYNOPSIS</span></span>
<span data-ttu-id="6302a-103">Ottenere un elenco di tutte le reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="6302a-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="6302a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6302a-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6302a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6302a-105">DESCRIPTION</span></span>
<span data-ttu-id="6302a-106">Ottenere un elenco di tutte le reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="6302a-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="6302a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6302a-107">EXAMPLES</span></span>

### <span data-ttu-id="6302a-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6302a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsVirtualNetwork
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
```

<span data-ttu-id="6302a-109">Restituisce un elenco di reti virtuali per l'indicatore dello stack di Azure.</span><span class="sxs-lookup"><span data-stu-id="6302a-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="6302a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6302a-110">PARAMETERS</span></span>

### <span data-ttu-id="6302a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6302a-111">-DefaultProfile</span></span>
<span data-ttu-id="6302a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6302a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6302a-113">-Filtro</span><span class="sxs-lookup"><span data-stu-id="6302a-113">-Filter</span></span>
<span data-ttu-id="6302a-114">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="6302a-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="6302a-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="6302a-115">-InlineCount</span></span>
<span data-ttu-id="6302a-116">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="6302a-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="6302a-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="6302a-117">-OrderBy</span></span>
<span data-ttu-id="6302a-118">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="6302a-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="6302a-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="6302a-119">-Skip</span></span>
<span data-ttu-id="6302a-120">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="6302a-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="6302a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6302a-121">-SubscriptionId</span></span>
<span data-ttu-id="6302a-122">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6302a-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6302a-123">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="6302a-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6302a-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="6302a-124">-Top</span></span>
<span data-ttu-id="6302a-125">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="6302a-125">OData top parameter.</span></span>

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

### <span data-ttu-id="6302a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6302a-126">CommonParameters</span></span>
<span data-ttu-id="6302a-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6302a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6302a-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6302a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6302a-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6302a-129">INPUTS</span></span>

## <span data-ttu-id="6302a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6302a-130">OUTPUTS</span></span>

### <span data-ttu-id="6302a-131">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6302a-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IVirtualNetwork</span></span>



## <span data-ttu-id="6302a-132">Note</span><span class="sxs-lookup"><span data-stu-id="6302a-132">NOTES</span></span>

## <span data-ttu-id="6302a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6302a-133">RELATED LINKS</span></span>

