---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C01AFE1-65E7-4C5F-B3ED-8FCD9C4D20FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: a42ffe7ded2eb47638dd961ae79b10dd21cf08ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023872"
---
# <span data-ttu-id="48567-101">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="48567-101">New-AzureInternalLoadBalancerConfig</span></span>

## <span data-ttu-id="48567-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48567-102">SYNOPSIS</span></span>
<span data-ttu-id="48567-103">Crea una configurazione di bilanciamento del carico interna.</span><span class="sxs-lookup"><span data-stu-id="48567-103">Creates an internal load balancer configuration.</span></span>

## <span data-ttu-id="48567-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48567-104">SYNTAX</span></span>

### <span data-ttu-id="48567-105">ServiceAndSlot (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48567-105">ServiceAndSlot (Default)</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="48567-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="48567-106">SubnetNameOnly</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="48567-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="48567-107">SubnetNameAndIP</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="48567-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48567-108">DESCRIPTION</span></span>
<span data-ttu-id="48567-109">Il cmdlet **New-AzureInternalLoadBalancerConfig** crea un oggetto **InternalLoadBalancerConfig** .</span><span class="sxs-lookup"><span data-stu-id="48567-109">The **New-AzureInternalLoadBalancerConfig** cmdlet creates an **InternalLoadBalancerConfig** object.</span></span>
<span data-ttu-id="48567-110">È possibile usare una configurazione di bilanciamento del carico interna quando si crea una distribuzione di una macchina virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="48567-110">You can use an internal load balancer configuration when you create an Azure virtual machine deployment.</span></span>

## <span data-ttu-id="48567-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48567-111">EXAMPLES</span></span>

### <span data-ttu-id="48567-112">Esempio 1: creare una configurazione di bilanciamento del carico interna</span><span class="sxs-lookup"><span data-stu-id="48567-112">Example 1: Create an internal load balancer configuration</span></span>
```
PS C:\> $IlbConfig = New-AzureInternalLoadBalancerConfig -InternalLoadBalancerName "Contoso" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="48567-113">Questo comando crea una configurazione di bilanciamento del carico interna per la subnet denominata FrontEndSubnet.</span><span class="sxs-lookup"><span data-stu-id="48567-113">This command creates an internal load balancer configuration for the subnet named FrontEndSubnet.</span></span>
<span data-ttu-id="48567-114">Il comando Archivia la configurazione nella variabile $IlbConfig da usare per la distribuzione di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="48567-114">The command stores the configuration in the $IlbConfig variable for you to use for a virtual machine deployment.</span></span>

## <span data-ttu-id="48567-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48567-115">PARAMETERS</span></span>

### <span data-ttu-id="48567-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="48567-116">-InformationAction</span></span>
<span data-ttu-id="48567-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="48567-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="48567-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="48567-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48567-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="48567-119">Continue</span></span>
- <span data-ttu-id="48567-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="48567-120">Ignore</span></span>
- <span data-ttu-id="48567-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="48567-121">Inquire</span></span>
- <span data-ttu-id="48567-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="48567-122">SilentlyContinue</span></span>
- <span data-ttu-id="48567-123">Stop</span><span class="sxs-lookup"><span data-stu-id="48567-123">Stop</span></span>
- <span data-ttu-id="48567-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="48567-124">Suspend</span></span>

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

### <span data-ttu-id="48567-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="48567-125">-InformationVariable</span></span>
<span data-ttu-id="48567-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="48567-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="48567-127">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="48567-127">-InternalLoadBalancerName</span></span>
<span data-ttu-id="48567-128">Specifica il nome del bilanciamento del carico interno che questo cmdlet include nella configurazione.</span><span class="sxs-lookup"><span data-stu-id="48567-128">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="48567-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="48567-129">-Profile</span></span>
<span data-ttu-id="48567-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48567-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="48567-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="48567-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48567-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="48567-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="48567-133">Specifica l'indirizzo IP di rete virtuale per un sistema di bilanciamento del carico interno che questo cmdlet include nella configurazione.</span><span class="sxs-lookup"><span data-stu-id="48567-133">Specifies the virtual network IP address for an internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48567-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="48567-134">-SubnetName</span></span>
<span data-ttu-id="48567-135">Specifica il nome della subnet per un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="48567-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48567-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48567-136">CommonParameters</span></span>
<span data-ttu-id="48567-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48567-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48567-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48567-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48567-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48567-139">INPUTS</span></span>

## <span data-ttu-id="48567-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48567-140">OUTPUTS</span></span>

### <span data-ttu-id="48567-141">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="48567-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerConfig</span></span>

## <span data-ttu-id="48567-142">Note</span><span class="sxs-lookup"><span data-stu-id="48567-142">NOTES</span></span>

## <span data-ttu-id="48567-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48567-143">RELATED LINKS</span></span>

[<span data-ttu-id="48567-144">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="48567-144">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="48567-145">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="48567-145">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="48567-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="48567-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="48567-147">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="48567-147">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


