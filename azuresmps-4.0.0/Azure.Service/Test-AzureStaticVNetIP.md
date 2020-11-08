---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E059EF1-740C-4AEB-AF41-BF6003BE15F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: a52f2585771ec10d6acf52b14c88bd1ed0af0427
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023894"
---
# <span data-ttu-id="41a92-101">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="41a92-101">Test-AzureStaticVNetIP</span></span>

## <span data-ttu-id="41a92-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41a92-102">SYNOPSIS</span></span>
<span data-ttu-id="41a92-103">Verifica la disponibilità di un indirizzo IP di rete virtuale statica e riceve un elenco di suggerimenti se l'indirizzo interrogato non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="41a92-103">Tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="41a92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41a92-104">SYNTAX</span></span>

```
Test-AzureStaticVNetIP [-VNetName] <String> [-IPAddress] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="41a92-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41a92-105">DESCRIPTION</span></span>
<span data-ttu-id="41a92-106">Il cmdlet **test-AzureStaticVNetIP** verifica la disponibilità di un indirizzo IP di rete virtuale statica e ottiene un elenco di suggerimenti se l'indirizzo richiesto non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="41a92-106">The **Test-AzureStaticVNetIP** cmdlet tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="41a92-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41a92-107">EXAMPLES</span></span>

### <span data-ttu-id="41a92-108">1:</span><span class="sxs-lookup"><span data-stu-id="41a92-108">1:</span></span>
```

```

## <span data-ttu-id="41a92-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41a92-109">PARAMETERS</span></span>

### <span data-ttu-id="41a92-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="41a92-110">-InformationAction</span></span>
<span data-ttu-id="41a92-111">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="41a92-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="41a92-112">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="41a92-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41a92-113">Continuare</span><span class="sxs-lookup"><span data-stu-id="41a92-113">Continue</span></span>
- <span data-ttu-id="41a92-114">Ignora</span><span class="sxs-lookup"><span data-stu-id="41a92-114">Ignore</span></span>
- <span data-ttu-id="41a92-115">Informarsi</span><span class="sxs-lookup"><span data-stu-id="41a92-115">Inquire</span></span>
- <span data-ttu-id="41a92-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="41a92-116">SilentlyContinue</span></span>
- <span data-ttu-id="41a92-117">Stop</span><span class="sxs-lookup"><span data-stu-id="41a92-117">Stop</span></span>
- <span data-ttu-id="41a92-118">Sospensione</span><span class="sxs-lookup"><span data-stu-id="41a92-118">Suspend</span></span>

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

### <span data-ttu-id="41a92-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="41a92-119">-InformationVariable</span></span>
<span data-ttu-id="41a92-120">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="41a92-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="41a92-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="41a92-121">-IPAddress</span></span>
<span data-ttu-id="41a92-122">Specifica l'indirizzo IP della rete virtuale statica a cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="41a92-122">Specifies the static virtual network IP address to query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a92-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="41a92-123">-Profile</span></span>
<span data-ttu-id="41a92-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41a92-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41a92-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="41a92-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41a92-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="41a92-126">-VNetName</span></span>
<span data-ttu-id="41a92-127">Specifica il nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="41a92-127">Specifies the Name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a92-128">CommonParameters</span></span>
<span data-ttu-id="41a92-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41a92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a92-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41a92-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a92-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41a92-131">INPUTS</span></span>

## <span data-ttu-id="41a92-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41a92-132">OUTPUTS</span></span>

## <span data-ttu-id="41a92-133">Note</span><span class="sxs-lookup"><span data-stu-id="41a92-133">NOTES</span></span>

## <span data-ttu-id="41a92-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41a92-134">RELATED LINKS</span></span>

[<span data-ttu-id="41a92-135">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="41a92-135">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="41a92-136">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="41a92-136">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


