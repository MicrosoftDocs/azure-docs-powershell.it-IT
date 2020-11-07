---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859525"
---
# <span data-ttu-id="ee7f1-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="ee7f1-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="ee7f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee7f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ee7f1-103">Tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-103">Directory tenant.</span></span>

## <span data-ttu-id="ee7f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee7f1-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ee7f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee7f1-105">DESCRIPTION</span></span>
<span data-ttu-id="ee7f1-106">Tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-106">Directory tenant.</span></span>

## <span data-ttu-id="ee7f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee7f1-107">EXAMPLES</span></span>

### <span data-ttu-id="ee7f1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee7f1-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ee7f1-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="ee7f1-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ee7f1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee7f1-110">PARAMETERS</span></span>

### <span data-ttu-id="ee7f1-111">-ID</span><span class="sxs-lookup"><span data-stu-id="ee7f1-111">-Id</span></span>
<span data-ttu-id="ee7f1-112">URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-112">URI of the resource.</span></span>

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

### <span data-ttu-id="ee7f1-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ee7f1-113">-Location</span></span>
<span data-ttu-id="ee7f1-114">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-114">Location of the resource.</span></span>

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

### <span data-ttu-id="ee7f1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee7f1-115">-Name</span></span>
<span data-ttu-id="ee7f1-116">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-116">Name of the resource.</span></span>

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

### <span data-ttu-id="ee7f1-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee7f1-117">-Tags</span></span>
<span data-ttu-id="ee7f1-118">Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-118">List of key-value pairs.</span></span>

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

### <span data-ttu-id="ee7f1-119">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="ee7f1-119">-TenantId</span></span>
<span data-ttu-id="ee7f1-120">Identificatore univoco del tenant.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-120">Tenant unique identifier.</span></span>

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

### <span data-ttu-id="ee7f1-121">-Digitare</span><span class="sxs-lookup"><span data-stu-id="ee7f1-121">-Type</span></span>
<span data-ttu-id="ee7f1-122">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-122">Type of resource.</span></span>

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

### <span data-ttu-id="ee7f1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee7f1-123">CommonParameters</span></span>
<span data-ttu-id="ee7f1-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee7f1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee7f1-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee7f1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee7f1-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee7f1-126">INPUTS</span></span>

## <span data-ttu-id="ee7f1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee7f1-127">OUTPUTS</span></span>

## <span data-ttu-id="ee7f1-128">Note</span><span class="sxs-lookup"><span data-stu-id="ee7f1-128">NOTES</span></span>

## <span data-ttu-id="ee7f1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee7f1-129">RELATED LINKS</span></span>

