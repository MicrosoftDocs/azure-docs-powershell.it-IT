---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 37255dfda50d7c055aad6941bbf417d1aa852d35
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860477"
---
# <span data-ttu-id="380d5-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="380d5-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="380d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="380d5-102">SYNOPSIS</span></span>
<span data-ttu-id="380d5-103">Crea un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="380d5-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="380d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="380d5-104">SYNTAX</span></span>

```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="380d5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="380d5-105">DESCRIPTION</span></span>
<span data-ttu-id="380d5-106">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="380d5-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="380d5-107">Il cmdlet **New-AzLocalNetworkGateway** crea l'oggetto che rappresenta il Gateway on-Prem in base al nome, al nome del gruppo di risorse, alla posizione e all'indirizzo IP del gateway, oltre al prefisso di indirizzo della rete locale che si collegherà ad Azure.</span><span class="sxs-lookup"><span data-stu-id="380d5-107">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="380d5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="380d5-108">EXAMPLES</span></span>

### <span data-ttu-id="380d5-109">1: creare un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="380d5-109">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="380d5-110">Crea l'oggetto del gateway di rete locale con il nome "myLocalGW" nel gruppo di risorse "myRG" in location "West US" con l'indirizzo IP "23.99.221.164" e il prefisso di indirizzo "10.5.51.0/24" on-Prem.</span><span class="sxs-lookup"><span data-stu-id="380d5-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="380d5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="380d5-111">PARAMETERS</span></span>

### <span data-ttu-id="380d5-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="380d5-112">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="380d5-113">-AsJob</span></span>
<span data-ttu-id="380d5-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="380d5-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="380d5-115">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="380d5-116">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380d5-117">-DefaultProfile</span></span>
<span data-ttu-id="380d5-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="380d5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="380d5-119">-Force</span></span>
<span data-ttu-id="380d5-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="380d5-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="380d5-121">-GatewayIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="380d5-122">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="380d5-123">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="380d5-124">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="380d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="380d5-126">Specifica il gruppo di risorse a cui appartiene il gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="380d5-126">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="380d5-127">-Tag</span></span>
<span data-ttu-id="380d5-128">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="380d5-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="380d5-129">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="380d5-129">For example:</span></span>

<span data-ttu-id="380d5-130">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="380d5-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="380d5-131">-Confirm</span></span>
<span data-ttu-id="380d5-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="380d5-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="380d5-133">-WhatIf</span></span>
<span data-ttu-id="380d5-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="380d5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="380d5-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="380d5-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380d5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380d5-136">CommonParameters</span></span>
<span data-ttu-id="380d5-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="380d5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380d5-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="380d5-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380d5-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="380d5-139">INPUTS</span></span>

## <span data-ttu-id="380d5-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="380d5-140">OUTPUTS</span></span>

### <span data-ttu-id="380d5-141">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="380d5-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="380d5-142">Note</span><span class="sxs-lookup"><span data-stu-id="380d5-142">NOTES</span></span>

## <span data-ttu-id="380d5-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="380d5-143">RELATED LINKS</span></span>

[<span data-ttu-id="380d5-144">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="380d5-144">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="380d5-145">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="380d5-145">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="380d5-146">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="380d5-146">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
