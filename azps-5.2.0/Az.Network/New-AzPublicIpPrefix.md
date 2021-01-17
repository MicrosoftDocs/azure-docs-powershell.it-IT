---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 231a4f9622aa9fecf0c6d832e5f7602da1bed1b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330631"
---
# <span data-ttu-id="a1cab-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a1cab-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="a1cab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1cab-102">SYNOPSIS</span></span>
<span data-ttu-id="a1cab-103">Crea un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="a1cab-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="a1cab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1cab-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1cab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1cab-105">DESCRIPTION</span></span>
<span data-ttu-id="a1cab-106">Il cmdlet **New-AzPublicIpPrefix** crea un prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="a1cab-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="a1cab-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1cab-107">EXAMPLES</span></span>

### <span data-ttu-id="a1cab-108">Esempio 1: creare un nuovo prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="a1cab-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="a1cab-109">Questo comando crea una nuova risorsa di prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="a1cab-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="a1cab-110">Esempio 2: creare un nuovo prefisso IP pubblico globale</span><span class="sxs-lookup"><span data-stu-id="a1cab-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="a1cab-111">Questo comando crea una nuova risorsa di prefisso IP pubblico globale.</span><span class="sxs-lookup"><span data-stu-id="a1cab-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="a1cab-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1cab-112">PARAMETERS</span></span>

### <span data-ttu-id="a1cab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1cab-113">-AsJob</span></span>
<span data-ttu-id="a1cab-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a1cab-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1cab-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a1cab-115">-CustomIpPrefix</span></span>
<span data-ttu-id="a1cab-116">CustomIpPrefix a cui verrà associato questo PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a1cab-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1cab-117">-DefaultProfile</span></span>
<span data-ttu-id="a1cab-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1cab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1cab-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a1cab-119">-Force</span></span>
<span data-ttu-id="a1cab-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="a1cab-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a1cab-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="a1cab-121">-IpAddressVersion</span></span>
<span data-ttu-id="a1cab-122">Versione dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="a1cab-122">The public IP address version.</span></span>

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

### <span data-ttu-id="a1cab-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="a1cab-123">-IpTag</span></span>
<span data-ttu-id="a1cab-124">Elenco IpTag.</span><span class="sxs-lookup"><span data-stu-id="a1cab-124">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cab-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a1cab-125">-Location</span></span>
<span data-ttu-id="a1cab-126">Posizione del prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="a1cab-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="a1cab-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1cab-127">-Name</span></span>
<span data-ttu-id="a1cab-128">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a1cab-128">The resource name.</span></span>

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

### <span data-ttu-id="a1cab-129">-LunghezzaPrefisso</span><span class="sxs-lookup"><span data-stu-id="a1cab-129">-PrefixLength</span></span>
<span data-ttu-id="a1cab-130">La lunghezza di PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="a1cab-130">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cab-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1cab-131">-ResourceGroupName</span></span>
<span data-ttu-id="a1cab-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1cab-132">The resource group name.</span></span>

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

### <span data-ttu-id="a1cab-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="a1cab-133">-Sku</span></span>
<span data-ttu-id="a1cab-134">Nome USK del prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="a1cab-134">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cab-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1cab-135">-Tag</span></span>
<span data-ttu-id="a1cab-136">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a1cab-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a1cab-137">-Tier</span><span class="sxs-lookup"><span data-stu-id="a1cab-137">-Tier</span></span>
<span data-ttu-id="a1cab-138">Livello di SKU del prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="a1cab-138">The public IP Prefix Sku tier.</span></span>

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

### <span data-ttu-id="a1cab-139">-Zona</span><span class="sxs-lookup"><span data-stu-id="a1cab-139">-Zone</span></span>
<span data-ttu-id="a1cab-140">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="a1cab-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="a1cab-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1cab-141">-Confirm</span></span>
<span data-ttu-id="a1cab-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1cab-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cab-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1cab-143">-WhatIf</span></span>
<span data-ttu-id="a1cab-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1cab-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1cab-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1cab-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cab-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1cab-146">CommonParameters</span></span>
<span data-ttu-id="a1cab-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1cab-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1cab-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1cab-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1cab-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1cab-149">INPUTS</span></span>

### <span data-ttu-id="a1cab-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a1cab-150">System.String</span></span>

### <span data-ttu-id="a1cab-151">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="a1cab-151">System.UInt16</span></span>

### <span data-ttu-id="a1cab-152">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="a1cab-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="a1cab-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="a1cab-153">System.String[]</span></span>

### <span data-ttu-id="a1cab-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a1cab-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a1cab-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1cab-155">OUTPUTS</span></span>

### <span data-ttu-id="a1cab-156">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a1cab-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="a1cab-157">Note</span><span class="sxs-lookup"><span data-stu-id="a1cab-157">NOTES</span></span>

## <span data-ttu-id="a1cab-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1cab-158">RELATED LINKS</span></span>

[<span data-ttu-id="a1cab-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a1cab-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="a1cab-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a1cab-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="a1cab-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a1cab-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
