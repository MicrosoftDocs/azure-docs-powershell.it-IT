---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: 032090bb494718a6420f54960106fe9c5fa9871c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866470"
---
# <span data-ttu-id="7b01d-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b01d-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="7b01d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b01d-102">SYNOPSIS</span></span>
<span data-ttu-id="7b01d-103">Crea un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7b01d-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b01d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b01d-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b01d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b01d-105">DESCRIPTION</span></span>
<span data-ttu-id="7b01d-106">Il cmdlet **New-AzureRmPublicIpAddress** crea un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7b01d-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="7b01d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b01d-107">EXAMPLES</span></span>

### <span data-ttu-id="7b01d-108">1: creare un nuovo indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="7b01d-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="7b01d-109">Questo comando crea una nuova risorsa indirizzo IP pubblico. Viene creato un record DNS per $dnsPrefix. $location. cloudapp.azure.com che punta all'indirizzo IP pubblico della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7b01d-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="7b01d-110">Un indirizzo IP pubblico viene immediatamente allocato a questa risorsa poiché il parametro-AllocationMethod viene specificato come "static".</span><span class="sxs-lookup"><span data-stu-id="7b01d-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="7b01d-111">Se è specificato come "dinamico", viene allocato un indirizzo IP pubblico solo quando si avvia (o crea) la risorsa associata, ad esempio una VM o un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="7b01d-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="7b01d-112">2: creare un indirizzo IP pubblico con un nome di dominio completo inverso</span><span class="sxs-lookup"><span data-stu-id="7b01d-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="7b01d-113">Questo comando crea una nuova risorsa indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7b01d-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="7b01d-114">Con il parametro-ReverseFqdn, Azure crea un record PTR DNS (ricerca inversa) per l'indirizzo IP pubblico assegnato alla risorsa, puntando alla $customFqdn specificata nel comando.</span><span class="sxs-lookup"><span data-stu-id="7b01d-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="7b01d-115">Come requisito preliminare, la $customFqdn (ad esempio webapp.contoso.com) dovrebbe avere un record CNAME DNS (Ricerca avanzata) che punta a $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="7b01d-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="7b01d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b01d-116">PARAMETERS</span></span>

### <span data-ttu-id="7b01d-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="7b01d-117">-AllocationMethod</span></span>
<span data-ttu-id="7b01d-118">Specifica il metodo con cui allocare l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7b01d-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="7b01d-119">I valori accettabili per questo parametro sono: statici o dinamici.</span><span class="sxs-lookup"><span data-stu-id="7b01d-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b01d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b01d-120">-AsJob</span></span>
<span data-ttu-id="7b01d-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7b01d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b01d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b01d-122">-DefaultProfile</span></span>
<span data-ttu-id="7b01d-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b01d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b01d-124">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="7b01d-124">-DomainNameLabel</span></span>
<span data-ttu-id="7b01d-125">Specifica il nome DNS relativo per un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7b01d-125">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="7b01d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="7b01d-126">-Force</span></span>
<span data-ttu-id="7b01d-127">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7b01d-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7b01d-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7b01d-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7b01d-129">Specifica il timeout inattivo, in minuti.</span><span class="sxs-lookup"><span data-stu-id="7b01d-129">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="7b01d-130">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7b01d-130">-IpAddressVersion</span></span>
<span data-ttu-id="7b01d-131">Specifica la versione dell'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="7b01d-131">Specifies the version of the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b01d-132">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7b01d-132">-Location</span></span>
<span data-ttu-id="7b01d-133">Specifica l'area geografica in cui creare un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7b01d-133">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="7b01d-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b01d-134">-Name</span></span>
<span data-ttu-id="7b01d-135">Specifica il nome dell'indirizzo IP pubblico creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b01d-135">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b01d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b01d-136">-ResourceGroupName</span></span>
<span data-ttu-id="7b01d-137">Specifica il nome del gruppo di risorse in cui creare un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7b01d-137">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="7b01d-138">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="7b01d-138">-ReverseFqdn</span></span>
<span data-ttu-id="7b01d-139">Specifica un nome di dominio completo inverso (FQDN).</span><span class="sxs-lookup"><span data-stu-id="7b01d-139">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="7b01d-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="7b01d-140">-Sku</span></span>
<span data-ttu-id="7b01d-141">Nome del SKU IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="7b01d-141">The public IP Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b01d-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b01d-142">-Tag</span></span>
<span data-ttu-id="7b01d-143">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7b01d-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7b01d-144">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="7b01d-144">For example:</span></span>

<span data-ttu-id="7b01d-145">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7b01d-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7b01d-146">-Zona</span><span class="sxs-lookup"><span data-stu-id="7b01d-146">-Zone</span></span>
<span data-ttu-id="7b01d-147">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="7b01d-147">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="7b01d-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b01d-148">-Confirm</span></span>
<span data-ttu-id="7b01d-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b01d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b01d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b01d-150">-WhatIf</span></span>
<span data-ttu-id="7b01d-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b01d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b01d-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b01d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b01d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b01d-153">CommonParameters</span></span>
<span data-ttu-id="7b01d-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b01d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b01d-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b01d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b01d-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b01d-156">INPUTS</span></span>

## <span data-ttu-id="7b01d-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b01d-157">OUTPUTS</span></span>

### <span data-ttu-id="7b01d-158">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b01d-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7b01d-159">Note</span><span class="sxs-lookup"><span data-stu-id="7b01d-159">NOTES</span></span>

## <span data-ttu-id="7b01d-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b01d-160">RELATED LINKS</span></span>

[<span data-ttu-id="7b01d-161">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b01d-161">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="7b01d-162">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b01d-162">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="7b01d-163">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b01d-163">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
