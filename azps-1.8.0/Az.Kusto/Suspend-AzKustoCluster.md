---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/suspend-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
ms.openlocfilehash: 6eceaffb371226c9dda0099a32a309272d6bdb3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835555"
---
# <span data-ttu-id="bebd2-101">Suspend-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="bebd2-101">Suspend-AzKustoCluster</span></span>

## <span data-ttu-id="bebd2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bebd2-102">SYNOPSIS</span></span>
<span data-ttu-id="bebd2-103">Sospendere un cluster di Kusto esistente.</span><span class="sxs-lookup"><span data-stu-id="bebd2-103">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="bebd2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bebd2-104">SYNTAX</span></span>

### <span data-ttu-id="bebd2-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bebd2-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bebd2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bebd2-106">ByResourceId</span></span>
```
Suspend-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bebd2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bebd2-107">ByInputObject</span></span>
```
Suspend-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bebd2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bebd2-108">DESCRIPTION</span></span>
<span data-ttu-id="bebd2-109">Sospendere un cluster di Kusto esistente.</span><span class="sxs-lookup"><span data-stu-id="bebd2-109">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="bebd2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bebd2-110">EXAMPLES</span></span>

### <span data-ttu-id="bebd2-111">Esempio 1-sospendere un cluster di Kusto esistente per nome</span><span class="sxs-lookup"><span data-stu-id="bebd2-111">Example 1 - Suspend an existing Kusto cluster by name</span></span>

```
PS C:\> Suspend-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="bebd2-112">Il comando precedente sospende il cluster kusto denominato "mykustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="bebd2-112">The above command suspends the Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="bebd2-113">Esempio 2-sospendere un cluster di Kusto esistente tramite piping</span><span class="sxs-lookup"><span data-stu-id="bebd2-113">Example 2 - Suspend an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Suspend-AzKustoCluster
```

<span data-ttu-id="bebd2-114">Il comando precedente ottiene il cluster kusto denominato "mykustocluster" nel gruppo di risorse "testrg" con il `Get-AzKustoCluster` cmdlet e quindi convoglia il risultato in `Suspend-AzKustoCluster` per sospenderlo.</span><span class="sxs-lookup"><span data-stu-id="bebd2-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Suspend-AzKustoCluster` to suspend it.</span></span>

## <span data-ttu-id="bebd2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bebd2-115">PARAMETERS</span></span>

### <span data-ttu-id="bebd2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bebd2-116">-DefaultProfile</span></span>
<span data-ttu-id="bebd2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bebd2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bebd2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bebd2-118">-InputObject</span></span>
<span data-ttu-id="bebd2-119">Oggetto cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="bebd2-119">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bebd2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bebd2-120">-Name</span></span>
<span data-ttu-id="bebd2-121">Nome del cluster da sospendere.</span><span class="sxs-lookup"><span data-stu-id="bebd2-121">Name of cluster to be suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bebd2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bebd2-122">-PassThru</span></span>
<span data-ttu-id="bebd2-123">Restituirà se il cluster specificato è stato sospeso o meno.</span><span class="sxs-lookup"><span data-stu-id="bebd2-123">Return whether the specified cluster was successfully suspended or not.</span></span>

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

### <span data-ttu-id="bebd2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bebd2-124">-ResourceGroupName</span></span>
<span data-ttu-id="bebd2-125">Nome del gruppo di risorse in cui è presente il cluster.</span><span class="sxs-lookup"><span data-stu-id="bebd2-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bebd2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bebd2-126">-ResourceId</span></span>
<span data-ttu-id="bebd2-127">Kusto cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="bebd2-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bebd2-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bebd2-128">-Confirm</span></span>
<span data-ttu-id="bebd2-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bebd2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bebd2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bebd2-130">-WhatIf</span></span>
<span data-ttu-id="bebd2-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bebd2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bebd2-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bebd2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bebd2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bebd2-133">CommonParameters</span></span>
<span data-ttu-id="bebd2-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bebd2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bebd2-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bebd2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bebd2-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bebd2-136">INPUTS</span></span>

### <span data-ttu-id="bebd2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bebd2-137">System.String</span></span>

### <span data-ttu-id="bebd2-138">Microsoft. Azure. Commands. kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="bebd2-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="bebd2-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bebd2-139">OUTPUTS</span></span>

### <span data-ttu-id="bebd2-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bebd2-140">System.Boolean</span></span>

## <span data-ttu-id="bebd2-141">Note</span><span class="sxs-lookup"><span data-stu-id="bebd2-141">NOTES</span></span>

## <span data-ttu-id="bebd2-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bebd2-142">RELATED LINKS</span></span>
