---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861705"
---
# <span data-ttu-id="afdfb-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="afdfb-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="afdfb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="afdfb-102">SYNOPSIS</span></span>
<span data-ttu-id="afdfb-103">Ottenere un elenco di tutti i bilanciatori di carico.</span><span class="sxs-lookup"><span data-stu-id="afdfb-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="afdfb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afdfb-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="afdfb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afdfb-105">DESCRIPTION</span></span>
<span data-ttu-id="afdfb-106">Ottenere un elenco di tutti i bilanciatori di carico.</span><span class="sxs-lookup"><span data-stu-id="afdfb-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="afdfb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afdfb-107">EXAMPLES</span></span>

### <span data-ttu-id="afdfb-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="afdfb-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="afdfb-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="afdfb-109">PARAMETERS</span></span>

### <span data-ttu-id="afdfb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afdfb-110">-DefaultProfile</span></span>
<span data-ttu-id="afdfb-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afdfb-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afdfb-112">-Filtro</span><span class="sxs-lookup"><span data-stu-id="afdfb-112">-Filter</span></span>
<span data-ttu-id="afdfb-113">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="afdfb-113">OData filter parameter.</span></span>

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

### <span data-ttu-id="afdfb-114">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="afdfb-114">-InlineCount</span></span>
<span data-ttu-id="afdfb-115">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="afdfb-115">OData inline count parameter.</span></span>

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

### <span data-ttu-id="afdfb-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="afdfb-116">-OrderBy</span></span>
<span data-ttu-id="afdfb-117">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="afdfb-117">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="afdfb-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="afdfb-118">-Skip</span></span>
<span data-ttu-id="afdfb-119">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="afdfb-119">OData skip parameter.</span></span>

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

### <span data-ttu-id="afdfb-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afdfb-120">-SubscriptionId</span></span>
<span data-ttu-id="afdfb-121">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="afdfb-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="afdfb-122">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="afdfb-122">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="afdfb-123">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="afdfb-123">-Top</span></span>
<span data-ttu-id="afdfb-124">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="afdfb-124">OData top parameter.</span></span>

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

### <span data-ttu-id="afdfb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afdfb-125">CommonParameters</span></span>
<span data-ttu-id="afdfb-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afdfb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afdfb-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afdfb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afdfb-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="afdfb-128">INPUTS</span></span>

## <span data-ttu-id="afdfb-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afdfb-129">OUTPUTS</span></span>

### <span data-ttu-id="afdfb-130">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. ILoadBalancer</span><span class="sxs-lookup"><span data-stu-id="afdfb-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="afdfb-131">Note</span><span class="sxs-lookup"><span data-stu-id="afdfb-131">NOTES</span></span>

## <span data-ttu-id="afdfb-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afdfb-132">RELATED LINKS</span></span>

