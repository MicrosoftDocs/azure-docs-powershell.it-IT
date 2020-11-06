---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75fef110a1266ca34bef645f39a879dda4aeeda4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491522"
---
# <span data-ttu-id="75bea-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="75bea-101">Get-AzsPlan</span></span>

## <span data-ttu-id="75bea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75bea-102">SYNOPSIS</span></span>
<span data-ttu-id="75bea-103">Elenca tutti i piani in tutti gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="75bea-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="75bea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75bea-104">SYNTAX</span></span>

### <span data-ttu-id="75bea-105">ListAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75bea-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="75bea-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="75bea-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="75bea-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="75bea-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="75bea-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="75bea-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="75bea-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75bea-109">DESCRIPTION</span></span>
<span data-ttu-id="75bea-110">Elenca tutti i piani in tutti gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="75bea-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="75bea-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75bea-111">EXAMPLES</span></span>

### <span data-ttu-id="75bea-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="75bea-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="75bea-113">Ottenere un piano limitare in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="75bea-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="75bea-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75bea-114">PARAMETERS</span></span>

### <span data-ttu-id="75bea-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="75bea-115">-Name</span></span>
<span data-ttu-id="75bea-116">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="75bea-116">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75bea-117">-ResourceGroupName</span></span>
<span data-ttu-id="75bea-118">Nome del gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="75bea-118">The name of the resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bea-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75bea-119">-ResourceId</span></span>
<span data-ttu-id="75bea-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="75bea-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bea-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="75bea-121">-Skip</span></span>
<span data-ttu-id="75bea-122">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="75bea-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bea-123">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="75bea-123">-Top</span></span>
<span data-ttu-id="75bea-124">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="75bea-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="75bea-125">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="75bea-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75bea-126">CommonParameters</span></span>
<span data-ttu-id="75bea-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75bea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75bea-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75bea-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75bea-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75bea-129">INPUTS</span></span>

## <span data-ttu-id="75bea-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75bea-130">OUTPUTS</span></span>

### <span data-ttu-id="75bea-131">Microsoft. AzureStack. Management. subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="75bea-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="75bea-132">Note</span><span class="sxs-lookup"><span data-stu-id="75bea-132">NOTES</span></span>

## <span data-ttu-id="75bea-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75bea-133">RELATED LINKS</span></span>

