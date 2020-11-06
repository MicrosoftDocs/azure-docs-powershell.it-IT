---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: CA67985F-C5D5-4CF4-81A4-C35FD769AF0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
ms.openlocfilehash: 9f02a1c9dfe0c4c41fa1e873201dbeb1d849dd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520085"
---
# <span data-ttu-id="24ab5-101">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="24ab5-101">Get-AzureRmUsage</span></span>

## <span data-ttu-id="24ab5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="24ab5-103">Ottiene le metriche di utilizzo per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="24ab5-103">Gets the usage metrics for a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24ab5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24ab5-104">SYNTAX</span></span>

```
Get-AzureRmUsage [-ResourceId] <String> [-ApiVersion <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-MetricNames <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24ab5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24ab5-105">DESCRIPTION</span></span>
<span data-ttu-id="24ab5-106">Il cmdlet **Get-AzureRmUsage** ottiene le metriche di utilizzo per una risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="24ab5-106">The **Get-AzureRmUsage** cmdlet gets the usage metrics for a specified resource.</span></span>

## <span data-ttu-id="24ab5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24ab5-107">EXAMPLES</span></span>

### <span data-ttu-id="24ab5-108">Esempio 1: ottenere le metriche di utilizzo per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="24ab5-108">Example 1: Get usage metrics by resource ID</span></span>
```
PS C:\>Get-AzureRmUsage -ResourceId "/subscriptions/bcdeb07f-1c43-20be-1f3b-4f0febc10f5b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/pattifuller"
```

<span data-ttu-id="24ab5-109">Questo comando consente di ottenere le metriche di utilizzo per il sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="24ab5-109">This command gets the usage metrics for the specified website.</span></span>

## <span data-ttu-id="24ab5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24ab5-110">PARAMETERS</span></span>

### <span data-ttu-id="24ab5-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="24ab5-111">-ApiVersion</span></span>
<span data-ttu-id="24ab5-112">Specifica una stringa di versione dell'API, ad esempio 2014-04-01, che viene accettata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="24ab5-112">Specifies an API version string, for example, 2014-04-01, which is accepted by the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ab5-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="24ab5-113">-EndTime</span></span>
<span data-ttu-id="24ab5-114">Specifica la data e l'ora più recenti da cercare.</span><span class="sxs-lookup"><span data-stu-id="24ab5-114">Specifies the latest time and date to search.</span></span>

<span data-ttu-id="24ab5-115">Puoi usare il cmdlet Get-Date per ottenere un oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="24ab5-115">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ab5-116">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="24ab5-116">-MetricNames</span></span>
<span data-ttu-id="24ab5-117">Specifica una matrice di nomi di metriche.</span><span class="sxs-lookup"><span data-stu-id="24ab5-117">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ab5-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24ab5-118">-ResourceId</span></span>
<span data-ttu-id="24ab5-119">Specifica l'ID della risorsa per la metrica.</span><span class="sxs-lookup"><span data-stu-id="24ab5-119">Specifies the ID of the resource for the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ab5-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="24ab5-120">-StartTime</span></span>
<span data-ttu-id="24ab5-121">Specifica la data e l'ora meno recenti in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="24ab5-121">Specifies the earliest time and date to search.</span></span>

<span data-ttu-id="24ab5-122">Puoi usare il cmdlet Get-Date per ottenere un oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="24ab5-122">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ab5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ab5-123">-DefaultProfile</span></span>
<span data-ttu-id="24ab5-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24ab5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24ab5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ab5-125">CommonParameters</span></span>
<span data-ttu-id="24ab5-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24ab5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ab5-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ab5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ab5-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24ab5-128">INPUTS</span></span>

## <span data-ttu-id="24ab5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24ab5-129">OUTPUTS</span></span>

### <span data-ttu-id="24ab5-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSUsageMetric []</span><span class="sxs-lookup"><span data-stu-id="24ab5-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSUsageMetric[]</span></span>

## <span data-ttu-id="24ab5-131">Note</span><span class="sxs-lookup"><span data-stu-id="24ab5-131">NOTES</span></span>

## <span data-ttu-id="24ab5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24ab5-132">RELATED LINKS</span></span>

[<span data-ttu-id="24ab5-133">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="24ab5-133">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


