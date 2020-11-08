---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A40F3BBB-4DC6-452E-A939-ED610F541EB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7797c916813c985802a0a2f63a5a43e033009a06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029648"
---
# <span data-ttu-id="3483c-101">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3483c-101">New-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="3483c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3483c-102">SYNOPSIS</span></span>
<span data-ttu-id="3483c-103">Crea un gateway di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="3483c-103">Creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="3483c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3483c-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGateway -VNetName <String> -GatewayName <String> [-GatewayType <String>]
 [-GatewaySKU <String>] [-Location <String>] [-VnetId <String>] [-Asn <UInt32>] [-PeerWeight <Int32>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3483c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3483c-105">DESCRIPTION</span></span>
<span data-ttu-id="3483c-106">Il cmdlet **New-AzureVirtualNetworkGateway** crea un gateway di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="3483c-106">The **New-AzureVirtualNetworkGateway** cmdlet creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="3483c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3483c-107">EXAMPLES</span></span>

## <span data-ttu-id="3483c-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3483c-108">PARAMETERS</span></span>

### <span data-ttu-id="3483c-109">-ASN</span><span class="sxs-lookup"><span data-stu-id="3483c-109">-Asn</span></span>
<span data-ttu-id="3483c-110">Specifica il numero di sistema autonomo (ASN).</span><span class="sxs-lookup"><span data-stu-id="3483c-110">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3483c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3483c-111">-Force</span></span>
<span data-ttu-id="3483c-112">Non confermare la creazione di gateway di rete virtuale Azure</span><span class="sxs-lookup"><span data-stu-id="3483c-112">Do not confirm Azure Virtual Network Gateway Creation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3483c-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="3483c-113">-GatewayName</span></span>
<span data-ttu-id="3483c-114">Specifica il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="3483c-114">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="3483c-115">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="3483c-115">-GatewaySKU</span></span>
<span data-ttu-id="3483c-116">Specifica l'USK del gateway di rete virtuale creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3483c-116">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="3483c-117">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="3483c-117">Valid values are:</span></span>

- <span data-ttu-id="3483c-118">Predefinita</span><span class="sxs-lookup"><span data-stu-id="3483c-118">Default</span></span>
- <span data-ttu-id="3483c-119">Standard</span><span class="sxs-lookup"><span data-stu-id="3483c-119">Standard</span></span>
- <span data-ttu-id="3483c-120">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="3483c-120">HighPerformance</span></span>

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

### <span data-ttu-id="3483c-121">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="3483c-121">-GatewayType</span></span>
<span data-ttu-id="3483c-122">Specifica il tipo di gateway.</span><span class="sxs-lookup"><span data-stu-id="3483c-122">Specifies the type of gateway.</span></span>

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

### <span data-ttu-id="3483c-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3483c-123">-Location</span></span>
<span data-ttu-id="3483c-124">Specifica la posizione.</span><span class="sxs-lookup"><span data-stu-id="3483c-124">Specifies the location.</span></span>

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

### <span data-ttu-id="3483c-125">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3483c-125">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3483c-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="3483c-126">-Profile</span></span>
<span data-ttu-id="3483c-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3483c-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3483c-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3483c-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3483c-129">-VnetId</span><span class="sxs-lookup"><span data-stu-id="3483c-129">-VnetId</span></span>
<span data-ttu-id="3483c-130">Specifica l'ID di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3483c-130">Specifies the ID of a virtual network.</span></span>

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

### <span data-ttu-id="3483c-131">-VNetName</span><span class="sxs-lookup"><span data-stu-id="3483c-131">-VNetName</span></span>
<span data-ttu-id="3483c-132">Specifica una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3483c-132">Specifies a virtual network.</span></span>

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

### <span data-ttu-id="3483c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3483c-133">CommonParameters</span></span>
<span data-ttu-id="3483c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3483c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3483c-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3483c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3483c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3483c-136">INPUTS</span></span>

## <span data-ttu-id="3483c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3483c-137">OUTPUTS</span></span>

## <span data-ttu-id="3483c-138">Note</span><span class="sxs-lookup"><span data-stu-id="3483c-138">NOTES</span></span>

## <span data-ttu-id="3483c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3483c-139">RELATED LINKS</span></span>

[<span data-ttu-id="3483c-140">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3483c-140">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="3483c-141">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3483c-141">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="3483c-142">Ridimensionare-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3483c-142">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)
