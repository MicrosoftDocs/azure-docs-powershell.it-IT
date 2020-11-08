---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029549"
---
# <span data-ttu-id="f1147-101">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="f1147-101">Resize-AzureVNetGateway</span></span>

## <span data-ttu-id="f1147-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1147-102">SYNOPSIS</span></span>
<span data-ttu-id="f1147-103">Ridimensiona un gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="f1147-103">Resizes a VPN gateway.</span></span>

## <span data-ttu-id="f1147-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1147-104">SYNTAX</span></span>

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1147-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1147-105">DESCRIPTION</span></span>
<span data-ttu-id="f1147-106">Il cmdlet **Resize-AzureVNetGateway** consente di ridimensionare un gateway VPN (Virtual Private Network) Virtual Network in un altro SKU.</span><span class="sxs-lookup"><span data-stu-id="f1147-106">The **Resize-AzureVNetGateway** cmdlet resizes a virtual network virtual private network (VPN) gateway to a different SKU.</span></span>
<span data-ttu-id="f1147-107">Gli SKU validi per un gateway di rete virtuale sono default, standard e HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="f1147-107">Valid SKUs for a virtual network gateway are Default, Standard, and HighPerformance.</span></span>

## <span data-ttu-id="f1147-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1147-108">EXAMPLES</span></span>

### <span data-ttu-id="f1147-109">Esempio 1: modificare l'USK per un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f1147-109">Example 1: Change the SKU for a virtual network gateway</span></span>
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

<span data-ttu-id="f1147-110">Questo comando cambia l'USK del gateway di rete virtuale per la rete virtuale denominata ContosoVN07 in HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="f1147-110">This command changes the SKU of the virtual network gateway for the virtual network named ContosoVN07 to HighPerformance.</span></span>

## <span data-ttu-id="f1147-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1147-111">PARAMETERS</span></span>

### <span data-ttu-id="f1147-112">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="f1147-112">-GatewaySKU</span></span>
<span data-ttu-id="f1147-113">Specifica l'USK a cui questo cmdlet ridimensiona il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1147-113">Specifies the SKU to which this cmdlet resizes virtual network gateway.</span></span>
<span data-ttu-id="f1147-114">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f1147-114">Valid values are:</span></span> 

- <span data-ttu-id="f1147-115">Predefinita</span><span class="sxs-lookup"><span data-stu-id="f1147-115">Default</span></span> 
- <span data-ttu-id="f1147-116">Standard</span><span class="sxs-lookup"><span data-stu-id="f1147-116">Standard</span></span> 
- <span data-ttu-id="f1147-117">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="f1147-117">HighPerformance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1147-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="f1147-118">-Profile</span></span>
<span data-ttu-id="f1147-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1147-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f1147-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f1147-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f1147-121">-VNetName</span><span class="sxs-lookup"><span data-stu-id="f1147-121">-VNetName</span></span>
<span data-ttu-id="f1147-122">Specifica la rete virtuale in cui questo cmdlet ridimensiona un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1147-122">Specifies the virtual network in which this cmdlet resizes a virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1147-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1147-123">CommonParameters</span></span>
<span data-ttu-id="f1147-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1147-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1147-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1147-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1147-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1147-126">INPUTS</span></span>

## <span data-ttu-id="f1147-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1147-127">OUTPUTS</span></span>

## <span data-ttu-id="f1147-128">Note</span><span class="sxs-lookup"><span data-stu-id="f1147-128">NOTES</span></span>

## <span data-ttu-id="f1147-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1147-129">RELATED LINKS</span></span>

[<span data-ttu-id="f1147-130">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="f1147-130">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="f1147-131">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="f1147-131">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="f1147-132">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="f1147-132">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="f1147-133">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="f1147-133">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="f1147-134">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="f1147-134">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


