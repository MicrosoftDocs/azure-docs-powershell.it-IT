---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 94D20309-5F72-4BE5-A150-2D6DD754286A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a9d793bb9bc8d96150b812474bed9f8997adbe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029566"
---
# <span data-ttu-id="c3cda-101">Remove-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="c3cda-101">Remove-AzureStaticVNetIP</span></span>

## <span data-ttu-id="c3cda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3cda-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cda-103">Rimuove le informazioni sull'indirizzo IP della rete virtuale statica da un oggetto macchina virtuale, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="c3cda-103">Removes the static virtual network IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="c3cda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3cda-104">SYNTAX</span></span>

```
Remove-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c3cda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3cda-105">DESCRIPTION</span></span>
<span data-ttu-id="c3cda-106">Il cmdlet **Remove-AzureStaticVNetIP** rimuove le informazioni sull'indirizzo IP di Virtual Network (VNet) da un oggetto macchina virtuale, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="c3cda-106">The **Remove-AzureStaticVNetIP** cmdlet removes the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="c3cda-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3cda-107">EXAMPLES</span></span>

### <span data-ttu-id="c3cda-108">1:</span><span class="sxs-lookup"><span data-stu-id="c3cda-108">1:</span></span>
```

```

## <span data-ttu-id="c3cda-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3cda-109">PARAMETERS</span></span>

### <span data-ttu-id="c3cda-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c3cda-110">-InformationAction</span></span>
<span data-ttu-id="c3cda-111">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c3cda-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c3cda-112">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3cda-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3cda-113">Continuare</span><span class="sxs-lookup"><span data-stu-id="c3cda-113">Continue</span></span>
- <span data-ttu-id="c3cda-114">Ignora</span><span class="sxs-lookup"><span data-stu-id="c3cda-114">Ignore</span></span>
- <span data-ttu-id="c3cda-115">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c3cda-115">Inquire</span></span>
- <span data-ttu-id="c3cda-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c3cda-116">SilentlyContinue</span></span>
- <span data-ttu-id="c3cda-117">Stop</span><span class="sxs-lookup"><span data-stu-id="c3cda-117">Stop</span></span>
- <span data-ttu-id="c3cda-118">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c3cda-118">Suspend</span></span>

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

### <span data-ttu-id="c3cda-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c3cda-119">-InformationVariable</span></span>
<span data-ttu-id="c3cda-120">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c3cda-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c3cda-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="c3cda-121">-Profile</span></span>
<span data-ttu-id="c3cda-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3cda-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3cda-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c3cda-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c3cda-124">-VM</span><span class="sxs-lookup"><span data-stu-id="c3cda-124">-VM</span></span>
<span data-ttu-id="c3cda-125">Specifica un oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="c3cda-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="c3cda-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cda-126">CommonParameters</span></span>
<span data-ttu-id="c3cda-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3cda-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cda-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3cda-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cda-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3cda-129">INPUTS</span></span>

## <span data-ttu-id="c3cda-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3cda-130">OUTPUTS</span></span>

## <span data-ttu-id="c3cda-131">Note</span><span class="sxs-lookup"><span data-stu-id="c3cda-131">NOTES</span></span>

## <span data-ttu-id="c3cda-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3cda-132">RELATED LINKS</span></span>

[<span data-ttu-id="c3cda-133">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="c3cda-133">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="c3cda-134">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="c3cda-134">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


