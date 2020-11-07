---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859589"
---
# <span data-ttu-id="d1f94-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="d1f94-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="d1f94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1f94-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f94-103">Elenca tutti i tenant della directory sotto l'abbonamento corrente e il nome del gruppo di risorse assegnato.</span><span class="sxs-lookup"><span data-stu-id="d1f94-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="d1f94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1f94-104">SYNTAX</span></span>

### <span data-ttu-id="d1f94-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1f94-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d1f94-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d1f94-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d1f94-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f94-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d1f94-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1f94-108">DESCRIPTION</span></span>
<span data-ttu-id="d1f94-109">Elenca tutti i tenant della directory sotto l'abbonamento corrente e il nome del gruppo di risorse assegnato.</span><span class="sxs-lookup"><span data-stu-id="d1f94-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="d1f94-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1f94-110">EXAMPLES</span></span>

### <span data-ttu-id="d1f94-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d1f94-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="d1f94-112">Elenca tutti i tenant della directory sotto l'abbonamento corrente e il nome del gruppo di risorse assegnato.</span><span class="sxs-lookup"><span data-stu-id="d1f94-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="d1f94-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1f94-113">PARAMETERS</span></span>

### <span data-ttu-id="d1f94-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1f94-114">-Name</span></span>
<span data-ttu-id="d1f94-115">Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="d1f94-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="d1f94-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1f94-116">-ResourceGroupName</span></span>
<span data-ttu-id="d1f94-117">{{Fill ResourceGroupName Description}}</span><span class="sxs-lookup"><span data-stu-id="d1f94-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="d1f94-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f94-118">-ResourceId</span></span>
<span data-ttu-id="d1f94-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d1f94-119">The resource id.</span></span>

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

### <span data-ttu-id="d1f94-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="d1f94-120">-Skip</span></span>
<span data-ttu-id="d1f94-121">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d1f94-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d1f94-122">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="d1f94-122">-Top</span></span>
<span data-ttu-id="d1f94-123">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d1f94-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d1f94-124">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="d1f94-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d1f94-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f94-125">CommonParameters</span></span>
<span data-ttu-id="d1f94-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1f94-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f94-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1f94-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f94-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1f94-128">INPUTS</span></span>

## <span data-ttu-id="d1f94-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1f94-129">OUTPUTS</span></span>

### <span data-ttu-id="d1f94-130">Microsoft. AzureStack. Management. subscriptions. admin. Models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="d1f94-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="d1f94-131">Note</span><span class="sxs-lookup"><span data-stu-id="d1f94-131">NOTES</span></span>

## <span data-ttu-id="d1f94-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1f94-132">RELATED LINKS</span></span>

