---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: bec6ded02853fbcfc08db38f0e627433d1d1ae10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515048"
---
# <span data-ttu-id="f6574-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f6574-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="f6574-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6574-102">SYNOPSIS</span></span>
<span data-ttu-id="f6574-103">Crea un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="f6574-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6574-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6574-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6574-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6574-105">DESCRIPTION</span></span>
<span data-ttu-id="f6574-106">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="f6574-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="f6574-107">Il cmdlet **New-AzureRmLocalNetworkGateway** crea l'oggetto che rappresenta il Gateway on-Prem in base al nome, al nome del gruppo di risorse, alla posizione e all'indirizzo IP del gateway, oltre al prefisso di indirizzo della rete locale che si collegherà ad Azure.</span><span class="sxs-lookup"><span data-stu-id="f6574-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="f6574-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6574-108">EXAMPLES</span></span>

### <span data-ttu-id="f6574-109">1: creare un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="f6574-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="f6574-110">Crea l'oggetto del gateway di rete locale con il nome "myLocalGW" nel gruppo di risorse "myRG" in location "West US" con l'indirizzo IP "23.99.221.164" e il prefisso di indirizzo "10.5.51.0/24" on-Prem.</span><span class="sxs-lookup"><span data-stu-id="f6574-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="f6574-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6574-111">PARAMETERS</span></span>

### <span data-ttu-id="f6574-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f6574-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="f6574-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6574-113">-AsJob</span></span>
<span data-ttu-id="f6574-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f6574-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6574-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="f6574-115">-Asn</span></span>
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

### <span data-ttu-id="f6574-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="f6574-116">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="f6574-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6574-117">-DefaultProfile</span></span>
<span data-ttu-id="f6574-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6574-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6574-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f6574-119">-Force</span></span>
<span data-ttu-id="f6574-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f6574-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f6574-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="f6574-121">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="f6574-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f6574-122">-Location</span></span>
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

### <span data-ttu-id="f6574-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6574-123">-Name</span></span>
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

### <span data-ttu-id="f6574-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="f6574-124">-PeerWeight</span></span>
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

### <span data-ttu-id="f6574-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6574-125">-ResourceGroupName</span></span>
<span data-ttu-id="f6574-126">Specifica il gruppo di risorse a cui appartiene il gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="f6574-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="f6574-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="f6574-127">-Tag</span></span>
<span data-ttu-id="f6574-128">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f6574-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f6574-129">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f6574-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f6574-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f6574-130">-Confirm</span></span>
<span data-ttu-id="f6574-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6574-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6574-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6574-132">-WhatIf</span></span>
<span data-ttu-id="f6574-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6574-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6574-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6574-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6574-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6574-135">CommonParameters</span></span>
<span data-ttu-id="f6574-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6574-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6574-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6574-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6574-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6574-138">INPUTS</span></span>

### <span data-ttu-id="f6574-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f6574-139">System.String</span></span>

### <span data-ttu-id="f6574-140">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f6574-140">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f6574-141">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="f6574-141">System.UInt32</span></span>

### <span data-ttu-id="f6574-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f6574-142">System.Int32</span></span>

### <span data-ttu-id="f6574-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f6574-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f6574-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6574-144">OUTPUTS</span></span>

### <span data-ttu-id="f6574-145">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f6574-145">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="f6574-146">Note</span><span class="sxs-lookup"><span data-stu-id="f6574-146">NOTES</span></span>

## <span data-ttu-id="f6574-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6574-147">RELATED LINKS</span></span>

[<span data-ttu-id="f6574-148">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f6574-148">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="f6574-149">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f6574-149">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="f6574-150">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f6574-150">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
