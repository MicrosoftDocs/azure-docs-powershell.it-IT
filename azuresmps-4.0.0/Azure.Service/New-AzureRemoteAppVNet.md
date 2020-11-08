---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023952"
---
# <span data-ttu-id="d3394-101">New-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="d3394-101">New-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="d3394-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3394-102">SYNOPSIS</span></span>
<span data-ttu-id="d3394-103">Crea una rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d3394-103">Creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="d3394-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3394-104">SYNTAX</span></span>

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d3394-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3394-105">DESCRIPTION</span></span>
<span data-ttu-id="d3394-106">Il cmdlet **New-AzureRemoteAppVNet** crea una rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d3394-106">The **New-AzureRemoteAppVNet** cmdlet creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="d3394-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3394-107">EXAMPLES</span></span>

### <span data-ttu-id="d3394-108">Esempio 1: creare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d3394-108">Example 1: Create a virtual network</span></span>
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

<span data-ttu-id="d3394-109">Questo comando crea una rete virtuale denominata ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="d3394-109">This command creates a virtual network named ContosoVNet.</span></span>

<span data-ttu-id="d3394-110">Per determinare lo stato dell'operazione, usare il cmdlet **Get-AzureRemoteAppOperationResult** con l'ID di rilevamento restituito dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3394-110">To determine the status of the operation, use the **Get-AzureRemoteAppOperationResult** cmdlet with the tracking ID that this cmdlet returns.</span></span>

## <span data-ttu-id="d3394-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3394-111">PARAMETERS</span></span>

### <span data-ttu-id="d3394-112">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3394-112">-DnsServerIpAddress</span></span>
<span data-ttu-id="d3394-113">Specifica una matrice degli indirizzi IPv4 dei server DNS.</span><span class="sxs-lookup"><span data-stu-id="d3394-113">Specifies an array of the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3394-114">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="d3394-114">-GatewayType</span></span>
<span data-ttu-id="d3394-115">Specifica il tipo di routing del gateway da usare.</span><span class="sxs-lookup"><span data-stu-id="d3394-115">Specifies the type of gateway routing to use.</span></span>
<span data-ttu-id="d3394-116">I valori accettabili per questo parametro sono: StaticRouting o DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="d3394-116">The acceptable values for this parameter are:  StaticRouting or DynamicRouting.</span></span>

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3394-117">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="d3394-117">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="d3394-118">Specifica una matrice di stringhe che specificano lo spazio degli indirizzi di rete locale, nella notazione CIDR (classe Interdomain Routing).</span><span class="sxs-lookup"><span data-stu-id="d3394-118">Specifies an array of strings that specify the local network address space, in Classless Interdomain Routing (CIDR) notation.</span></span>
<span data-ttu-id="d3394-119">Questo spazio indirizzo non deve sovrapporsi allo spazio di indirizzi di rete virtuale specificato dal parametro *VirtualNetworkAddressSpace* .</span><span class="sxs-lookup"><span data-stu-id="d3394-119">This address space must not overlap with the virtual network address space that the *VirtualNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3394-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d3394-120">-Location</span></span>
<span data-ttu-id="d3394-121">Specifica la posizione in cui creare la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3394-121">Specifies the location in which to create the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3394-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="d3394-122">-Profile</span></span>
<span data-ttu-id="d3394-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3394-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3394-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d3394-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3394-125">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="d3394-125">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="d3394-126">Specifica una matrice di stringa che specifica lo spazio degli indirizzi di rete virtuale nella notazione CIDR.</span><span class="sxs-lookup"><span data-stu-id="d3394-126">Specifies an array of string that specify the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="d3394-127">Deve essere nell'intervallo di indirizzi IP privati e non può sovrapporsi allo spazio di indirizzi di rete locale specificato dal parametro *LocalNetworkAddressSpace* .</span><span class="sxs-lookup"><span data-stu-id="d3394-127">This must be in the private IP address range and cannot overlap with the local network address space that the *LocalNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3394-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d3394-128">-VNetName</span></span>
<span data-ttu-id="d3394-129">Specifica il nome della rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d3394-129">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3394-130">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3394-130">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="d3394-131">Specifica l'indirizzo del dispositivo VPN (Virtual Private Network).</span><span class="sxs-lookup"><span data-stu-id="d3394-131">Specifies the address of the virtual private network (VPN) device.</span></span>
<span data-ttu-id="d3394-132">Deve essere un indirizzo pubblico.</span><span class="sxs-lookup"><span data-stu-id="d3394-132">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3394-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3394-133">CommonParameters</span></span>
<span data-ttu-id="d3394-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3394-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3394-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3394-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3394-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3394-136">INPUTS</span></span>

## <span data-ttu-id="d3394-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3394-137">OUTPUTS</span></span>

## <span data-ttu-id="d3394-138">Note</span><span class="sxs-lookup"><span data-stu-id="d3394-138">NOTES</span></span>

## <span data-ttu-id="d3394-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3394-139">RELATED LINKS</span></span>

[<span data-ttu-id="d3394-140">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="d3394-140">Get-AzureRemoteAppOperationResult</span></span>](./Get-AzureRemoteAppOperationResult.md)

[<span data-ttu-id="d3394-141">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="d3394-141">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="d3394-142">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="d3394-142">Remove-AzureRemoteAppVNet</span></span>](./Remove-AzureRemoteAppVNet.md)

[<span data-ttu-id="d3394-143">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="d3394-143">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


