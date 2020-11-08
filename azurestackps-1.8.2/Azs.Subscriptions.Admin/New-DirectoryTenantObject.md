---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030312"
---
# <span data-ttu-id="6f6eb-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="6f6eb-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="6f6eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6eb-103">Tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-103">Directory tenant.</span></span>

## <span data-ttu-id="6f6eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f6eb-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="6f6eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f6eb-105">DESCRIPTION</span></span>
<span data-ttu-id="6f6eb-106">Tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-106">Directory tenant.</span></span>

## <span data-ttu-id="6f6eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f6eb-107">EXAMPLES</span></span>

### <span data-ttu-id="6f6eb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6f6eb-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6f6eb-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="6f6eb-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="6f6eb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f6eb-110">PARAMETERS</span></span>

### <span data-ttu-id="6f6eb-111">-ID</span><span class="sxs-lookup"><span data-stu-id="6f6eb-111">-Id</span></span>
<span data-ttu-id="6f6eb-112">URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6eb-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6f6eb-113">-Location</span></span>
<span data-ttu-id="6f6eb-114">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6eb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f6eb-115">-Name</span></span>
<span data-ttu-id="6f6eb-116">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-116">Name of the resource.</span></span>

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

### <span data-ttu-id="6f6eb-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="6f6eb-117">-Tags</span></span>
<span data-ttu-id="6f6eb-118">Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-118">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6eb-119">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="6f6eb-119">-TenantId</span></span>
<span data-ttu-id="6f6eb-120">Identificatore univoco del tenant.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-120">Tenant unique identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f6eb-121">-Digitare</span><span class="sxs-lookup"><span data-stu-id="6f6eb-121">-Type</span></span>
<span data-ttu-id="6f6eb-122">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-122">Type of resource.</span></span>

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

### <span data-ttu-id="6f6eb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6eb-123">CommonParameters</span></span>
<span data-ttu-id="6f6eb-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f6eb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6eb-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f6eb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6eb-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f6eb-126">INPUTS</span></span>

## <span data-ttu-id="6f6eb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f6eb-127">OUTPUTS</span></span>

## <span data-ttu-id="6f6eb-128">Note</span><span class="sxs-lookup"><span data-stu-id="6f6eb-128">NOTES</span></span>

## <span data-ttu-id="6f6eb-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f6eb-129">RELATED LINKS</span></span>

