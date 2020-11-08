---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023758"
---
# <span data-ttu-id="37a0c-101">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="37a0c-101">Set-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="37a0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="37a0c-103">Aggiunge o modifica una regola di sicurezza di rete in un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="37a0c-103">Adds or modifies a network security rule in a network security group.</span></span>

## <span data-ttu-id="37a0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37a0c-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="37a0c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37a0c-105">DESCRIPTION</span></span>
<span data-ttu-id="37a0c-106">Il cmdlet **set-AzureNetworkSecurityRule** aggiunge o modifica una regola di sicurezza della rete Azure in un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="37a0c-106">The **Set-AzureNetworkSecurityRule** cmdlet adds or modifies an Azure network security rule in a network security group.</span></span>

## <span data-ttu-id="37a0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37a0c-107">EXAMPLES</span></span>

## <span data-ttu-id="37a0c-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37a0c-108">PARAMETERS</span></span>

### <span data-ttu-id="37a0c-109">-Azione</span><span class="sxs-lookup"><span data-stu-id="37a0c-109">-Action</span></span>
<span data-ttu-id="37a0c-110">Specifica l'azione per una regola di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="37a0c-110">Specifies the action for a network security rule.</span></span>
<span data-ttu-id="37a0c-111">I valori validi sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="37a0c-111">Valid values are: Allow and Deny.</span></span>

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

### <span data-ttu-id="37a0c-112">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="37a0c-112">-DestinationAddressPrefix</span></span>
<span data-ttu-id="37a0c-113">Specifica l'indirizzo CIDR (classe Interdomain Routing) dell'intervallo IP di destinazione per la regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="37a0c-113">Specifies the Classless Interdomain Routing (CIDR) address of the destination IP range for the network security rule.</span></span>
<span data-ttu-id="37a0c-114">Un asterisco (\*) specifica un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="37a0c-114">An asterisk (\*) specifies any IP address.</span></span>

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

### <span data-ttu-id="37a0c-115">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="37a0c-115">-DestinationPortRange</span></span>
<span data-ttu-id="37a0c-116">Specifica un intervallo di porte di destinazione per la regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="37a0c-116">Specifies a destination port range for the network security rule.</span></span>
<span data-ttu-id="37a0c-117">I valori validi sono costituiti da numeri interi compresi tra 0 e 65535.</span><span class="sxs-lookup"><span data-stu-id="37a0c-117">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="37a0c-118">Puoi specificare un singolo valore o specificare un intervallo nel formato LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="37a0c-118">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="37a0c-119">Un trattino separa i due valori.</span><span class="sxs-lookup"><span data-stu-id="37a0c-119">A hyphen separates the two values.</span></span>

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

### <span data-ttu-id="37a0c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="37a0c-120">-Name</span></span>
<span data-ttu-id="37a0c-121">Specifica il nome della regola di sicurezza della rete che questo cmdlet aggiunge o modifica.</span><span class="sxs-lookup"><span data-stu-id="37a0c-121">Specifies the name for the network security rule that this cmdlet adds or modifies.</span></span>

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

### <span data-ttu-id="37a0c-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="37a0c-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="37a0c-123">Specifica il gruppo di sicurezza di rete modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37a0c-123">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="37a0c-124">Per ottenere un oggetto **INetworkSecurityGroup** , usa il cmdlet Get-AzureNetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="37a0c-124">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37a0c-125">-Priorità</span><span class="sxs-lookup"><span data-stu-id="37a0c-125">-Priority</span></span>
<span data-ttu-id="37a0c-126">Specifica la priorità per la regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="37a0c-126">Specifies the priority for the network security rule.</span></span>
<span data-ttu-id="37a0c-127">I valori validi sono: numeri interi da 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="37a0c-127">Valid values are: integers from 100 to 4096.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37a0c-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="37a0c-128">-Profile</span></span>
<span data-ttu-id="37a0c-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37a0c-129">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="37a0c-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="37a0c-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37a0c-131">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="37a0c-131">-Protocol</span></span>
<span data-ttu-id="37a0c-132">Specifica il protocollo per la regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="37a0c-132">Specifies the protocol for the network security rule.</span></span>
<span data-ttu-id="37a0c-133">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="37a0c-133">Valid values are:</span></span> 

- <span data-ttu-id="37a0c-134">TCP</span><span class="sxs-lookup"><span data-stu-id="37a0c-134">TCP</span></span> 
- <span data-ttu-id="37a0c-135">UDP</span><span class="sxs-lookup"><span data-stu-id="37a0c-135">UDP</span></span> 
- *

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

### <span data-ttu-id="37a0c-136">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="37a0c-136">-SourceAddressPrefix</span></span>
<span data-ttu-id="37a0c-137">Specifica l'indirizzo CIDR dell'intervallo IP di origine per la regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="37a0c-137">Specifies the CIDR address of the source IP range for the network security rule.</span></span>
<span data-ttu-id="37a0c-138">Un asterisco (\*) specifica un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="37a0c-138">An asterisk (\*) specifies any IP address.</span></span>

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

### <span data-ttu-id="37a0c-139">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="37a0c-139">-SourcePortRange</span></span>
<span data-ttu-id="37a0c-140">Specifica un intervallo della porta di origine per la regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="37a0c-140">Specifies a source port range for the network security rule.</span></span>
<span data-ttu-id="37a0c-141">I valori validi sono costituiti da numeri interi compresi tra 0 e 65535.</span><span class="sxs-lookup"><span data-stu-id="37a0c-141">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="37a0c-142">Puoi specificare un singolo valore o specificare un intervallo nel formato LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="37a0c-142">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="37a0c-143">Un trattino separa i due valori.</span><span class="sxs-lookup"><span data-stu-id="37a0c-143">A hyphen separates the two values.</span></span>

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

### <span data-ttu-id="37a0c-144">-Digitare</span><span class="sxs-lookup"><span data-stu-id="37a0c-144">-Type</span></span>
<span data-ttu-id="37a0c-145">Specifica il tipo di connessione per la regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="37a0c-145">Specifies the type of connection for the network security rule.</span></span>
<span data-ttu-id="37a0c-146">I valori validi sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="37a0c-146">Valid values are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="37a0c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a0c-147">CommonParameters</span></span>
<span data-ttu-id="37a0c-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37a0c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a0c-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37a0c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a0c-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37a0c-150">INPUTS</span></span>

## <span data-ttu-id="37a0c-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37a0c-151">OUTPUTS</span></span>

## <span data-ttu-id="37a0c-152">Note</span><span class="sxs-lookup"><span data-stu-id="37a0c-152">NOTES</span></span>

## <span data-ttu-id="37a0c-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37a0c-153">RELATED LINKS</span></span>

[<span data-ttu-id="37a0c-154">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="37a0c-154">Remove-AzureNetworkSecurityRule</span></span>](./Remove-AzureNetworkSecurityRule.md)


