---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032583"
---
# <span data-ttu-id="aa916-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="aa916-101">New-AzHostGroup</span></span>

## <span data-ttu-id="aa916-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa916-102">SYNOPSIS</span></span>
<span data-ttu-id="aa916-103">Crea un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="aa916-103">Creates a host group.</span></span>

## <span data-ttu-id="aa916-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa916-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa916-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa916-105">DESCRIPTION</span></span>
<span data-ttu-id="aa916-106">Questo cmdlet creerà un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="aa916-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="aa916-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa916-107">EXAMPLES</span></span>

### <span data-ttu-id="aa916-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aa916-108">Example 1</span></span>
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

<span data-ttu-id="aa916-109">Questo comando crea un gruppo host nella posizione e nella zona specificate.</span><span class="sxs-lookup"><span data-stu-id="aa916-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="aa916-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa916-110">PARAMETERS</span></span>

### <span data-ttu-id="aa916-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa916-111">-AsJob</span></span>
<span data-ttu-id="aa916-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="aa916-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa916-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa916-113">-DefaultProfile</span></span>
<span data-ttu-id="aa916-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa916-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa916-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="aa916-115">-Location</span></span>
<span data-ttu-id="aa916-116">Specifica la posizione.</span><span class="sxs-lookup"><span data-stu-id="aa916-116">Specifies location.</span></span>

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

### <span data-ttu-id="aa916-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa916-117">-Name</span></span>
<span data-ttu-id="aa916-118">Specifica il nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="aa916-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="aa916-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="aa916-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="aa916-120">Specifica il numero di domini di errore che il gruppo ospitante può estendere.</span><span class="sxs-lookup"><span data-stu-id="aa916-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="aa916-121">Il valore minimo è 1 e il valore massimo è 3.</span><span class="sxs-lookup"><span data-stu-id="aa916-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="aa916-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa916-122">-ResourceGroupName</span></span>
<span data-ttu-id="aa916-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aa916-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="aa916-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa916-124">-Tag</span></span>
<span data-ttu-id="aa916-125">Specifica i tag</span><span class="sxs-lookup"><span data-stu-id="aa916-125">Specifies Tags</span></span>

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

### <span data-ttu-id="aa916-126">-Zona</span><span class="sxs-lookup"><span data-stu-id="aa916-126">-Zone</span></span>
<span data-ttu-id="aa916-127">Specifica le aree del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="aa916-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="aa916-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="aa916-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="aa916-129">Specifica se HostGroup consentirà la posizione automatica della VM.</span><span class="sxs-lookup"><span data-stu-id="aa916-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="aa916-130">Posizionamento automatico: queste VM vengono posizionate su host dedicati, scelti da Azure, sotto il gruppo host dedicato.</span><span class="sxs-lookup"><span data-stu-id="aa916-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="aa916-131">Se non viene specificato, il valore predefinito sarà true.</span><span class="sxs-lookup"><span data-stu-id="aa916-131">If not specified, default value will be true.</span></span>

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


### <span data-ttu-id="aa916-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa916-132">-Confirm</span></span>
<span data-ttu-id="aa916-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa916-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa916-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa916-134">-WhatIf</span></span>
<span data-ttu-id="aa916-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa916-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa916-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa916-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa916-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa916-137">CommonParameters</span></span>
<span data-ttu-id="aa916-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa916-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa916-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa916-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa916-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa916-140">INPUTS</span></span>

### <span data-ttu-id="aa916-141">System. String</span><span class="sxs-lookup"><span data-stu-id="aa916-141">System.String</span></span>

## <span data-ttu-id="aa916-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa916-142">OUTPUTS</span></span>

### <span data-ttu-id="aa916-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="aa916-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="aa916-144">Note</span><span class="sxs-lookup"><span data-stu-id="aa916-144">NOTES</span></span>

## <span data-ttu-id="aa916-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa916-145">RELATED LINKS</span></span>
