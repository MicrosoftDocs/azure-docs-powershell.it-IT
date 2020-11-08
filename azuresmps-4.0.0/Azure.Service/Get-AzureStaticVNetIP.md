---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 12BF47AA-9E82-425E-A1EB-BAD64D800943
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3be6496993ed6de248103b9a222df4cbe15ed2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030019"
---
# <span data-ttu-id="ad70a-101">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="ad70a-101">Get-AzureStaticVNetIP</span></span>

## <span data-ttu-id="ad70a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad70a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad70a-103">Ottiene le informazioni sull'indirizzo IP VNet statico da un oggetto macchina virtuale, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="ad70a-103">Gets the static VNet IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="ad70a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad70a-104">SYNTAX</span></span>

```
Get-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ad70a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad70a-105">DESCRIPTION</span></span>
<span data-ttu-id="ad70a-106">Il cmdlet **Get-AzureStaticVNetIP** ottiene le informazioni sull'indirizzo IP della rete virtuale statica (VNet) da un oggetto macchina virtuale, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="ad70a-106">The **Get-AzureStaticVNetIP** cmdlet gets the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="ad70a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad70a-107">EXAMPLES</span></span>

### <span data-ttu-id="ad70a-108">1:</span><span class="sxs-lookup"><span data-stu-id="ad70a-108">1:</span></span>
```

```

## <span data-ttu-id="ad70a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad70a-109">PARAMETERS</span></span>

### <span data-ttu-id="ad70a-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ad70a-110">-InformationAction</span></span>
<span data-ttu-id="ad70a-111">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="ad70a-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ad70a-112">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ad70a-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad70a-113">Continuare</span><span class="sxs-lookup"><span data-stu-id="ad70a-113">Continue</span></span>
- <span data-ttu-id="ad70a-114">Ignora</span><span class="sxs-lookup"><span data-stu-id="ad70a-114">Ignore</span></span>
- <span data-ttu-id="ad70a-115">Informarsi</span><span class="sxs-lookup"><span data-stu-id="ad70a-115">Inquire</span></span>
- <span data-ttu-id="ad70a-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ad70a-116">SilentlyContinue</span></span>
- <span data-ttu-id="ad70a-117">Stop</span><span class="sxs-lookup"><span data-stu-id="ad70a-117">Stop</span></span>
- <span data-ttu-id="ad70a-118">Sospensione</span><span class="sxs-lookup"><span data-stu-id="ad70a-118">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad70a-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ad70a-119">-InformationVariable</span></span>
<span data-ttu-id="ad70a-120">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="ad70a-120">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad70a-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="ad70a-121">-Profile</span></span>
<span data-ttu-id="ad70a-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad70a-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad70a-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ad70a-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad70a-124">-VM</span><span class="sxs-lookup"><span data-stu-id="ad70a-124">-VM</span></span>
<span data-ttu-id="ad70a-125">Specifica un oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="ad70a-125">Specifies a persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad70a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad70a-126">CommonParameters</span></span>
<span data-ttu-id="ad70a-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad70a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad70a-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad70a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad70a-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad70a-129">INPUTS</span></span>

## <span data-ttu-id="ad70a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad70a-130">OUTPUTS</span></span>

## <span data-ttu-id="ad70a-131">Note</span><span class="sxs-lookup"><span data-stu-id="ad70a-131">NOTES</span></span>

## <span data-ttu-id="ad70a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad70a-132">RELATED LINKS</span></span>

[<span data-ttu-id="ad70a-133">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="ad70a-133">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


