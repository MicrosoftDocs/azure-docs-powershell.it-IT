---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029989"
---
# <span data-ttu-id="d8adb-101">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="d8adb-101">Get-AzureVNetSite</span></span>

## <span data-ttu-id="d8adb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8adb-102">SYNOPSIS</span></span>
<span data-ttu-id="d8adb-103">Ottiene un oggetto elenco con informazioni sulle reti virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8adb-103">Gets a list object with information about Azure virtual networks.</span></span>

## <span data-ttu-id="d8adb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8adb-104">SYNTAX</span></span>

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d8adb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8adb-105">DESCRIPTION</span></span>
<span data-ttu-id="d8adb-106">Il cmdlet **Get-AzureVNetSite** ottiene un oggetto elenco con informazioni sulle reti virtuali Azure per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d8adb-106">The **Get-AzureVNetSite** cmdlet gets a list object with information about Azure virtual networks for the current subscription.</span></span>
<span data-ttu-id="d8adb-107">Se si specifica un nome di rete virtuale, vengono restituite solo le informazioni relative alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d8adb-107">If you specify a virtual network name, only information for that virtual network is returned.</span></span>

## <span data-ttu-id="d8adb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8adb-108">EXAMPLES</span></span>

### <span data-ttu-id="d8adb-109">Esempio 1: ottenere informazioni su tutte le reti virtuali nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="d8adb-109">Example 1: Get information about all virtual networks in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite
```

<span data-ttu-id="d8adb-110">Questo comando consente di ottenere informazioni su tutte le reti virtuali nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d8adb-110">This command gets information about all the virtual networks in the current subscription.</span></span>

### <span data-ttu-id="d8adb-111">Esempio 2: ottenere informazioni su una rete virtuale specifica nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="d8adb-111">Example 2: Get information about a specific virtual network in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

<span data-ttu-id="d8adb-112">Questo comando recupera solo le informazioni sulla rete virtuale MyProductionNetwork.</span><span class="sxs-lookup"><span data-stu-id="d8adb-112">This command retrieves information on the MyProductionNetwork virtual network only.</span></span>

## <span data-ttu-id="d8adb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8adb-113">PARAMETERS</span></span>

### <span data-ttu-id="d8adb-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d8adb-114">-InformationAction</span></span>
<span data-ttu-id="d8adb-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d8adb-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d8adb-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8adb-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8adb-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="d8adb-117">Continue</span></span>
- <span data-ttu-id="d8adb-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="d8adb-118">Ignore</span></span>
- <span data-ttu-id="d8adb-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d8adb-119">Inquire</span></span>
- <span data-ttu-id="d8adb-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d8adb-120">SilentlyContinue</span></span>
- <span data-ttu-id="d8adb-121">Stop</span><span class="sxs-lookup"><span data-stu-id="d8adb-121">Stop</span></span>
- <span data-ttu-id="d8adb-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d8adb-122">Suspend</span></span>

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

### <span data-ttu-id="d8adb-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d8adb-123">-InformationVariable</span></span>
<span data-ttu-id="d8adb-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d8adb-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d8adb-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="d8adb-125">-Profile</span></span>
<span data-ttu-id="d8adb-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8adb-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8adb-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d8adb-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8adb-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d8adb-128">-VNetName</span></span>
<span data-ttu-id="d8adb-129">Specifica un nome di rete virtuale per cui restituire informazioni.</span><span class="sxs-lookup"><span data-stu-id="d8adb-129">Specifies a virtual network name to return information about.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8adb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8adb-130">CommonParameters</span></span>
<span data-ttu-id="d8adb-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8adb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8adb-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8adb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8adb-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8adb-133">INPUTS</span></span>

## <span data-ttu-id="d8adb-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8adb-134">OUTPUTS</span></span>

## <span data-ttu-id="d8adb-135">Note</span><span class="sxs-lookup"><span data-stu-id="d8adb-135">NOTES</span></span>

## <span data-ttu-id="d8adb-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8adb-136">RELATED LINKS</span></span>

[<span data-ttu-id="d8adb-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="d8adb-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="d8adb-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="d8adb-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="d8adb-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="d8adb-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


