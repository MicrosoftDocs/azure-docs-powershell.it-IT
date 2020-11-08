---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023682"
---
# <span data-ttu-id="61f20-101">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="61f20-101">Add-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="61f20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61f20-102">SYNOPSIS</span></span>
<span data-ttu-id="61f20-103">Aggiunge un bilanciamento del carico interno a un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="61f20-103">Adds an internal load balancer to an Azure service.</span></span>

## <span data-ttu-id="61f20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61f20-104">SYNTAX</span></span>

### <span data-ttu-id="61f20-105">ServiceAndSlot (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61f20-105">ServiceAndSlot (Default)</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="61f20-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="61f20-106">SubnetNameOnly</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="61f20-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="61f20-107">SubnetNameAndIP</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="61f20-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61f20-108">DESCRIPTION</span></span>
<span data-ttu-id="61f20-109">Il cmdlet **Add-AzureInternalLoadBalancer** aggiunge una configurazione di bilanciamento del carico interna a un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="61f20-109">The **Add-AzureInternalLoadBalancer** cmdlet adds an internal load balancer configuration to an Azure service.</span></span>
<span data-ttu-id="61f20-110">Per una rete virtuale, è possibile specificare una subnet o l'indirizzo IP del sistema di bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="61f20-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="61f20-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61f20-111">EXAMPLES</span></span>

### <span data-ttu-id="61f20-112">Esempio 1: aggiungere un bilanciamento del carico interno</span><span class="sxs-lookup"><span data-stu-id="61f20-112">Example 1: Add an internal load balancer</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

<span data-ttu-id="61f20-113">Questo comando aggiunge un bilanciamento del carico interno denominato ContosoILB al servizio denominato ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="61f20-113">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>

### <span data-ttu-id="61f20-114">Esempio 2: aggiungere un bilanciamento del carico interno per una subnet specificata</span><span class="sxs-lookup"><span data-stu-id="61f20-114">Example 2: Add an internal load balancer for a specified subnet</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="61f20-115">Questo comando aggiunge un bilanciamento del carico interno denominato ContosoILB al servizio denominato ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="61f20-115">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="61f20-116">Il comando specifica la subnet denominata FrontEndSubnet.</span><span class="sxs-lookup"><span data-stu-id="61f20-116">The command specifies the subnet named FrontEndSubnet.</span></span>

### <span data-ttu-id="61f20-117">Esempio 3: aggiungere un bilanciamento del carico interno per una subnet e un indirizzo specificati</span><span class="sxs-lookup"><span data-stu-id="61f20-117">Example 3: Add an internal load balancer for a specified subnet and address</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

<span data-ttu-id="61f20-118">Questo comando aggiunge un bilanciamento del carico interno denominato ContosoILB al servizio denominato ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="61f20-118">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="61f20-119">Il comando specifica la subnet denominata FrontEndSubnet e l'indirizzo statico della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="61f20-119">The command specifies the subnet named FrontEndSubnet and the static address of the virtual network.</span></span>

## <span data-ttu-id="61f20-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61f20-120">PARAMETERS</span></span>

### <span data-ttu-id="61f20-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="61f20-121">-InformationAction</span></span>
<span data-ttu-id="61f20-122">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="61f20-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="61f20-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="61f20-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61f20-124">Continuare</span><span class="sxs-lookup"><span data-stu-id="61f20-124">Continue</span></span>
- <span data-ttu-id="61f20-125">Ignora</span><span class="sxs-lookup"><span data-stu-id="61f20-125">Ignore</span></span>
- <span data-ttu-id="61f20-126">Informarsi</span><span class="sxs-lookup"><span data-stu-id="61f20-126">Inquire</span></span>
- <span data-ttu-id="61f20-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="61f20-127">SilentlyContinue</span></span>
- <span data-ttu-id="61f20-128">Stop</span><span class="sxs-lookup"><span data-stu-id="61f20-128">Stop</span></span>
- <span data-ttu-id="61f20-129">Sospensione</span><span class="sxs-lookup"><span data-stu-id="61f20-129">Suspend</span></span>

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

### <span data-ttu-id="61f20-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="61f20-130">-InformationVariable</span></span>
<span data-ttu-id="61f20-131">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="61f20-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="61f20-132">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="61f20-132">-InternalLoadBalancerName</span></span>
<span data-ttu-id="61f20-133">Specifica il nome del bilanciamento del carico interno aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61f20-133">Specifies the name of the internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="61f20-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="61f20-134">-Profile</span></span>
<span data-ttu-id="61f20-135">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61f20-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61f20-136">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="61f20-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="61f20-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="61f20-137">-ServiceName</span></span>
<span data-ttu-id="61f20-138">Specifica il nome del servizio a cui questo cmdlet aggiunge un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="61f20-138">Specifies the name of the service to which this cmdlet adds an internal load balancer.</span></span>

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

### <span data-ttu-id="61f20-139">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="61f20-139">-StaticVNetIPAddress</span></span>
<span data-ttu-id="61f20-140">Specifica l'indirizzo IP di rete virtuale per un sistema di bilanciamento del carico interno aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61f20-140">Specifies the virtual network IP address for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="61f20-141">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="61f20-141">-SubnetName</span></span>
<span data-ttu-id="61f20-142">Specifica il nome della subnet per un bilanciamento del carico interno aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61f20-142">Specifies the name of the subnet for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="61f20-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f20-143">CommonParameters</span></span>
<span data-ttu-id="61f20-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f20-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f20-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f20-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f20-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61f20-146">INPUTS</span></span>

## <span data-ttu-id="61f20-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61f20-147">OUTPUTS</span></span>

### <span data-ttu-id="61f20-148">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="61f20-148">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="61f20-149">Note</span><span class="sxs-lookup"><span data-stu-id="61f20-149">NOTES</span></span>

## <span data-ttu-id="61f20-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61f20-150">RELATED LINKS</span></span>

[<span data-ttu-id="61f20-151">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="61f20-151">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="61f20-152">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="61f20-152">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="61f20-153">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="61f20-153">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="61f20-154">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="61f20-154">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


