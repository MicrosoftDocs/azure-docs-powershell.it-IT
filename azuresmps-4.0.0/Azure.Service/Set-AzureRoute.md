---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023781"
---
# <span data-ttu-id="021be-101">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="021be-101">Set-AzureRoute</span></span>

## <span data-ttu-id="021be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="021be-102">SYNOPSIS</span></span>
<span data-ttu-id="021be-103">Crea una route in una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="021be-103">Creates a route in a route table.</span></span>

## <span data-ttu-id="021be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="021be-104">SYNTAX</span></span>

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="021be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="021be-105">DESCRIPTION</span></span>
<span data-ttu-id="021be-106">Il cmdlet **set-AzureRoute** crea una route in una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="021be-106">The **Set-AzureRoute** cmdlet creates a route in a route table.</span></span>
<span data-ttu-id="021be-107">La nuova route ha effetto quasi immediatamente sulle macchine virtuali associate alla tabella route.</span><span class="sxs-lookup"><span data-stu-id="021be-107">The new route takes effect almost immediately on the virtual machines that are associated with the route table.</span></span>

## <span data-ttu-id="021be-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="021be-108">EXAMPLES</span></span>

### <span data-ttu-id="021be-109">Esempio 1: aggiungere una route hop Next appliance virtuale</span><span class="sxs-lookup"><span data-stu-id="021be-109">Example 1: Add a virtual appliance next hop route</span></span>
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="021be-110">Questo comando crea una tabella di route denominata ApplianceRouteTable nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="021be-110">This command creates a route table named ApplianceRouteTable in the specified location.</span></span>
<span data-ttu-id="021be-111">Il comando passa la tabella route al cmdlet Current.</span><span class="sxs-lookup"><span data-stu-id="021be-111">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="021be-112">Il cmdlet corrente aggiunge una route denominata ApplianceRoute03, che è un tipo di hop successivo di VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="021be-112">The current cmdlet adds a route named ApplianceRoute03, which is a VirtualAppliance next hop type.</span></span>
<span data-ttu-id="021be-113">Il comando specifica l'indirizzo IP dell'hop successivo e il prefisso dell'indirizzo per la route.</span><span class="sxs-lookup"><span data-stu-id="021be-113">The command specifies the next hop IP address and the address prefix for the route.</span></span>

### <span data-ttu-id="021be-114">Esempio 2: aggiungere una route hop Next Internet</span><span class="sxs-lookup"><span data-stu-id="021be-114">Example 2: Add an Internet next hop route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="021be-115">Questo comando consente di ottenere una tabella di route denominata ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="021be-115">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="021be-116">Il comando passa la tabella route al cmdlet Current.</span><span class="sxs-lookup"><span data-stu-id="021be-116">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="021be-117">Il cmdlet corrente aggiunge una route denominata InternetRoute, che è un tipo di hop successivo Internet.</span><span class="sxs-lookup"><span data-stu-id="021be-117">The current cmdlet adds a route named InternetRoute, which is an Internet next hop type.</span></span>
<span data-ttu-id="021be-118">Il comando specifica il prefisso dell'indirizzo per la route.</span><span class="sxs-lookup"><span data-stu-id="021be-118">The command specifies the address prefix for the route.</span></span>

## <span data-ttu-id="021be-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="021be-119">PARAMETERS</span></span>

### <span data-ttu-id="021be-120">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="021be-120">-AddressPrefix</span></span>
<span data-ttu-id="021be-121">Specifica un prefisso di indirizzo per la nuova route.</span><span class="sxs-lookup"><span data-stu-id="021be-121">Specifies an address prefix for the new route.</span></span>

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

### <span data-ttu-id="021be-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="021be-122">-NextHopIpAddress</span></span>
<span data-ttu-id="021be-123">Specifica l'indirizzo IP dell'appliance che rappresenta l'hop successivo per il traffico che usa questa route.</span><span class="sxs-lookup"><span data-stu-id="021be-123">Specifies the IP address of the appliance that is the next hop for traffic that uses this route.</span></span>
<span data-ttu-id="021be-124">Specificare questo valore solo se si specifica un valore di VirtualAppliance per il parametro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="021be-124">Specify this value only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="021be-125">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="021be-125">-NextHopType</span></span>
<span data-ttu-id="021be-126">Specifica il tipo di hop successivo per il traffico che usa questa route.</span><span class="sxs-lookup"><span data-stu-id="021be-126">Specifies the next hop type for traffic that uses this route.</span></span>
<span data-ttu-id="021be-127">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="021be-127">Valid values are:</span></span> 

- <span data-ttu-id="021be-128">VPNGateway</span><span class="sxs-lookup"><span data-stu-id="021be-128">VPNGateway</span></span>
- <span data-ttu-id="021be-129">VNETLocal</span><span class="sxs-lookup"><span data-stu-id="021be-129">VNETLocal</span></span>
- <span data-ttu-id="021be-130">Internet</span><span class="sxs-lookup"><span data-stu-id="021be-130">Internet</span></span>
- <span data-ttu-id="021be-131">VirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="021be-131">VirtualAppliance</span></span>
- <span data-ttu-id="021be-132">Null</span><span class="sxs-lookup"><span data-stu-id="021be-132">Null</span></span>

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

### <span data-ttu-id="021be-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="021be-133">-Profile</span></span>
<span data-ttu-id="021be-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021be-134">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="021be-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="021be-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="021be-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="021be-136">-RouteName</span></span>
<span data-ttu-id="021be-137">Specifica un nome per la nuova route aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021be-137">Specifies a name for the new route that this cmdlet adds.</span></span>

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

### <span data-ttu-id="021be-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="021be-138">-RouteTable</span></span>
<span data-ttu-id="021be-139">Specifica la tabella di route a cui questo cmdlet aggiunge la nuova route.</span><span class="sxs-lookup"><span data-stu-id="021be-139">Specifies the route table to which this cmdlet adds the new route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="021be-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021be-140">CommonParameters</span></span>
<span data-ttu-id="021be-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="021be-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021be-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="021be-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021be-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="021be-143">INPUTS</span></span>

## <span data-ttu-id="021be-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="021be-144">OUTPUTS</span></span>

## <span data-ttu-id="021be-145">Note</span><span class="sxs-lookup"><span data-stu-id="021be-145">NOTES</span></span>

## <span data-ttu-id="021be-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="021be-146">RELATED LINKS</span></span>

[<span data-ttu-id="021be-147">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="021be-147">Remove-AzureRoute</span></span>](./Remove-AzureRoute.md)


