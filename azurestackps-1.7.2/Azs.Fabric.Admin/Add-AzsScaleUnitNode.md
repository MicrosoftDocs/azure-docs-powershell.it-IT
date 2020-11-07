---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09391f521a2b75663b25731c6cc20ef78a658d5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858794"
---
# <span data-ttu-id="8b92e-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="8b92e-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="8b92e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b92e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b92e-103">Scalare un'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="8b92e-103">Scale out a scale unit.</span></span>

## <span data-ttu-id="8b92e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b92e-104">SYNTAX</span></span>

```
Add-AzsScaleUnitNode [-NodeList] <ScaleOutScaleUnitParameters[]> [[-ResourceGroupName] <String>]
 [-ScaleUnit] <String> [[-Location] <String>] [-AwaitStorageConvergence] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="8b92e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b92e-105">DESCRIPTION</span></span>
<span data-ttu-id="8b92e-106">Aggiungere un nuovo nodo unità di scala al cluster di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="8b92e-106">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="8b92e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b92e-107">EXAMPLES</span></span>

### <span data-ttu-id="8b92e-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8b92e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName
```

<span data-ttu-id="8b92e-109">Aggiunge un elenco di nodi all'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="8b92e-109">Adds a list of nodes to the scale unit.</span></span>

## <span data-ttu-id="8b92e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b92e-110">PARAMETERS</span></span>

### <span data-ttu-id="8b92e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b92e-111">-AsJob</span></span>
<span data-ttu-id="8b92e-112">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="8b92e-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b92e-113">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="8b92e-113">-AwaitStorageConvergence</span></span>
<span data-ttu-id="8b92e-114">Attendere il completamento della replica di archiviazione prima di restituire il successo.</span><span class="sxs-lookup"><span data-stu-id="8b92e-114">Wait for storage replication to complete before returning success.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b92e-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8b92e-115">-Location</span></span>
<span data-ttu-id="8b92e-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8b92e-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b92e-117">-NodeList</span><span class="sxs-lookup"><span data-stu-id="8b92e-117">-NodeList</span></span>
<span data-ttu-id="8b92e-118">Elenco di dati di input che consente di aggiungere un set di nodi di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="8b92e-118">A list of input data that allows for adding a set of scale unit nodes.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b92e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b92e-119">-ResourceGroupName</span></span>
<span data-ttu-id="8b92e-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b92e-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b92e-121">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="8b92e-121">-ScaleUnit</span></span>
<span data-ttu-id="8b92e-122">Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="8b92e-122">Name of the scale units.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b92e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b92e-123">CommonParameters</span></span>
<span data-ttu-id="8b92e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b92e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b92e-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b92e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b92e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b92e-126">INPUTS</span></span>

## <span data-ttu-id="8b92e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b92e-127">OUTPUTS</span></span>

## <span data-ttu-id="8b92e-128">Note</span><span class="sxs-lookup"><span data-stu-id="8b92e-128">NOTES</span></span>

## <span data-ttu-id="8b92e-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b92e-129">RELATED LINKS</span></span>

