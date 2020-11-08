---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029649"
---
# <span data-ttu-id="983db-101">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="983db-101">New-AzureVNetGateway</span></span>

## <span data-ttu-id="983db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="983db-102">SYNOPSIS</span></span>
<span data-ttu-id="983db-103">Crea un gateway VPN in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="983db-103">Creates a VPN gateway in a virtual network.</span></span>

## <span data-ttu-id="983db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="983db-104">SYNTAX</span></span>

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="983db-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="983db-105">DESCRIPTION</span></span>
<span data-ttu-id="983db-106">Il cmdlet **New-AzureVNetGateway** crea un gateway VPN (Virtual Private Network) in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="983db-106">The **New-AzureVNetGateway** cmdlet creates a virtual private network (VPN) gateway in a virtual network.</span></span>
<span data-ttu-id="983db-107">È anche possibile specificare l'USK del gateway, ovvero default, standard o HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="983db-107">You can also specify the SKU of the gateway, either Default, Standard, or HighPerformance.</span></span>
<span data-ttu-id="983db-108">Puoi specificare il tipo, StaticRouting o DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="983db-108">You can specify the type, either StaticRouting or DynamicRouting.</span></span>

## <span data-ttu-id="983db-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="983db-109">EXAMPLES</span></span>

### <span data-ttu-id="983db-110">Esempio 1: creare un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="983db-110">Example 1: Create a virtual network gateway</span></span>
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

<span data-ttu-id="983db-111">Questo comando crea un gateway di rete virtuale per la rete virtuale denominata ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="983db-111">This command creates a virtual network gateway for the virtual network named ContosoVN07.</span></span>
<span data-ttu-id="983db-112">Il gateway è l'USK predefinito e usa il routing dinamico.</span><span class="sxs-lookup"><span data-stu-id="983db-112">The gateway is the Default SKU and uses dynamic routing.</span></span>

## <span data-ttu-id="983db-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="983db-113">PARAMETERS</span></span>

### <span data-ttu-id="983db-114">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="983db-114">-GatewaySKU</span></span>
<span data-ttu-id="983db-115">Specifica l'USK del gateway di rete virtuale creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="983db-115">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="983db-116">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="983db-116">Valid values are:</span></span> 

- <span data-ttu-id="983db-117">Predefinita</span><span class="sxs-lookup"><span data-stu-id="983db-117">Default</span></span> 
- <span data-ttu-id="983db-118">Standard</span><span class="sxs-lookup"><span data-stu-id="983db-118">Standard</span></span> 
- <span data-ttu-id="983db-119">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="983db-119">HighPerformance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983db-120">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="983db-120">-GatewayType</span></span>
<span data-ttu-id="983db-121">Specifica il tipo di gateway creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="983db-121">Specifies the type of gateway that this cmdlet creates.</span></span>
<span data-ttu-id="983db-122">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="983db-122">Valid values are:</span></span> 

- <span data-ttu-id="983db-123">StaticRouting</span><span class="sxs-lookup"><span data-stu-id="983db-123">StaticRouting</span></span> 
- <span data-ttu-id="983db-124">DynamicRouting</span><span class="sxs-lookup"><span data-stu-id="983db-124">DynamicRouting</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="983db-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="983db-125">-Profile</span></span>
<span data-ttu-id="983db-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="983db-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="983db-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="983db-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="983db-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="983db-128">-VNetName</span></span>
<span data-ttu-id="983db-129">Specifica la rete virtuale in cui questo cmdlet aggiunge un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="983db-129">Specifies the virtual network in which this cmdlet adds a virtual network gateway.</span></span>

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

### <span data-ttu-id="983db-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="983db-130">CommonParameters</span></span>
<span data-ttu-id="983db-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="983db-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="983db-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="983db-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="983db-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="983db-133">INPUTS</span></span>

## <span data-ttu-id="983db-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="983db-134">OUTPUTS</span></span>

## <span data-ttu-id="983db-135">Note</span><span class="sxs-lookup"><span data-stu-id="983db-135">NOTES</span></span>

## <span data-ttu-id="983db-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="983db-136">RELATED LINKS</span></span>

[<span data-ttu-id="983db-137">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="983db-137">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="983db-138">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="983db-138">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="983db-139">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="983db-139">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="983db-140">Ridimensionare-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="983db-140">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="983db-141">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="983db-141">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


