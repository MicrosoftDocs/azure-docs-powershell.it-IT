---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ae30d06970d9533c32c96f33a1917fa8d2a6e41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490801"
---
# <span data-ttu-id="c9340-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="c9340-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="c9340-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9340-102">SYNOPSIS</span></span>
<span data-ttu-id="c9340-103">Elenca tutti i tenant della directory sotto l'abbonamento corrente e il nome del gruppo di risorse assegnato.</span><span class="sxs-lookup"><span data-stu-id="c9340-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="c9340-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9340-104">SYNTAX</span></span>

### <span data-ttu-id="c9340-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c9340-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c9340-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="c9340-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9340-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9340-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c9340-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9340-108">DESCRIPTION</span></span>
<span data-ttu-id="c9340-109">Elenca tutti i tenant della directory sotto l'abbonamento corrente e il nome del gruppo di risorse assegnato.</span><span class="sxs-lookup"><span data-stu-id="c9340-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="c9340-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9340-110">EXAMPLES</span></span>

### <span data-ttu-id="c9340-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c9340-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="c9340-112">Elenca tutti i tenant della directory sotto l'abbonamento corrente e il nome del gruppo di risorse assegnato.</span><span class="sxs-lookup"><span data-stu-id="c9340-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="c9340-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9340-113">PARAMETERS</span></span>

### <span data-ttu-id="c9340-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9340-114">-Name</span></span>
<span data-ttu-id="c9340-115">Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="c9340-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="c9340-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9340-116">-ResourceGroupName</span></span>
<span data-ttu-id="c9340-117">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c9340-117">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9340-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9340-118">-ResourceId</span></span>
<span data-ttu-id="c9340-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c9340-119">The resource id.</span></span>

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

### <span data-ttu-id="c9340-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="c9340-120">-Skip</span></span>
<span data-ttu-id="c9340-121">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="c9340-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9340-122">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="c9340-122">-Top</span></span>
<span data-ttu-id="c9340-123">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="c9340-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c9340-124">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="c9340-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9340-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9340-125">CommonParameters</span></span>
<span data-ttu-id="c9340-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9340-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9340-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9340-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9340-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9340-128">INPUTS</span></span>

## <span data-ttu-id="c9340-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9340-129">OUTPUTS</span></span>

### <span data-ttu-id="c9340-130">Microsoft. AzureStack. Management. subscriptions. admin. Models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="c9340-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="c9340-131">Note</span><span class="sxs-lookup"><span data-stu-id="c9340-131">NOTES</span></span>

## <span data-ttu-id="c9340-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9340-132">RELATED LINKS</span></span>

