---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 69ab5a7ae89184a5d77344d45801da307e7840bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959677"
---
# <span data-ttu-id="475ea-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="475ea-101">New-AzHostGroup</span></span>

## <span data-ttu-id="475ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="475ea-102">SYNOPSIS</span></span>
<span data-ttu-id="475ea-103">Crea un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="475ea-103">Creates a host group.</span></span>

## <span data-ttu-id="475ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="475ea-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="475ea-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="475ea-105">DESCRIPTION</span></span>
<span data-ttu-id="475ea-106">Questo cmdlet creerà un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="475ea-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="475ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="475ea-107">EXAMPLES</span></span>

### <span data-ttu-id="475ea-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="475ea-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="475ea-109">Questo comando crea un gruppo host nella posizione e nell'area specificata.</span><span class="sxs-lookup"><span data-stu-id="475ea-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="475ea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="475ea-110">PARAMETERS</span></span>

### <span data-ttu-id="475ea-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="475ea-111">-AsJob</span></span>
<span data-ttu-id="475ea-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="475ea-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="475ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475ea-113">-DefaultProfile</span></span>
<span data-ttu-id="475ea-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="475ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="475ea-115">-Location</span><span class="sxs-lookup"><span data-stu-id="475ea-115">-Location</span></span>
<span data-ttu-id="475ea-116">Specifica la posizione.</span><span class="sxs-lookup"><span data-stu-id="475ea-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475ea-117">-Name</span><span class="sxs-lookup"><span data-stu-id="475ea-117">-Name</span></span>
<span data-ttu-id="475ea-118">Specifica il nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="475ea-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="475ea-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="475ea-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="475ea-120">Specifica il numero di domini di errore che il gruppo host può contenere.</span><span class="sxs-lookup"><span data-stu-id="475ea-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="475ea-121">Il valore minimo è 1 e il valore massimo è 3.</span><span class="sxs-lookup"><span data-stu-id="475ea-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="475ea-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="475ea-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="475ea-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="475ea-124">-Tag</span></span>
<span data-ttu-id="475ea-125">Specifica i tag</span><span class="sxs-lookup"><span data-stu-id="475ea-125">Specifies Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475ea-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="475ea-126">-Zone</span></span>
<span data-ttu-id="475ea-127">Specifica le aree del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="475ea-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475ea-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="475ea-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="475ea-129">Specifica se HostGroup abiliterà il posizionamento automatico delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="475ea-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="475ea-130">Il posizionamento automatico indica che queste macchine virtuali sono collocate in host dedicati, scelti da Azure, nel gruppo host dedicato.</span><span class="sxs-lookup"><span data-stu-id="475ea-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="475ea-131">Se non viene specificato, il valore predefinito sarà False.</span><span class="sxs-lookup"><span data-stu-id="475ea-131">If not specified, default value will be false.</span></span>

```yaml
Type: bool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="475ea-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="475ea-132">-Confirm</span></span>
<span data-ttu-id="475ea-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="475ea-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="475ea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="475ea-134">-WhatIf</span></span>
<span data-ttu-id="475ea-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="475ea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="475ea-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="475ea-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="475ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475ea-137">CommonParameters</span></span>
<span data-ttu-id="475ea-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475ea-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="475ea-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475ea-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="475ea-140">INPUTS</span></span>

### <span data-ttu-id="475ea-141">System.String</span><span class="sxs-lookup"><span data-stu-id="475ea-141">System.String</span></span>

## <span data-ttu-id="475ea-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="475ea-142">OUTPUTS</span></span>

### <span data-ttu-id="475ea-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="475ea-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="475ea-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="475ea-144">NOTES</span></span>

## <span data-ttu-id="475ea-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="475ea-145">RELATED LINKS</span></span>
