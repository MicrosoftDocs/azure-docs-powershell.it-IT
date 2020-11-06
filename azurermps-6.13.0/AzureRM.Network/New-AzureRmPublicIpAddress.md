---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 7ef0d3ce20868c4240abc43278cdc38a33efa5b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521820"
---
# <span data-ttu-id="ca3e2-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca3e2-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="ca3e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca3e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ca3e2-103">Crea un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca3e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca3e2-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-PublicIpPrefix <Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix>]
 [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca3e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca3e2-105">DESCRIPTION</span></span>
<span data-ttu-id="ca3e2-106">Il cmdlet **New-AzureRmPublicIpAddress** crea un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="ca3e2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca3e2-107">EXAMPLES</span></span>

### <span data-ttu-id="ca3e2-108">1: creare un nuovo indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="ca3e2-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="ca3e2-109">Questo comando crea una nuova risorsa indirizzo IP pubblico. Viene creato un record DNS per $dnsPrefix. $location. cloudapp.azure.com che punta all'indirizzo IP pubblico della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="ca3e2-110">Un indirizzo IP pubblico viene immediatamente allocato a questa risorsa poiché il parametro-AllocationMethod viene specificato come "static".</span><span class="sxs-lookup"><span data-stu-id="ca3e2-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="ca3e2-111">Se è specificato come "dinamico", viene allocato un indirizzo IP pubblico solo quando si avvia (o crea) la risorsa associata, ad esempio una VM o un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="ca3e2-112">2: creare un indirizzo IP pubblico con un nome di dominio completo inverso</span><span class="sxs-lookup"><span data-stu-id="ca3e2-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="ca3e2-113">Questo comando crea una nuova risorsa indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="ca3e2-114">Con il parametro-ReverseFqdn, Azure crea un record PTR DNS (ricerca inversa) per l'indirizzo IP pubblico assegnato alla risorsa, puntando alla $customFqdn specificata nel comando.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="ca3e2-115">Come requisito preliminare, la $customFqdn (ad esempio webapp.contoso.com) dovrebbe avere un record CNAME DNS (Ricerca avanzata) che punta a $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="ca3e2-116">3: creare un nuovo indirizzo IP pubblico con IpTag</span><span class="sxs-lookup"><span data-stu-id="ca3e2-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="ca3e2-117">Questo comando crea una nuova risorsa indirizzo IP pubblico. Viene creato un record DNS per $dnsPrefix. $location. cloudapp.azure.com che punta all'indirizzo IP pubblico della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="ca3e2-118">Un indirizzo IP pubblico viene immediatamente allocato a questa risorsa poiché il parametro-AllocationMethod viene specificato come "static".</span><span class="sxs-lookup"><span data-stu-id="ca3e2-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="ca3e2-119">Se è specificato come "dinamico", viene allocato un indirizzo IP pubblico solo quando si avvia (o crea) la risorsa associata, ad esempio una VM o un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="ca3e2-120">Un Iptag viene usato per specifici i tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="ca3e2-121">Iptag può essere specificato usando New-AzureRmPublicIpTag e passato come input through-IpTags.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="ca3e2-122">4: creare un nuovo indirizzo IP pubblico da un prefisso</span><span class="sxs-lookup"><span data-stu-id="ca3e2-122">4: Create a new public IP address from a Prefix</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="ca3e2-123">Questo comando crea una nuova risorsa indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="ca3e2-124">Viene creato un record DNS per $dnsPrefix. $location. cloudapp.azure.com che punta all'indirizzo IP pubblico della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="ca3e2-125">Un indirizzo IP pubblico viene immediatamente allocato alla risorsa dalla publicIpPrefix specificata.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="ca3e2-126">Questa opzione è supportata solo per le AllocationMethod ' standard ' SKU è static '.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="ca3e2-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca3e2-127">PARAMETERS</span></span>

### <span data-ttu-id="ca3e2-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="ca3e2-128">-AllocationMethod</span></span>
<span data-ttu-id="ca3e2-129">Specifica il metodo con cui allocare l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="ca3e2-130">I valori accettabili per questo parametro sono: statici o dinamici.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3e2-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca3e2-131">-AsJob</span></span>
<span data-ttu-id="ca3e2-132">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ca3e2-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca3e2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca3e2-133">-DefaultProfile</span></span>
<span data-ttu-id="ca3e2-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca3e2-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="ca3e2-135">-DomainNameLabel</span></span>
<span data-ttu-id="ca3e2-136">Specifica il nome DNS relativo per un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-136">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="ca3e2-137">-Force</span><span class="sxs-lookup"><span data-stu-id="ca3e2-137">-Force</span></span>
<span data-ttu-id="ca3e2-138">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca3e2-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ca3e2-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ca3e2-140">Specifica il timeout inattivo, in minuti.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-140">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="ca3e2-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="ca3e2-141">-IpAddressVersion</span></span>
<span data-ttu-id="ca3e2-142">Specifica la versione dell'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-142">Specifies the version of the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3e2-143">-IpTag</span><span class="sxs-lookup"><span data-stu-id="ca3e2-143">-IpTag</span></span>
<span data-ttu-id="ca3e2-144">Elenco IpTag.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-144">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3e2-145">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ca3e2-145">-Location</span></span>
<span data-ttu-id="ca3e2-146">Specifica l'area geografica in cui creare un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-146">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="ca3e2-147">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ca3e2-147">-PublicIpPrefix</span></span>
<span data-ttu-id="ca3e2-148">Specifica il PSPublicIpPrefix da cui allocare l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-148">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3e2-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca3e2-149">-Name</span></span>
<span data-ttu-id="ca3e2-150">Specifica il nome dell'indirizzo IP pubblico creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-150">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3e2-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca3e2-151">-ResourceGroupName</span></span>
<span data-ttu-id="ca3e2-152">Specifica il nome del gruppo di risorse in cui creare un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="ca3e2-153">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="ca3e2-153">-ReverseFqdn</span></span>
<span data-ttu-id="ca3e2-154">Specifica un nome di dominio completo inverso (FQDN).</span><span class="sxs-lookup"><span data-stu-id="ca3e2-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="ca3e2-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="ca3e2-155">-Sku</span></span>
<span data-ttu-id="ca3e2-156">Nome del SKU IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-156">The public IP Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3e2-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca3e2-157">-Tag</span></span>
<span data-ttu-id="ca3e2-158">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ca3e2-159">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ca3e2-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ca3e2-160">-Zona</span><span class="sxs-lookup"><span data-stu-id="ca3e2-160">-Zone</span></span>
<span data-ttu-id="ca3e2-161">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="ca3e2-162">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca3e2-162">-Confirm</span></span>
<span data-ttu-id="ca3e2-163">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca3e2-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca3e2-164">-WhatIf</span></span>
<span data-ttu-id="ca3e2-165">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca3e2-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca3e2-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca3e2-167">CommonParameters</span></span>
<span data-ttu-id="ca3e2-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca3e2-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca3e2-169">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca3e2-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca3e2-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca3e2-170">INPUTS</span></span>

### <span data-ttu-id="ca3e2-171">System. String</span><span class="sxs-lookup"><span data-stu-id="ca3e2-171">System.String</span></span>

### <span data-ttu-id="ca3e2-172">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSPublicIpTag, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ca3e2-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ca3e2-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ca3e2-173">System.Int32</span></span>

### <span data-ttu-id="ca3e2-174">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ca3e2-174">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ca3e2-175">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca3e2-175">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ca3e2-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca3e2-176">OUTPUTS</span></span>

### <span data-ttu-id="ca3e2-177">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca3e2-177">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="ca3e2-178">Note</span><span class="sxs-lookup"><span data-stu-id="ca3e2-178">NOTES</span></span>

## <span data-ttu-id="ca3e2-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca3e2-179">RELATED LINKS</span></span>

[<span data-ttu-id="ca3e2-180">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca3e2-180">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="ca3e2-181">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca3e2-181">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="ca3e2-182">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca3e2-182">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
