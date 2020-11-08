---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C0EEC51F-F8AB-4A6C-8F99-2B2DFFE9BB26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b5f4d5319e705c4f0481edcb5a44a579f4ff01d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023576"
---
# <span data-ttu-id="d592f-101">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="d592f-101">Get-AzureReservedIP</span></span>

## <span data-ttu-id="d592f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d592f-102">SYNOPSIS</span></span>
<span data-ttu-id="d592f-103">Ottiene un indirizzo IP riservato in base al nome o elenca tutti gli indirizzi IP riservati nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d592f-103">Gets a reserved IP address by its name or lists all the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="d592f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d592f-104">SYNTAX</span></span>

```
Get-AzureReservedIP [[-ReservedIPName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d592f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d592f-105">DESCRIPTION</span></span>
<span data-ttu-id="d592f-106">Il cmdlet **Get-AzureReservedIP** ottiene un indirizzo IP riservato in base al nome o elenca tutti gli indirizzi IP riservati nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d592f-106">The **Get-AzureReservedIP** cmdlet gets a reserved IP address by its name or lists all of the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="d592f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d592f-107">EXAMPLES</span></span>

### <span data-ttu-id="d592f-108">Esempio 1: ottenere tutti gli indirizzi IP riservati</span><span class="sxs-lookup"><span data-stu-id="d592f-108">Example 1: Get all reserved IP addresses</span></span>
```
PS C:\> Get-AzureReservedIP
```

<span data-ttu-id="d592f-109">Questo comando ottiene tutti gli indirizzi IP riservati.</span><span class="sxs-lookup"><span data-stu-id="d592f-109">This command gets all reserved IP addresses.</span></span>

### <span data-ttu-id="d592f-110">Esempio 2: ottenere un indirizzo IP riservato con un nome specificato</span><span class="sxs-lookup"><span data-stu-id="d592f-110">Example 2: Get a reserved IP address with a specified name</span></span>
```
PS C:\> Get-AzureReservedIP -ReservedIPName $IpName
```

<span data-ttu-id="d592f-111">Questo comando ottiene l'indirizzo IP riservato con il nome specificato dalla variabile $IpName.</span><span class="sxs-lookup"><span data-stu-id="d592f-111">This command gets the reserved IP address that has the name specified by the $IpName variable.</span></span>

## <span data-ttu-id="d592f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d592f-112">PARAMETERS</span></span>

### <span data-ttu-id="d592f-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d592f-113">-InformationAction</span></span>
<span data-ttu-id="d592f-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d592f-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d592f-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d592f-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d592f-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="d592f-116">Continue</span></span>
- <span data-ttu-id="d592f-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="d592f-117">Ignore</span></span>
- <span data-ttu-id="d592f-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d592f-118">Inquire</span></span>
- <span data-ttu-id="d592f-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d592f-119">SilentlyContinue</span></span>
- <span data-ttu-id="d592f-120">Stop</span><span class="sxs-lookup"><span data-stu-id="d592f-120">Stop</span></span>
- <span data-ttu-id="d592f-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d592f-121">Suspend</span></span>

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

### <span data-ttu-id="d592f-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d592f-122">-InformationVariable</span></span>
<span data-ttu-id="d592f-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d592f-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d592f-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="d592f-124">-Profile</span></span>
<span data-ttu-id="d592f-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d592f-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d592f-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d592f-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d592f-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="d592f-127">-ReservedIPName</span></span>
<span data-ttu-id="d592f-128">Specifica il nome IP riservato.</span><span class="sxs-lookup"><span data-stu-id="d592f-128">Specifies the reserved IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d592f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d592f-129">CommonParameters</span></span>
<span data-ttu-id="d592f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d592f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d592f-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d592f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d592f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d592f-132">INPUTS</span></span>

## <span data-ttu-id="d592f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d592f-133">OUTPUTS</span></span>

## <span data-ttu-id="d592f-134">Note</span><span class="sxs-lookup"><span data-stu-id="d592f-134">NOTES</span></span>

## <span data-ttu-id="d592f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d592f-135">RELATED LINKS</span></span>

[<span data-ttu-id="d592f-136">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="d592f-136">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="d592f-137">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="d592f-137">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


