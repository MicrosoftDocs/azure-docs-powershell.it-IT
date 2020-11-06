---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b43acb45bc5b606303cbd33c20f0975919bb6b59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491006"
---
# <span data-ttu-id="d3efc-101">Get-AzsBlobServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="d3efc-101">Get-AzsBlobServiceMetricDefinition</span></span>

## <span data-ttu-id="d3efc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3efc-102">SYNOPSIS</span></span>
<span data-ttu-id="d3efc-103">Restituisce l'elenco di definizioni metriche per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="d3efc-103">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="d3efc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3efc-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d3efc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3efc-105">DESCRIPTION</span></span>
<span data-ttu-id="d3efc-106">Restituisce l'elenco di definizioni metriche per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="d3efc-106">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="d3efc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3efc-107">EXAMPLES</span></span>

### <span data-ttu-id="d3efc-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d3efc-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="d3efc-109">Ottenere un elenco di definizioni metriche per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="d3efc-109">Get a list of metric definitions for the blob service.</span></span>

## <span data-ttu-id="d3efc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3efc-110">PARAMETERS</span></span>

### <span data-ttu-id="d3efc-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="d3efc-111">-FarmName</span></span>
<span data-ttu-id="d3efc-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="d3efc-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3efc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3efc-113">-ResourceGroupName</span></span>
<span data-ttu-id="d3efc-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3efc-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3efc-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="d3efc-115">-Skip</span></span>
<span data-ttu-id="d3efc-116">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d3efc-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3efc-117">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="d3efc-117">-Top</span></span>
<span data-ttu-id="d3efc-118">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d3efc-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d3efc-119">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="d3efc-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3efc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3efc-120">CommonParameters</span></span>
<span data-ttu-id="d3efc-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3efc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3efc-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3efc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3efc-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3efc-123">INPUTS</span></span>

## <span data-ttu-id="d3efc-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3efc-124">OUTPUTS</span></span>

### <span data-ttu-id="d3efc-125">Microsoft. AzureStack. Management. storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="d3efc-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="d3efc-126">Note</span><span class="sxs-lookup"><span data-stu-id="d3efc-126">NOTES</span></span>

## <span data-ttu-id="d3efc-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3efc-127">RELATED LINKS</span></span>

