---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023162"
---
# <span data-ttu-id="b56c9-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="b56c9-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="b56c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b56c9-102">SYNOPSIS</span></span>
<span data-ttu-id="b56c9-103">Elenco di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="b56c9-103">List of public ip addresses.</span></span>

## <span data-ttu-id="b56c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b56c9-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b56c9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b56c9-105">DESCRIPTION</span></span>
<span data-ttu-id="b56c9-106">Elenco di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="b56c9-106">List of public ip addresses.</span></span>

## <span data-ttu-id="b56c9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b56c9-107">EXAMPLES</span></span>

### <span data-ttu-id="b56c9-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b56c9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="b56c9-109">Ottenere l'elenco degli indirizzi IP pubblici, assegnati o non assegnati.</span><span class="sxs-lookup"><span data-stu-id="b56c9-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="b56c9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b56c9-110">PARAMETERS</span></span>

### <span data-ttu-id="b56c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56c9-111">-DefaultProfile</span></span>
<span data-ttu-id="b56c9-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b56c9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b56c9-113">-Filtro</span><span class="sxs-lookup"><span data-stu-id="b56c9-113">-Filter</span></span>
<span data-ttu-id="b56c9-114">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="b56c9-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="b56c9-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="b56c9-115">-InlineCount</span></span>
<span data-ttu-id="b56c9-116">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="b56c9-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="b56c9-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b56c9-117">-OrderBy</span></span>
<span data-ttu-id="b56c9-118">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="b56c9-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="b56c9-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="b56c9-119">-Skip</span></span>
<span data-ttu-id="b56c9-120">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="b56c9-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="b56c9-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b56c9-121">-SubscriptionId</span></span>
<span data-ttu-id="b56c9-122">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b56c9-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b56c9-123">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b56c9-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b56c9-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="b56c9-124">-Top</span></span>
<span data-ttu-id="b56c9-125">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="b56c9-125">OData top parameter.</span></span>

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

### <span data-ttu-id="b56c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56c9-126">CommonParameters</span></span>
<span data-ttu-id="b56c9-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b56c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56c9-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b56c9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56c9-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b56c9-129">INPUTS</span></span>

## <span data-ttu-id="b56c9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b56c9-130">OUTPUTS</span></span>

### <span data-ttu-id="b56c9-131">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="b56c9-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="b56c9-132">Note</span><span class="sxs-lookup"><span data-stu-id="b56c9-132">NOTES</span></span>

## <span data-ttu-id="b56c9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b56c9-133">RELATED LINKS</span></span>

