---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184454"
---
# <span data-ttu-id="53156-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="53156-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="53156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53156-102">SYNOPSIS</span></span>
<span data-ttu-id="53156-103">Crea una ipAllocation di Azure.</span><span class="sxs-lookup"><span data-stu-id="53156-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="53156-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53156-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53156-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="53156-105">DESCRIPTION</span></span>
<span data-ttu-id="53156-106">Il cmdlet **New-AzIpAllocation** crea una ipAllocation di Azure</span><span class="sxs-lookup"><span data-stu-id="53156-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="53156-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53156-107">EXAMPLES</span></span>

### <span data-ttu-id="53156-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53156-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="53156-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="53156-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="53156-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53156-110">PARAMETERS</span></span>

### <span data-ttu-id="53156-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53156-111">-AsJob</span></span>
<span data-ttu-id="53156-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="53156-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53156-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53156-113">-DefaultProfile</span></span>
<span data-ttu-id="53156-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53156-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53156-115">-Force</span><span class="sxs-lookup"><span data-stu-id="53156-115">-Force</span></span>
<span data-ttu-id="53156-116">Non chiedere conferma se si vuole ignorare una risorsa</span><span class="sxs-lookup"><span data-stu-id="53156-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="53156-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="53156-117">-IpAllocationTag</span></span>
<span data-ttu-id="53156-118">Tag di allocazione dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="53156-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="53156-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="53156-119">-IpAllocationType</span></span>
<span data-ttu-id="53156-120">Tipo di allocazione IP</span><span class="sxs-lookup"><span data-stu-id="53156-120">The type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hypernet, Undefined

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53156-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="53156-121">-IpamAllocationId</span></span>
<span data-ttu-id="53156-122">ID di assegnazione ipam dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="53156-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="53156-123">-Location</span><span class="sxs-lookup"><span data-stu-id="53156-123">-Location</span></span>
<span data-ttu-id="53156-124">posizione.</span><span class="sxs-lookup"><span data-stu-id="53156-124">location.</span></span>

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

### <span data-ttu-id="53156-125">-Name</span><span class="sxs-lookup"><span data-stu-id="53156-125">-Name</span></span>
<span data-ttu-id="53156-126">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="53156-126">The resource name.</span></span>

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

### <span data-ttu-id="53156-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="53156-127">-Prefix</span></span>
<span data-ttu-id="53156-128">Prefisso dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="53156-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="53156-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="53156-129">-PrefixLength</span></span>
<span data-ttu-id="53156-130">Lunghezza prefisso dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="53156-130">The prefix length of the IP allocation</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53156-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="53156-131">-PrefixType</span></span>
<span data-ttu-id="53156-132">Tipo di prefisso dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="53156-132">The prefix type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPV4, IPV6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53156-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53156-133">-ResourceGroupName</span></span>
<span data-ttu-id="53156-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="53156-134">The resource group name.</span></span>

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

### <span data-ttu-id="53156-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="53156-135">-Tag</span></span>
<span data-ttu-id="53156-136">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="53156-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="53156-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53156-137">-Confirm</span></span>
<span data-ttu-id="53156-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53156-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53156-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53156-139">-WhatIf</span></span>
<span data-ttu-id="53156-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53156-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53156-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53156-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53156-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53156-142">CommonParameters</span></span>
<span data-ttu-id="53156-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53156-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53156-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="53156-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53156-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="53156-145">INPUTS</span></span>

### <span data-ttu-id="53156-146">System.String</span><span class="sxs-lookup"><span data-stu-id="53156-146">System.String</span></span>

### <span data-ttu-id="53156-147">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="53156-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="53156-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="53156-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="53156-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53156-149">OUTPUTS</span></span>

### <span data-ttu-id="53156-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="53156-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="53156-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="53156-151">NOTES</span></span>

## <span data-ttu-id="53156-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53156-152">RELATED LINKS</span></span>
