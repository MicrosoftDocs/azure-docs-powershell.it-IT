---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DF95285F-97F4-4064-8E27-EE6E93843E55
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a14865c986bf6439df833a38f87835792a6e3c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023584"
---
# <span data-ttu-id="25ddd-101">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="25ddd-101">Get-AzureRemoteAppVpnDevice</span></span>

## <span data-ttu-id="25ddd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="25ddd-103">Recupera le informazioni su un dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="25ddd-103">Retrieves information about a VPN device.</span></span>

## <span data-ttu-id="25ddd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25ddd-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDevice [-VNetName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="25ddd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="25ddd-106">Il cmdlet **Get-AzureRemoteAppVpnDevice** recupera le informazioni su un dispositivo VPN (Virtual Private Network).</span><span class="sxs-lookup"><span data-stu-id="25ddd-106">The **Get-AzureRemoteAppVpnDevice** cmdlet retrieves information about a virtual private network (VPN) device.</span></span>

## <span data-ttu-id="25ddd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25ddd-107">EXAMPLES</span></span>

### <span data-ttu-id="25ddd-108">Esempio 1: restituire le configurazioni dei dispositivi VPN disponibili per una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="25ddd-108">Example 1: Return the available VPN device configurations for a virtual network</span></span>
```
PS C:\> Get-AzureRemoteVpnDevice -VNetName "ContosoVNet"


Name                   Platforms

----                   ---------

Cisco Systems, Inc.    {ASA 5500 Series Adaptive Security Appliances, ASR 1000 Series Aggregation Services Routers, ASR 1000 Series Aggregation Services Routers - Dynamic Routing, ISR Series Integrated Services Routers...} 

Juniper Networks, Inc. {SRX Series Routers, SRX Series Routers - Dynamic Routing, J Series Routers, J Series Routers - Dynamic Routing...} 

Microsoft Corporation  {RRAS}
```

<span data-ttu-id="25ddd-109">Questo comando restituisce le configurazioni dei dispositivi VPN disponibili per la rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="25ddd-109">This command returns the available VPN device configurations for the specified virtual network.</span></span>

## <span data-ttu-id="25ddd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25ddd-110">PARAMETERS</span></span>

### <span data-ttu-id="25ddd-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="25ddd-111">-Profile</span></span>
<span data-ttu-id="25ddd-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25ddd-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25ddd-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="25ddd-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25ddd-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="25ddd-114">-VNetName</span></span>
<span data-ttu-id="25ddd-115">Specifica il nome della rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="25ddd-115">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25ddd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ddd-116">CommonParameters</span></span>
<span data-ttu-id="25ddd-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25ddd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ddd-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25ddd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ddd-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25ddd-119">INPUTS</span></span>

## <span data-ttu-id="25ddd-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25ddd-120">OUTPUTS</span></span>

### <span data-ttu-id="25ddd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="25ddd-121">System.String</span></span>

## <span data-ttu-id="25ddd-122">Note</span><span class="sxs-lookup"><span data-stu-id="25ddd-122">NOTES</span></span>

## <span data-ttu-id="25ddd-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25ddd-123">RELATED LINKS</span></span>

[<span data-ttu-id="25ddd-124">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="25ddd-124">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="25ddd-125">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="25ddd-125">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


