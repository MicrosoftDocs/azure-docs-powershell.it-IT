---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 6f22c8026d3b72a6c9cd52563252aa3d4bcad039
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866507"
---
# <span data-ttu-id="f0d76-101">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0d76-101">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f0d76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0d76-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d76-103">Aggiunge un pool di indirizzi back-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0d76-103">Adds a back-end address pool to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0d76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0d76-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0d76-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0d76-105">DESCRIPTION</span></span>
<span data-ttu-id="f0d76-106">Il cmdlet **Add-AzureRmApplicationGatewayBackendAddressPool** aggiunge un pool di indirizzi back-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0d76-106">The **Add-AzureRmApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="f0d76-107">Un indirizzo di back-end può essere specificato usando un indirizzo IP, un nome di dominio completo (FQDN) o un ID di configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="f0d76-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="f0d76-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0d76-108">EXAMPLES</span></span>

### <span data-ttu-id="f0d76-109">Esempio 1: aggiungere un pool di indirizzi back-end usando un nome di dominio completo del server back-end</span><span class="sxs-lookup"><span data-stu-id="f0d76-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="f0d76-110">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando aggiunge il pool di indirizzi back-end del gateway dell'applicazione archiviato in $AppGw tramite FQDN.</span><span class="sxs-lookup"><span data-stu-id="f0d76-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="f0d76-111">Esempio 2: aggiungere un pool di indirizzi back-end tramite indirizzi IP del server di backend</span><span class="sxs-lookup"><span data-stu-id="f0d76-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="f0d76-112">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando aggiunge il pool di indirizzi back-end del gateway dell'applicazione archiviato in $AppGw tramite indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="f0d76-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="f0d76-113">Esempio 3: pool di indirizzi back-end seta usando l'ID dell'indirizzo IP del server di backend</span><span class="sxs-lookup"><span data-stu-id="f0d76-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="f0d76-114">Il primo comando ottiene un oggetto interfaccia di rete denominato Nic01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $Nic 01. Il secondo comando ottiene un oggetto interfaccia di rete denominato Nic02 che appartiene al gruppo di risorse denominato ResourceGroup02 e lo archivia nella variabile $Nic 02. Il terzo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il comando Forth usa gli ID di configurazione IP back-end da $Nic 01 e $Nic 02 per aggiungere il pool di indirizzi back-end del gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f0d76-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f0d76-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0d76-115">PARAMETERS</span></span>

### <span data-ttu-id="f0d76-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0d76-116">-ApplicationGateway</span></span>
<span data-ttu-id="f0d76-117">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge un pool di indirizzi back-end.</span><span class="sxs-lookup"><span data-stu-id="f0d76-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="f0d76-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="f0d76-118">-BackendFqdns</span></span>
<span data-ttu-id="f0d76-119">Specifica un elenco di FQDN del backend che questo cmdlet aggiunge come pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="f0d76-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="f0d76-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="f0d76-120">-BackendIPAddresses</span></span>
<span data-ttu-id="f0d76-121">Specifica un elenco di indirizzi IP di back-end che questo cmdlet aggiunge come pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="f0d76-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="f0d76-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d76-122">-DefaultProfile</span></span>
<span data-ttu-id="f0d76-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d76-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d76-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0d76-124">-Name</span></span>
<span data-ttu-id="f0d76-125">Specifica il nome del pool di server back-end aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0d76-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f0d76-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0d76-126">-Confirm</span></span>
<span data-ttu-id="f0d76-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0d76-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0d76-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d76-128">-WhatIf</span></span>
<span data-ttu-id="f0d76-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0d76-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0d76-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0d76-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0d76-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d76-131">CommonParameters</span></span>
<span data-ttu-id="f0d76-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d76-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d76-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d76-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d76-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0d76-134">INPUTS</span></span>

###  
<span data-ttu-id="f0d76-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f0d76-135">System.String</span></span>

## <span data-ttu-id="f0d76-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0d76-136">OUTPUTS</span></span>

### <span data-ttu-id="f0d76-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0d76-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f0d76-138">Note</span><span class="sxs-lookup"><span data-stu-id="f0d76-138">NOTES</span></span>

## <span data-ttu-id="f0d76-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0d76-139">RELATED LINKS</span></span>

[<span data-ttu-id="f0d76-140">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0d76-140">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f0d76-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0d76-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f0d76-142">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0d76-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f0d76-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0d76-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f0d76-144">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0d76-144">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


