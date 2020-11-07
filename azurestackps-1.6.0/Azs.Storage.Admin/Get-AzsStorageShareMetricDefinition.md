---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 646ee96dec361ac6318b4cfe48b80ec4c3686321
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685198"
---
# <span data-ttu-id="cb834-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="cb834-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="cb834-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb834-102">SYNOPSIS</span></span>
<span data-ttu-id="cb834-103">Restituisce un elenco di definizioni metriche per una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cb834-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="cb834-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb834-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-Name] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="cb834-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb834-105">DESCRIPTION</span></span>
<span data-ttu-id="cb834-106">Restituisce un elenco di definizioni metriche per una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cb834-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="cb834-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb834-107">EXAMPLES</span></span>

### <span data-ttu-id="cb834-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cb834-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Name "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="cb834-109">Ottenere l'elenco delle definizioni metriche per una condivisione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cb834-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="cb834-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb834-110">PARAMETERS</span></span>

### <span data-ttu-id="cb834-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="cb834-111">-FarmName</span></span>
<span data-ttu-id="cb834-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="cb834-112">Farm Id.</span></span>

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

### <span data-ttu-id="cb834-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb834-113">-Name</span></span>
<span data-ttu-id="cb834-114">Condividi nome.</span><span class="sxs-lookup"><span data-stu-id="cb834-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb834-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb834-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb834-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb834-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb834-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="cb834-117">-Skip</span></span>
<span data-ttu-id="cb834-118">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="cb834-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb834-119">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="cb834-119">-Top</span></span>
<span data-ttu-id="cb834-120">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="cb834-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cb834-121">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="cb834-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb834-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb834-122">CommonParameters</span></span>
<span data-ttu-id="cb834-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb834-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb834-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb834-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb834-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb834-125">INPUTS</span></span>

## <span data-ttu-id="cb834-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb834-126">OUTPUTS</span></span>

### <span data-ttu-id="cb834-127">Microsoft. AzureStack. Management. storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="cb834-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="cb834-128">Note</span><span class="sxs-lookup"><span data-stu-id="cb834-128">NOTES</span></span>

## <span data-ttu-id="cb834-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb834-129">RELATED LINKS</span></span>

