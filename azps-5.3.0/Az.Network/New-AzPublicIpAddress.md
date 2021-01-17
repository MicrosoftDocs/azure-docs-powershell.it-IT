---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 8c48c7ec1f651348309c012275287bd88dd42bcc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474501"
---
# <span data-ttu-id="102c5-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="102c5-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="102c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="102c5-102">SYNOPSIS</span></span>
<span data-ttu-id="102c5-103">Crea un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="102c5-103">Creates a public IP address.</span></span>

## <span data-ttu-id="102c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="102c5-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="102c5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="102c5-105">DESCRIPTION</span></span>
<span data-ttu-id="102c5-106">Il cmdlet **New-AzPublicIpAddress** crea un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="102c5-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="102c5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="102c5-107">EXAMPLES</span></span>

### <span data-ttu-id="102c5-108">Esempio 1: creare un nuovo indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="102c5-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="102c5-109">Questo comando crea una nuova risorsa indirizzo IP pubblico. Viene creato un record DNS per $dnsPrefix. $location. cloudapp.azure.com che punta all'indirizzo IP pubblico della risorsa.</span><span class="sxs-lookup"><span data-stu-id="102c5-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="102c5-110">Un indirizzo IP pubblico viene immediatamente allocato a questa risorsa poiché il parametro-AllocationMethod viene specificato come "static".</span><span class="sxs-lookup"><span data-stu-id="102c5-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="102c5-111">Se è specificato come "dinamico", viene allocato un indirizzo IP pubblico solo quando si avvia (o crea) la risorsa associata, ad esempio una VM o un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="102c5-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="102c5-112">Esempio 2: creare un indirizzo IP pubblico con un nome di dominio completo inverso</span><span class="sxs-lookup"><span data-stu-id="102c5-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="102c5-113">Questo comando crea una nuova risorsa indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="102c5-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="102c5-114">Con il parametro-ReverseFqdn, Azure crea un record PTR DNS (ricerca inversa) per l'indirizzo IP pubblico assegnato alla risorsa, puntando alla $customFqdn specificata nel comando.</span><span class="sxs-lookup"><span data-stu-id="102c5-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="102c5-115">Come requisito preliminare, la $customFqdn (ad esempio webapp.contoso.com) dovrebbe avere un record CNAME DNS (Ricerca avanzata) che punta a $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="102c5-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="102c5-116">Esempio 3: creare un nuovo indirizzo IP pubblico con IpTag</span><span class="sxs-lookup"><span data-stu-id="102c5-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="102c5-117">Questo comando crea una nuova risorsa indirizzo IP pubblico. Viene creato un record DNS per $dnsPrefix. $location. cloudapp.azure.com che punta all'indirizzo IP pubblico della risorsa.</span><span class="sxs-lookup"><span data-stu-id="102c5-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="102c5-118">Un indirizzo IP pubblico viene immediatamente allocato a questa risorsa poiché il parametro-AllocationMethod viene specificato come "static".</span><span class="sxs-lookup"><span data-stu-id="102c5-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="102c5-119">Se è specificato come "dinamico", viene allocato un indirizzo IP pubblico solo quando si avvia (o crea) la risorsa associata, ad esempio una VM o un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="102c5-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="102c5-120">Un Iptag viene usato per specifici i tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="102c5-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="102c5-121">Iptag può essere specificato usando New-AzPublicIpTag e passato come input through-IpTags.</span><span class="sxs-lookup"><span data-stu-id="102c5-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="102c5-122">Esempio 4: creare un nuovo indirizzo IP pubblico da un prefisso</span><span class="sxs-lookup"><span data-stu-id="102c5-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="102c5-123">Questo comando crea una nuova risorsa indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="102c5-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="102c5-124">Viene creato un record DNS per $dnsPrefix. $location. cloudapp.azure.com che punta all'indirizzo IP pubblico della risorsa.</span><span class="sxs-lookup"><span data-stu-id="102c5-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="102c5-125">Un indirizzo IP pubblico viene immediatamente allocato alla risorsa dalla publicIpPrefix specificata.</span><span class="sxs-lookup"><span data-stu-id="102c5-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="102c5-126">Questa opzione è supportata solo per le AllocationMethod ' standard ' SKU è static '.</span><span class="sxs-lookup"><span data-stu-id="102c5-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="102c5-127">Esempio 5: creare un nuovo indirizzo IP pubblico globale</span><span class="sxs-lookup"><span data-stu-id="102c5-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="102c5-128">Questo comando crea una nuova risorsa indirizzo IP pubblico globale. Viene creato un record DNS per $dnsPrefix. $location. cloudapp.azure.com che punta all'indirizzo IP pubblico della risorsa.</span><span class="sxs-lookup"><span data-stu-id="102c5-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="102c5-129">Un indirizzo IP pubblico globale viene immediatamente assegnato alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="102c5-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="102c5-130">Questa opzione è supportata solo per le AllocationMethod ' standard ' SKU è static '.</span><span class="sxs-lookup"><span data-stu-id="102c5-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="102c5-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="102c5-131">PARAMETERS</span></span>

