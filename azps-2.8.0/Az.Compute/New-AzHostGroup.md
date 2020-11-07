---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 9d6614204c8c6e8e95617ed989e3f75b88c9744e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675332"
---
# <span data-ttu-id="9dbdf-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="9dbdf-101">New-AzHostGroup</span></span>

## <span data-ttu-id="9dbdf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9dbdf-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbdf-103">Crea un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-103">Creates a host group.</span></span>

## <span data-ttu-id="9dbdf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9dbdf-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dbdf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9dbdf-105">DESCRIPTION</span></span>
<span data-ttu-id="9dbdf-106">Questo cmdlet creerà un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="9dbdf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9dbdf-107">EXAMPLES</span></span>

### <span data-ttu-id="9dbdf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9dbdf-108">Example 1</span></span>
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

<span data-ttu-id="9dbdf-109">Questo comando crea un gruppo host nella posizione e nella zona specificate.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="9dbdf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9dbdf-110">PARAMETERS</span></span>

### <span data-ttu-id="9dbdf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dbdf-111">-AsJob</span></span>
<span data-ttu-id="9dbdf-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9dbdf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dbdf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbdf-113">-DefaultProfile</span></span>
<span data-ttu-id="9dbdf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dbdf-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9dbdf-115">-Location</span></span>
<span data-ttu-id="9dbdf-116">Specifica la posizione.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-116">Specifies location.</span></span>

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

### <span data-ttu-id="9dbdf-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9dbdf-117">-Name</span></span>
<span data-ttu-id="9dbdf-118">Specifica il nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="9dbdf-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="9dbdf-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="9dbdf-120">Specifica il numero di domini di errore che il gruppo ospitante può estendere.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="9dbdf-121">Il valore minimo è 1 e il valore massimo è 3.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="9dbdf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dbdf-122">-ResourceGroupName</span></span>
<span data-ttu-id="9dbdf-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="9dbdf-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="9dbdf-124">-Tag</span></span>
<span data-ttu-id="9dbdf-125">Specifica i tag</span><span class="sxs-lookup"><span data-stu-id="9dbdf-125">Specifies Tags</span></span>

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

### <span data-ttu-id="9dbdf-126">-Zona</span><span class="sxs-lookup"><span data-stu-id="9dbdf-126">-Zone</span></span>
<span data-ttu-id="9dbdf-127">Specifica le aree del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="9dbdf-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9dbdf-128">-Confirm</span></span>
<span data-ttu-id="9dbdf-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dbdf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dbdf-130">-WhatIf</span></span>
<span data-ttu-id="9dbdf-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dbdf-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dbdf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbdf-133">CommonParameters</span></span>
<span data-ttu-id="9dbdf-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbdf-135">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dbdf-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbdf-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9dbdf-136">INPUTS</span></span>

### <span data-ttu-id="9dbdf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9dbdf-137">System.String</span></span>

## <span data-ttu-id="9dbdf-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9dbdf-138">OUTPUTS</span></span>

### <span data-ttu-id="9dbdf-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="9dbdf-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="9dbdf-140">Note</span><span class="sxs-lookup"><span data-stu-id="9dbdf-140">NOTES</span></span>

## <span data-ttu-id="9dbdf-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9dbdf-141">RELATED LINKS</span></span>
