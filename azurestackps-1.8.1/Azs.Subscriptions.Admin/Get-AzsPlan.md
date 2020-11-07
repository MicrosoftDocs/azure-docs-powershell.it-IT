---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02baf67cc13269d9d53c0adb40337adbd9929641
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859558"
---
# <span data-ttu-id="5a82b-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="5a82b-101">Get-AzsPlan</span></span>

## <span data-ttu-id="5a82b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a82b-102">SYNOPSIS</span></span>
<span data-ttu-id="5a82b-103">Elenca tutti i piani in tutti gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="5a82b-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="5a82b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a82b-104">SYNTAX</span></span>

### <span data-ttu-id="5a82b-105">ListAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a82b-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5a82b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5a82b-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="5a82b-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="5a82b-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5a82b-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a82b-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5a82b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a82b-109">DESCRIPTION</span></span>
<span data-ttu-id="5a82b-110">Elenca tutti i piani in tutti gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="5a82b-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="5a82b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a82b-111">EXAMPLES</span></span>

### <span data-ttu-id="5a82b-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5a82b-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="5a82b-113">Ottenere un piano limitare in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5a82b-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="5a82b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a82b-114">PARAMETERS</span></span>

### <span data-ttu-id="5a82b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a82b-115">-Name</span></span>
<span data-ttu-id="5a82b-116">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="5a82b-116">Name of the plan.</span></span>

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

### <span data-ttu-id="5a82b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a82b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a82b-118">Nome del gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5a82b-118">The name of the resource group the resource is located under.</span></span>

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

### <span data-ttu-id="5a82b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a82b-119">-ResourceId</span></span>
<span data-ttu-id="5a82b-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5a82b-120">The resource id.</span></span>

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

### <span data-ttu-id="5a82b-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="5a82b-121">-Skip</span></span>
<span data-ttu-id="5a82b-122">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="5a82b-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5a82b-123">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="5a82b-123">-Top</span></span>
<span data-ttu-id="5a82b-124">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="5a82b-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5a82b-125">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="5a82b-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5a82b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a82b-126">CommonParameters</span></span>
<span data-ttu-id="5a82b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a82b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a82b-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a82b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a82b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a82b-129">INPUTS</span></span>

## <span data-ttu-id="5a82b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a82b-130">OUTPUTS</span></span>

### <span data-ttu-id="5a82b-131">Microsoft. AzureStack. Management. subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="5a82b-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="5a82b-132">Note</span><span class="sxs-lookup"><span data-stu-id="5a82b-132">NOTES</span></span>

## <span data-ttu-id="5a82b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a82b-133">RELATED LINKS</span></span>

