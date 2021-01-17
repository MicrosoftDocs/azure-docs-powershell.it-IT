---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476525"
---
# <span data-ttu-id="1ccd7-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ccd7-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="1ccd7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ccd7-102">SYNOPSIS</span></span>
<span data-ttu-id="1ccd7-103">Crea un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="1ccd7-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="1ccd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ccd7-104">SYNTAX</span></span>

### <span data-ttu-id="1ccd7-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="1ccd7-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ccd7-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="1ccd7-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ccd7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ccd7-107">DESCRIPTION</span></span>
<span data-ttu-id="1ccd7-108">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="1ccd7-109">Il cmdlet **New-AzLocalNetworkGateway** crea l'oggetto che rappresenta il Gateway on-Prem in base al nome, al nome del gruppo di risorse, alla posizione e all'indirizzo IP del gateway, oltre al prefisso di indirizzo della rete locale che si collegherà ad Azure.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="1ccd7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ccd7-110">EXAMPLES</span></span>

### <span data-ttu-id="1ccd7-111">Esempio 1: creare un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="1ccd7-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="1ccd7-112">Crea l'oggetto del gateway di rete locale con il nome "myLocalGW" nel gruppo di risorse "myRG" in location "West US" con l'indirizzo IP "23.99.221.164" e il prefisso di indirizzo "10.5.51.0/24" on-Prem.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="1ccd7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ccd7-113">PARAMETERS</span></span>

### <span data-ttu-id="1ccd7-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1ccd7-114">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ccd7-115">-AsJob</span></span>
<span data-ttu-id="1ccd7-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1ccd7-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="1ccd7-117">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="1ccd7-118">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ccd7-119">-DefaultProfile</span></span>
<span data-ttu-id="1ccd7-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1ccd7-121">-Force</span></span>
<span data-ttu-id="1ccd7-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-123">-FQDN</span><span class="sxs-lookup"><span data-stu-id="1ccd7-123">-Fqdn</span></span>
<span data-ttu-id="1ccd7-124">FQDN del gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="1ccd7-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1ccd7-126">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ccd7-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="1ccd7-128">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ccd7-129">-ResourceGroupName</span></span>
<span data-ttu-id="1ccd7-130">Specifica il gruppo di risorse a cui appartiene il gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-130">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ccd7-131">-Tag</span></span>
<span data-ttu-id="1ccd7-132">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1ccd7-133">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1ccd7-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ccd7-134">-Confirm</span></span>
<span data-ttu-id="1ccd7-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ccd7-136">-WhatIf</span></span>
<span data-ttu-id="1ccd7-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ccd7-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccd7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ccd7-139">CommonParameters</span></span>
<span data-ttu-id="1ccd7-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ccd7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ccd7-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ccd7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ccd7-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ccd7-142">INPUTS</span></span>

### <span data-ttu-id="1ccd7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1ccd7-143">System.String</span></span>

### <span data-ttu-id="1ccd7-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="1ccd7-144">System.String[]</span></span>

### <span data-ttu-id="1ccd7-145">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="1ccd7-145">System.UInt32</span></span>

### <span data-ttu-id="1ccd7-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1ccd7-146">System.Int32</span></span>

### <span data-ttu-id="1ccd7-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1ccd7-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1ccd7-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ccd7-148">OUTPUTS</span></span>

### <span data-ttu-id="1ccd7-149">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ccd7-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="1ccd7-150">Note</span><span class="sxs-lookup"><span data-stu-id="1ccd7-150">NOTES</span></span>

## <span data-ttu-id="1ccd7-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ccd7-151">RELATED LINKS</span></span>

[<span data-ttu-id="1ccd7-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ccd7-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="1ccd7-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ccd7-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="1ccd7-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1ccd7-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
