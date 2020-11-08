---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6D23ECB-C06E-4EB7-8096-33787E39694D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66f6bac80b219a2b3629b399bb568140a5cef217
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023912"
---
# <span data-ttu-id="ccbc0-101">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ccbc0-101">Set-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="ccbc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ccbc0-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbc0-103">Modifica una configurazione di bilanciamento del carico interna in un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-103">Modifies an internal load balancer configuration in an Azure service.</span></span>

## <span data-ttu-id="ccbc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ccbc0-104">SYNTAX</span></span>

### <span data-ttu-id="ccbc0-105">ServiceAndSlot (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ccbc0-105">ServiceAndSlot (Default)</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccbc0-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="ccbc0-106">SubnetNameOnly</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ccbc0-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="ccbc0-107">SubnetNameAndIP</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ccbc0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccbc0-108">DESCRIPTION</span></span>
<span data-ttu-id="ccbc0-109">Il cmdlet **set-AzureInternalLoadBalancer** modifica una configurazione di bilanciamento del carico interna in un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-109">The **Set-AzureInternalLoadBalancer** cmdlet modifies an internal load balancer configuration in an Azure service.</span></span>
<span data-ttu-id="ccbc0-110">Per una rete virtuale, è possibile specificare una subnet o l'indirizzo IP del sistema di bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="ccbc0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ccbc0-111">EXAMPLES</span></span>

### <span data-ttu-id="ccbc0-112">1:</span><span class="sxs-lookup"><span data-stu-id="ccbc0-112">1:</span></span>
```

```

## <span data-ttu-id="ccbc0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ccbc0-113">PARAMETERS</span></span>

### <span data-ttu-id="ccbc0-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ccbc0-114">-InformationAction</span></span>
<span data-ttu-id="ccbc0-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ccbc0-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ccbc0-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ccbc0-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="ccbc0-117">Continue</span></span>
- <span data-ttu-id="ccbc0-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="ccbc0-118">Ignore</span></span>
- <span data-ttu-id="ccbc0-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="ccbc0-119">Inquire</span></span>
- <span data-ttu-id="ccbc0-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ccbc0-120">SilentlyContinue</span></span>
- <span data-ttu-id="ccbc0-121">Stop</span><span class="sxs-lookup"><span data-stu-id="ccbc0-121">Stop</span></span>
- <span data-ttu-id="ccbc0-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="ccbc0-122">Suspend</span></span>

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

### <span data-ttu-id="ccbc0-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ccbc0-123">-InformationVariable</span></span>
<span data-ttu-id="ccbc0-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ccbc0-125">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="ccbc0-125">-InternalLoadBalancerName</span></span>
<span data-ttu-id="ccbc0-126">Specifica il nome del bilanciamento del carico interno che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-126">Specifies the name of the internal load balancer that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbc0-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="ccbc0-127">-Profile</span></span>
<span data-ttu-id="ccbc0-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ccbc0-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ccbc0-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ccbc0-130">-ServiceName</span></span>
<span data-ttu-id="ccbc0-131">Specifica il nome del servizio in cui questo cmdlet modifica un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-131">Specifies the name of the service in which this cmdlet modifies an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbc0-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="ccbc0-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="ccbc0-133">Specifica l'indirizzo IP di rete virtuale per un sistema di bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-133">Specifies the virtual network IP address for an internal load balancer.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbc0-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ccbc0-134">-SubnetName</span></span>
<span data-ttu-id="ccbc0-135">Specifica il nome della subnet per un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbc0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbc0-136">CommonParameters</span></span>
<span data-ttu-id="ccbc0-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccbc0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbc0-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccbc0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbc0-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ccbc0-139">INPUTS</span></span>

## <span data-ttu-id="ccbc0-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ccbc0-140">OUTPUTS</span></span>

## <span data-ttu-id="ccbc0-141">Note</span><span class="sxs-lookup"><span data-stu-id="ccbc0-141">NOTES</span></span>

## <span data-ttu-id="ccbc0-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ccbc0-142">RELATED LINKS</span></span>

[<span data-ttu-id="ccbc0-143">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ccbc0-143">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="ccbc0-144">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ccbc0-144">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="ccbc0-145">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="ccbc0-145">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="ccbc0-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ccbc0-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)


