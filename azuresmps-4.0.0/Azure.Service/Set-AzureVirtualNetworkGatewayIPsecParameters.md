---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 150EE0DC-07CD-4E24-AF70-0C1A7BB61433
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b663ced66318335afb1fe4c3bf0e6a1520ede7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029874"
---
# <span data-ttu-id="3dc8f-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="3dc8f-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="3dc8f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dc8f-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc8f-103">Imposta i parametri IPsec per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-103">Sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="3dc8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dc8f-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3dc8f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dc8f-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc8f-106">Il cmdlet **set-AzureVirtualNetworkGatewayIPsecParameters** imposta i parametri IPSec per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-106">The **Set-AzureVirtualNetworkGatewayIPsecParameters** cmdlet sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="3dc8f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dc8f-107">EXAMPLES</span></span>

## <span data-ttu-id="3dc8f-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dc8f-108">PARAMETERS</span></span>

### <span data-ttu-id="3dc8f-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="3dc8f-109">-ConnectedEntityId</span></span>
<span data-ttu-id="3dc8f-110">Specifica l'ID di un'entità connessa.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="3dc8f-111">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="3dc8f-111">-EncryptionType</span></span>
<span data-ttu-id="3dc8f-112">Specifica il tipo di crittografia per il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-112">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="3dc8f-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3dc8f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3dc8f-114">NoEncryption</span><span class="sxs-lookup"><span data-stu-id="3dc8f-114">NoEncryption</span></span>
- <span data-ttu-id="3dc8f-115">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="3dc8f-115">RequireEncryption</span></span>

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

### <span data-ttu-id="3dc8f-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3dc8f-116">-GatewayId</span></span>
<span data-ttu-id="3dc8f-117">Specifica l'ID di un gateway.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="3dc8f-118">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="3dc8f-118">-PfsGroup</span></span>
<span data-ttu-id="3dc8f-119">Specifica il gruppo di segretezza avanzata (PFS) ideale.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-119">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="3dc8f-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3dc8f-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3dc8f-121">PFS1</span><span class="sxs-lookup"><span data-stu-id="3dc8f-121">PFS1</span></span>
- <span data-ttu-id="3dc8f-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3dc8f-122">None</span></span>

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

### <span data-ttu-id="3dc8f-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="3dc8f-123">-Profile</span></span>
<span data-ttu-id="3dc8f-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3dc8f-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3dc8f-126">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="3dc8f-126">-SADataSizeKilobytes</span></span>
<span data-ttu-id="3dc8f-127">Specifica le dimensioni, in kilobyte, dell'associazione di sicurezza (SA).</span><span class="sxs-lookup"><span data-stu-id="3dc8f-127">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="3dc8f-128">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="3dc8f-128">-SALifetimeSeconds</span></span>
<span data-ttu-id="3dc8f-129">Specifica il periodo, in secondi, dell'associazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-129">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="3dc8f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc8f-130">CommonParameters</span></span>
<span data-ttu-id="3dc8f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc8f-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dc8f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc8f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dc8f-133">INPUTS</span></span>

## <span data-ttu-id="3dc8f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dc8f-134">OUTPUTS</span></span>

## <span data-ttu-id="3dc8f-135">Note</span><span class="sxs-lookup"><span data-stu-id="3dc8f-135">NOTES</span></span>

## <span data-ttu-id="3dc8f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dc8f-136">RELATED LINKS</span></span>

[<span data-ttu-id="3dc8f-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="3dc8f-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Get-AzureVirtualNetworkGatewayIPsecParameters.md)


