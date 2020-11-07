---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: dd5a0a14a0c2146ce6187a3ae08fda1bc3e60702
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688607"
---
# <span data-ttu-id="9f4b6-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9f4b6-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="9f4b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f4b6-102">SYNOPSIS</span></span>
<span data-ttu-id="9f4b6-103">Aggiorna un pool di indirizzi back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f4b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f4b6-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f4b6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f4b6-105">DESCRIPTION</span></span>
<span data-ttu-id="9f4b6-106">Il cmdlet **set-AzureRmApplicationGatewayBackendAddressPool** aggiorna un pool di indirizzi back-end per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="9f4b6-107">Gli indirizzi di back-end possono essere specificati come indirizzi IP, nomi di dominio completi (FQDN) o ID configurazioni IP.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="9f4b6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f4b6-108">EXAMPLES</span></span>

### <span data-ttu-id="9f4b6-109">Esempio 1: impostazione di un pool di indirizzi back-end tramite FQDN</span><span class="sxs-lookup"><span data-stu-id="9f4b6-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="9f4b6-110">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9f4b6-111">Il secondo comando Aggiorna il pool di indirizzi back-end del gateway dell'applicazione in $AppGw usando FQDN.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="9f4b6-112">Esempio 2: impostazione di un pool di indirizzi back-end tramite indirizzi IP del server di backend</span><span class="sxs-lookup"><span data-stu-id="9f4b6-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="9f4b6-113">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9f4b6-114">Il secondo comando Aggiorna il pool di indirizzi back-end del gateway dell'applicazione in $AppGw usando gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="9f4b6-115">Esempio 3: impostazione di un pool di indirizzi back-end utilizzando l'ID dell'indirizzo IP del server di backend</span><span class="sxs-lookup"><span data-stu-id="9f4b6-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="9f4b6-116">Il primo comando ottiene un oggetto interfaccia di rete denominato Nic01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $Nic 01.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="9f4b6-117">Il secondo comando ottiene un oggetto interfaccia di rete denominato Nic02 che appartiene al gruppo di risorse denominato ResourceGroup02 e lo archivia nella variabile $Nic 02.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="9f4b6-118">Il terzo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9f4b6-119">Il comando Forth usa gli ID di configurazione IP back-end da $Nic 01 e $Nic 02 per aggiornare il pool di indirizzi back-end del gateway dell'applicazione in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="9f4b6-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f4b6-120">PARAMETERS</span></span>

### <span data-ttu-id="9f4b6-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f4b6-121">-ApplicationGateway</span></span>
<span data-ttu-id="9f4b6-122">Specifica il gateway dell'applicazione con cui questo cmdlet associa il pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f4b6-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="9f4b6-123">-BackendFqdns</span></span>
<span data-ttu-id="9f4b6-124">Specifica un elenco di indirizzi IP di back-end da usare come pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f4b6-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="9f4b6-125">-BackendIPAddresses</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f4b6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f4b6-126">-Name</span></span>
<span data-ttu-id="9f4b6-127">Specifica il nome del pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-127">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="9f4b6-128">Questo pool di indirizzi back-end deve esistere nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-128">This back-end address pool must exist in the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f4b6-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9f4b6-129">-Confirm</span></span>
<span data-ttu-id="9f4b6-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f4b6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f4b6-131">-WhatIf</span></span>
<span data-ttu-id="9f4b6-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f4b6-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f4b6-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f4b6-134">-DefaultProfile</span></span>
<span data-ttu-id="9f4b6-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f4b6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f4b6-136">CommonParameters</span></span>
<span data-ttu-id="9f4b6-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f4b6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f4b6-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f4b6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f4b6-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f4b6-139">INPUTS</span></span>

### <span data-ttu-id="9f4b6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9f4b6-140">System.String</span></span>

## <span data-ttu-id="9f4b6-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f4b6-141">OUTPUTS</span></span>

### <span data-ttu-id="9f4b6-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f4b6-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f4b6-143">Note</span><span class="sxs-lookup"><span data-stu-id="9f4b6-143">NOTES</span></span>

## <span data-ttu-id="9f4b6-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f4b6-144">RELATED LINKS</span></span>

[<span data-ttu-id="9f4b6-145">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9f4b6-145">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9f4b6-146">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9f4b6-146">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9f4b6-147">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9f4b6-147">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="9f4b6-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9f4b6-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


