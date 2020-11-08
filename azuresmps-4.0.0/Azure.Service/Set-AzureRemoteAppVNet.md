---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 97B96661-E60A-4505-AD06-D2A541DB820E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19f7b09d26df88591e03acf8b01842efdead05e2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029514"
---
# <span data-ttu-id="3be1d-101">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="3be1d-101">Set-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="3be1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3be1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3be1d-103">Imposta le proprietà di una rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3be1d-103">Sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="3be1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3be1d-104">SYNTAX</span></span>

```
Set-AzureRemoteAppVNet -VNetName <String> [-VirtualNetworkAddressSpace <String[]>]
 [-LocalNetworkAddressSpace <String[]>] [-DnsServerIpAddress <String[]>] [-VpnDeviceIpAddress <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3be1d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3be1d-105">DESCRIPTION</span></span>
<span data-ttu-id="3be1d-106">Il cmdlet **set-AzureRemoteAppVNet** imposta le proprietà di una rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3be1d-106">The **Set-AzureRemoteAppVNet** cmdlet sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="3be1d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3be1d-107">EXAMPLES</span></span>

### <span data-ttu-id="3be1d-108">Esempio 1: impostare le proprietà di una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="3be1d-108">Example 1: Set the properties of a virtual network</span></span>
```
PS C:\> Set-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "131.253.33.200" -LocalNetworkAddressSpace "192.168.0.0/24" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.253.33.200"
```

<span data-ttu-id="3be1d-109">Questo comando imposta le proprietà di una rete virtuale denominata ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="3be1d-109">This command sets the properties of a virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="3be1d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3be1d-110">PARAMETERS</span></span>

### <span data-ttu-id="3be1d-111">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="3be1d-111">-DnsServerIpAddress</span></span>
<span data-ttu-id="3be1d-112">Specifica gli indirizzi IPv4 dei server DNS.</span><span class="sxs-lookup"><span data-stu-id="3be1d-112">Specifies the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3be1d-113">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="3be1d-113">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="3be1d-114">Specifica lo spazio degli indirizzi di rete locale, in classi Inter-Domain la notazione CIDR (routing).</span><span class="sxs-lookup"><span data-stu-id="3be1d-114">Specifies the local network address space, in Classes Inter-Domain Routing (CIDR) notation.</span></span>
<span data-ttu-id="3be1d-115">Questa operazione non deve sovrapporsi allo spazio degli indirizzi di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3be1d-115">This must not overlap the virtual network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3be1d-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="3be1d-116">-Profile</span></span>
<span data-ttu-id="3be1d-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3be1d-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3be1d-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3be1d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3be1d-119">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="3be1d-119">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="3be1d-120">Specifica lo spazio degli indirizzi di rete virtuale nella notazione CIDR.</span><span class="sxs-lookup"><span data-stu-id="3be1d-120">Specifies the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="3be1d-121">Questo deve essere nell'intervallo di indirizzi IP privati e non può sovrapporsi allo spazio di indirizzi di rete locale.</span><span class="sxs-lookup"><span data-stu-id="3be1d-121">This must be in the private IP address range and cannot overlap the local network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3be1d-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="3be1d-122">-VNetName</span></span>
<span data-ttu-id="3be1d-123">Specifica il nome della rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3be1d-123">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="3be1d-124">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="3be1d-124">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="3be1d-125">Specifica l'indirizzo del dispositivo VPN (Virtual Private Network).</span><span class="sxs-lookup"><span data-stu-id="3be1d-125">Specifies the address of the Virtual Private Network (VPN) device.</span></span>
<span data-ttu-id="3be1d-126">Deve essere un indirizzo pubblico.</span><span class="sxs-lookup"><span data-stu-id="3be1d-126">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3be1d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be1d-127">CommonParameters</span></span>
<span data-ttu-id="3be1d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3be1d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be1d-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3be1d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be1d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3be1d-130">INPUTS</span></span>

## <span data-ttu-id="3be1d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3be1d-131">OUTPUTS</span></span>

## <span data-ttu-id="3be1d-132">Note</span><span class="sxs-lookup"><span data-stu-id="3be1d-132">NOTES</span></span>

## <span data-ttu-id="3be1d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3be1d-133">RELATED LINKS</span></span>

[<span data-ttu-id="3be1d-134">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="3be1d-134">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)


