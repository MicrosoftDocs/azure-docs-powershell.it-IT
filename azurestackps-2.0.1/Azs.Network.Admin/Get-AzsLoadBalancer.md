---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023173"
---
# <span data-ttu-id="3a0b9-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3a0b9-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="3a0b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3a0b9-103">Ottenere un elenco di tutti i bilanciatori di carico.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="3a0b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a0b9-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3a0b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a0b9-105">DESCRIPTION</span></span>
<span data-ttu-id="3a0b9-106">Ottenere un elenco di tutti i bilanciatori di carico.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="3a0b9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a0b9-107">EXAMPLES</span></span>

### <span data-ttu-id="3a0b9-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3a0b9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="3a0b9-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a0b9-109">PARAMETERS</span></span>

### <span data-ttu-id="3a0b9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a0b9-110">-DefaultProfile</span></span>
<span data-ttu-id="3a0b9-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a0b9-112">-Filtro</span><span class="sxs-lookup"><span data-stu-id="3a0b9-112">-Filter</span></span>
<span data-ttu-id="3a0b9-113">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-113">OData filter parameter.</span></span>

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

### <span data-ttu-id="3a0b9-114">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="3a0b9-114">-InlineCount</span></span>
<span data-ttu-id="3a0b9-115">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-115">OData inline count parameter.</span></span>

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

### <span data-ttu-id="3a0b9-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="3a0b9-116">-OrderBy</span></span>
<span data-ttu-id="3a0b9-117">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-117">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="3a0b9-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="3a0b9-118">-Skip</span></span>
<span data-ttu-id="3a0b9-119">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-119">OData skip parameter.</span></span>

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

### <span data-ttu-id="3a0b9-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a0b9-120">-SubscriptionId</span></span>
<span data-ttu-id="3a0b9-121">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3a0b9-122">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-122">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3a0b9-123">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="3a0b9-123">-Top</span></span>
<span data-ttu-id="3a0b9-124">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-124">OData top parameter.</span></span>

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

### <span data-ttu-id="3a0b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a0b9-125">CommonParameters</span></span>
<span data-ttu-id="3a0b9-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a0b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a0b9-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a0b9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a0b9-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a0b9-128">INPUTS</span></span>

## <span data-ttu-id="3a0b9-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a0b9-129">OUTPUTS</span></span>

### <span data-ttu-id="3a0b9-130">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. ILoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3a0b9-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="3a0b9-131">Note</span><span class="sxs-lookup"><span data-stu-id="3a0b9-131">NOTES</span></span>

## <span data-ttu-id="3a0b9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a0b9-132">RELATED LINKS</span></span>

