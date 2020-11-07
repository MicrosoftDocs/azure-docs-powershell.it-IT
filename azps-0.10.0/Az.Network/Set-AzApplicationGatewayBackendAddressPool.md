---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: fd9d9c1b7956c16ab981b5426e9453de4d730dd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862861"
---
# <span data-ttu-id="15a35-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="15a35-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="15a35-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15a35-102">SYNOPSIS</span></span>
<span data-ttu-id="15a35-103">Aggiorna un pool di indirizzi back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="15a35-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="15a35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15a35-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a35-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15a35-105">DESCRIPTION</span></span>
<span data-ttu-id="15a35-106">Il cmdlet **set-AzApplicationGatewayBackendAddressPool** aggiorna un pool di indirizzi back-end per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="15a35-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="15a35-107">Gli indirizzi di back-end possono essere specificati come indirizzi IP, nomi di dominio completi (FQDN) o ID configurazioni IP.</span><span class="sxs-lookup"><span data-stu-id="15a35-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="15a35-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15a35-108">EXAMPLES</span></span>

### <span data-ttu-id="15a35-109">Esempio 1: impostazione di un pool di indirizzi back-end tramite FQDN</span><span class="sxs-lookup"><span data-stu-id="15a35-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="15a35-110">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="15a35-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="15a35-111">Il secondo comando Aggiorna il pool di indirizzi back-end del gateway dell'applicazione in $AppGw usando FQDN.</span><span class="sxs-lookup"><span data-stu-id="15a35-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="15a35-112">Esempio 2: impostazione di un pool di indirizzi back-end tramite indirizzi IP del server di backend</span><span class="sxs-lookup"><span data-stu-id="15a35-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="15a35-113">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="15a35-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="15a35-114">Il secondo comando Aggiorna il pool di indirizzi back-end del gateway dell'applicazione in $AppGw usando gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="15a35-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="15a35-115">Esempio 3: impostazione di un pool di indirizzi back-end utilizzando l'ID dell'indirizzo IP del server di backend</span><span class="sxs-lookup"><span data-stu-id="15a35-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\> $Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="15a35-116">Il primo comando ottiene un oggetto interfaccia di rete denominato Nic01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $Nic 01.</span><span class="sxs-lookup"><span data-stu-id="15a35-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="15a35-117">Il secondo comando ottiene un oggetto interfaccia di rete denominato Nic02 che appartiene al gruppo di risorse denominato ResourceGroup02 e lo archivia nella variabile $Nic 02.</span><span class="sxs-lookup"><span data-stu-id="15a35-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="15a35-118">Il terzo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="15a35-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="15a35-119">Il comando Forth usa gli ID di configurazione IP back-end da $Nic 01 e $Nic 02 per aggiornare il pool di indirizzi back-end del gateway dell'applicazione in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="15a35-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="15a35-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15a35-120">PARAMETERS</span></span>

### <span data-ttu-id="15a35-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15a35-121">-ApplicationGateway</span></span>
<span data-ttu-id="15a35-122">Specifica il gateway dell'applicazione con cui questo cmdlet associa il pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="15a35-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15a35-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="15a35-123">-BackendFqdns</span></span>
<span data-ttu-id="15a35-124">Specifica un elenco di indirizzi IP di back-end da usare come pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="15a35-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="15a35-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="15a35-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="15a35-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a35-126">-DefaultProfile</span></span>
<span data-ttu-id="15a35-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15a35-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15a35-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="15a35-128">-Name</span></span>
<span data-ttu-id="15a35-129">Specifica il nome del pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="15a35-129">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="15a35-130">Questo pool di indirizzi back-end deve esistere nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="15a35-130">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="15a35-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15a35-131">-Confirm</span></span>
<span data-ttu-id="15a35-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15a35-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a35-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a35-133">-WhatIf</span></span>
<span data-ttu-id="15a35-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15a35-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a35-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15a35-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a35-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a35-136">CommonParameters</span></span>
<span data-ttu-id="15a35-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a35-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a35-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a35-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a35-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15a35-139">INPUTS</span></span>

### <span data-ttu-id="15a35-140">System. String</span><span class="sxs-lookup"><span data-stu-id="15a35-140">System.String</span></span>

## <span data-ttu-id="15a35-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15a35-141">OUTPUTS</span></span>

### <span data-ttu-id="15a35-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15a35-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="15a35-143">Note</span><span class="sxs-lookup"><span data-stu-id="15a35-143">NOTES</span></span>

## <span data-ttu-id="15a35-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15a35-144">RELATED LINKS</span></span>

[<span data-ttu-id="15a35-145">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="15a35-145">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="15a35-146">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="15a35-146">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="15a35-147">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="15a35-147">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="15a35-148">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="15a35-148">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