### <span data-ttu-id="102c5-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="102c5-132">-AllocationMethod</span></span>
<span data-ttu-id="102c5-133">Specifica il metodo con cui allocare l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="102c5-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="102c5-134">I valori accettabili per questo parametro sono: statici o dinamici.</span><span class="sxs-lookup"><span data-stu-id="102c5-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="102c5-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="102c5-135">-AsJob</span></span>
<span data-ttu-id="102c5-136">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="102c5-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="102c5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="102c5-137">-DefaultProfile</span></span>
<span data-ttu-id="102c5-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="102c5-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="102c5-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="102c5-139">-DomainNameLabel</span></span>
<span data-ttu-id="102c5-140">Specifica il nome DNS relativo per un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="102c5-140">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="102c5-141">-Force</span><span class="sxs-lookup"><span data-stu-id="102c5-141">-Force</span></span>
<span data-ttu-id="102c5-142">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="102c5-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="102c5-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="102c5-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="102c5-144">Specifica il timeout inattivo, in minuti.</span><span class="sxs-lookup"><span data-stu-id="102c5-144">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="102c5-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="102c5-145">-IpAddressVersion</span></span>
<span data-ttu-id="102c5-146">Specifica la versione dell'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="102c5-146">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="102c5-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="102c5-147">-IpTag</span></span>
<span data-ttu-id="102c5-148">Elenco IpTag.</span><span class="sxs-lookup"><span data-stu-id="102c5-148">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="102c5-149">-Posizione</span><span class="sxs-lookup"><span data-stu-id="102c5-149">-Location</span></span>
<span data-ttu-id="102c5-150">Specifica l'area geografica in cui creare un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="102c5-150">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="102c5-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="102c5-151">-Name</span></span>
<span data-ttu-id="102c5-152">Specifica il nome dell'indirizzo IP pubblico creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="102c5-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="102c5-153">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="102c5-153">-PublicIpPrefix</span></span>
<span data-ttu-id="102c5-154">Specifica il PSPublicIpPrefix da cui allocare l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="102c5-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="102c5-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="102c5-155">-ResourceGroupName</span></span>
<span data-ttu-id="102c5-156">Specifica il nome del gruppo di risorse in cui creare un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="102c5-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="102c5-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="102c5-157">-ReverseFqdn</span></span>
<span data-ttu-id="102c5-158">Specifica un nome di dominio completo inverso (FQDN).</span><span class="sxs-lookup"><span data-stu-id="102c5-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="102c5-159">-SKU</span><span class="sxs-lookup"><span data-stu-id="102c5-159">-Sku</span></span>
<span data-ttu-id="102c5-160">Nome del SKU IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="102c5-160">The public IP Sku name.</span></span>

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

### <span data-ttu-id="102c5-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="102c5-161">-Tag</span></span>
<span data-ttu-id="102c5-162">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="102c5-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="102c5-163">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="102c5-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="102c5-164">-Tier</span><span class="sxs-lookup"><span data-stu-id="102c5-164">-Tier</span></span>
<span data-ttu-id="102c5-165">Livello SKU pubblico IP.</span><span class="sxs-lookup"><span data-stu-id="102c5-165">The public IP Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="102c5-166">-Zona</span><span class="sxs-lookup"><span data-stu-id="102c5-166">-Zone</span></span>
<span data-ttu-id="102c5-167">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="102c5-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="102c5-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="102c5-168">-Confirm</span></span>
<span data-ttu-id="102c5-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="102c5-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="102c5-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="102c5-170">-WhatIf</span></span>
<span data-ttu-id="102c5-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="102c5-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="102c5-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="102c5-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="102c5-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="102c5-173">CommonParameters</span></span>
<span data-ttu-id="102c5-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="102c5-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="102c5-175">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="102c5-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="102c5-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="102c5-176">INPUTS</span></span>

### <span data-ttu-id="102c5-177">System. String</span><span class="sxs-lookup"><span data-stu-id="102c5-177">System.String</span></span>

### <span data-ttu-id="102c5-178">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag []</span><span class="sxs-lookup"><span data-stu-id="102c5-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="102c5-179">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="102c5-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="102c5-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="102c5-180">System.Int32</span></span>

### <span data-ttu-id="102c5-181">System. String []</span><span class="sxs-lookup"><span data-stu-id="102c5-181">System.String[]</span></span>

### <span data-ttu-id="102c5-182">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="102c5-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="102c5-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="102c5-183">OUTPUTS</span></span>

### <span data-ttu-id="102c5-184">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="102c5-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="102c5-185">Note</span><span class="sxs-lookup"><span data-stu-id="102c5-185">NOTES</span></span>

## <span data-ttu-id="102c5-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="102c5-186">RELATED LINKS</span></span>

[<span data-ttu-id="102c5-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="102c5-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="102c5-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="102c5-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="102c5-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="102c5-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
