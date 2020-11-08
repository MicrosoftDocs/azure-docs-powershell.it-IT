---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030429"
---
# <span data-ttu-id="ff493-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="ff493-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="ff493-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff493-102">SYNOPSIS</span></span>
<span data-ttu-id="ff493-103">Elenco di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="ff493-103">List of public ip addresses.</span></span>

## <span data-ttu-id="ff493-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff493-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ff493-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff493-105">DESCRIPTION</span></span>
<span data-ttu-id="ff493-106">Elenco di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="ff493-106">List of public ip addresses.</span></span>

## <span data-ttu-id="ff493-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff493-107">EXAMPLES</span></span>

### <span data-ttu-id="ff493-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ff493-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="ff493-109">Ottenere l'elenco degli indirizzi IP pubblici, assegnati o non assegnati.</span><span class="sxs-lookup"><span data-stu-id="ff493-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="ff493-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff493-110">PARAMETERS</span></span>

### <span data-ttu-id="ff493-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff493-111">-DefaultProfile</span></span>
<span data-ttu-id="ff493-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff493-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff493-113">-Filtro</span><span class="sxs-lookup"><span data-stu-id="ff493-113">-Filter</span></span>
<span data-ttu-id="ff493-114">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="ff493-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="ff493-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="ff493-115">-InlineCount</span></span>
<span data-ttu-id="ff493-116">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="ff493-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="ff493-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="ff493-117">-OrderBy</span></span>
<span data-ttu-id="ff493-118">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="ff493-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="ff493-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="ff493-119">-Skip</span></span>
<span data-ttu-id="ff493-120">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="ff493-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="ff493-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff493-121">-SubscriptionId</span></span>
<span data-ttu-id="ff493-122">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ff493-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ff493-123">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ff493-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ff493-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="ff493-124">-Top</span></span>
<span data-ttu-id="ff493-125">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="ff493-125">OData top parameter.</span></span>

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

### <span data-ttu-id="ff493-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff493-126">CommonParameters</span></span>
<span data-ttu-id="ff493-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff493-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff493-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff493-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff493-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff493-129">INPUTS</span></span>

## <span data-ttu-id="ff493-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff493-130">OUTPUTS</span></span>

### <span data-ttu-id="ff493-131">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="ff493-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="ff493-132">Note</span><span class="sxs-lookup"><span data-stu-id="ff493-132">NOTES</span></span>

## <span data-ttu-id="ff493-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff493-133">RELATED LINKS</span></span>

