---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
ms.openlocfilehash: d52bc8737392bf6fce004a90b1f2fe5207cffea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688075"
---
# <span data-ttu-id="06fb5-101">New-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="06fb5-101">New-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="06fb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="06fb5-103">Crea un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="06fb5-103">Creates a Public IP Prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06fb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06fb5-104">SYNTAX</span></span>

```
New-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06fb5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06fb5-105">DESCRIPTION</span></span>
<span data-ttu-id="06fb5-106">Il cmdlet **New-AzureRmPublicIpPrefix** crea un prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="06fb5-106">The **New-AzureRmPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="06fb5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06fb5-107">EXAMPLES</span></span>

### <span data-ttu-id="06fb5-108">1: creare un nuovo prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="06fb5-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="06fb5-109">Questo comando crea una nuova risorsa di prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="06fb5-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="06fb5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06fb5-110">PARAMETERS</span></span>

### <span data-ttu-id="06fb5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06fb5-111">-AsJob</span></span>
<span data-ttu-id="06fb5-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="06fb5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06fb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06fb5-113">-DefaultProfile</span></span>
<span data-ttu-id="06fb5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06fb5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06fb5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="06fb5-115">-Force</span></span>
<span data-ttu-id="06fb5-116">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="06fb5-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="06fb5-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="06fb5-117">-IpAddressVersion</span></span>
<span data-ttu-id="06fb5-118">Versione dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="06fb5-118">The public IP address version.</span></span>

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

### <span data-ttu-id="06fb5-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="06fb5-119">-IpTag</span></span>
<span data-ttu-id="06fb5-120">Elenco IpTag.</span><span class="sxs-lookup"><span data-stu-id="06fb5-120">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06fb5-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="06fb5-121">-Location</span></span>
<span data-ttu-id="06fb5-122">Posizione del prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="06fb5-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="06fb5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="06fb5-123">-Name</span></span>
<span data-ttu-id="06fb5-124">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="06fb5-124">The resource name.</span></span>

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

### <span data-ttu-id="06fb5-125">-LunghezzaPrefisso</span><span class="sxs-lookup"><span data-stu-id="06fb5-125">-PrefixLength</span></span>
<span data-ttu-id="06fb5-126">La lunghezza di PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="06fb5-126">The PublicIPPrefix length</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06fb5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06fb5-127">-ResourceGroupName</span></span>
<span data-ttu-id="06fb5-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06fb5-128">The resource group name.</span></span>

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

### <span data-ttu-id="06fb5-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="06fb5-129">-Sku</span></span>
<span data-ttu-id="06fb5-130">Nome USK del prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="06fb5-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06fb5-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="06fb5-131">-Tag</span></span>
<span data-ttu-id="06fb5-132">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="06fb5-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="06fb5-133">-Zona</span><span class="sxs-lookup"><span data-stu-id="06fb5-133">-Zone</span></span>
<span data-ttu-id="06fb5-134">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="06fb5-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="06fb5-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06fb5-135">-Confirm</span></span>
<span data-ttu-id="06fb5-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06fb5-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06fb5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06fb5-137">-WhatIf</span></span>
<span data-ttu-id="06fb5-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06fb5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06fb5-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06fb5-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06fb5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06fb5-140">CommonParameters</span></span>
<span data-ttu-id="06fb5-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06fb5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="06fb5-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06fb5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06fb5-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06fb5-143">INPUTS</span></span>

### <span data-ttu-id="06fb5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="06fb5-144">System.String</span></span>
<span data-ttu-id="06fb5-145">System. UInt16 System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="06fb5-145">System.UInt16 System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="06fb5-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06fb5-146">OUTPUTS</span></span>

### <span data-ttu-id="06fb5-147">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="06fb5-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="06fb5-148">Note</span><span class="sxs-lookup"><span data-stu-id="06fb5-148">NOTES</span></span>

## <span data-ttu-id="06fb5-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06fb5-149">RELATED LINKS</span></span>
