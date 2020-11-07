---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 890ec07cecd46badaccc1c2140290fd8042d319b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674054"
---
# <span data-ttu-id="92d98-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="92d98-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="92d98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92d98-102">SYNOPSIS</span></span>
<span data-ttu-id="92d98-103">Aggiornare un cluster di Kusto esistente.</span><span class="sxs-lookup"><span data-stu-id="92d98-103">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="92d98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92d98-104">SYNTAX</span></span>

### <span data-ttu-id="92d98-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92d98-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>] [-Capacity <Int32>]
 [-Tier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92d98-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="92d98-106">ByResourceId</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92d98-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92d98-107">ByInputObject</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-InputObject] <PSKustoCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92d98-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92d98-108">DESCRIPTION</span></span>
<span data-ttu-id="92d98-109">Aggiornare un cluster di Kusto esistente.</span><span class="sxs-lookup"><span data-stu-id="92d98-109">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="92d98-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92d98-110">EXAMPLES</span></span>

### <span data-ttu-id="92d98-111">Esempio 1-aggiornare un cluster esistente per nome</span><span class="sxs-lookup"><span data-stu-id="92d98-111">Example 1 - Update an existing cluster by name</span></span>

```
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Sku D14_v2

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Sku               : D14_v2
Capacity          : 5
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="92d98-112">Il comando precedente aggiorna il livello del cluster kusto "mykustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="92d98-112">The above command updates the tier of the Kusto cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="92d98-113">Esempio 2-aggiornare un cluster esistente tramite piping</span><span class="sxs-lookup"><span data-stu-id="92d98-113">Example 2 - Update an existing cluster by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Update-AzKustoCluster -Sku D14_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D14_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="92d98-114">Il comando precedente restituisce il cluster kusto "mykustocluster" nel gruppo di risorse "testrg" che usa il `Get-AzKustoCluster` cmdlet e quindi convoglia il risultato in per `Update-AzKustoCluster` aggiornare il livello del cluster in "standard".</span><span class="sxs-lookup"><span data-stu-id="92d98-114">The above command gets the Kusto cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Update-AzKustoCluster` to update the cluster's tier to "standard".</span></span>

## <span data-ttu-id="92d98-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92d98-115">PARAMETERS</span></span>

### <span data-ttu-id="92d98-116">-Capacità</span><span class="sxs-lookup"><span data-stu-id="92d98-116">-Capacity</span></span>
<span data-ttu-id="92d98-117">Numero di istanza della VM.</span><span class="sxs-lookup"><span data-stu-id="92d98-117">The instance number of the VM.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d98-118">-DefaultProfile</span></span>
<span data-ttu-id="92d98-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92d98-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d98-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92d98-120">-InputObject</span></span>
<span data-ttu-id="92d98-121">Oggetto cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="92d98-121">Kusto cluster object.</span></span>

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

### <span data-ttu-id="92d98-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="92d98-122">-Name</span></span>
<span data-ttu-id="92d98-123">Nome del cluster da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="92d98-123">Name of cluster to be updated.</span></span>

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

### <span data-ttu-id="92d98-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92d98-124">-ResourceGroupName</span></span>
<span data-ttu-id="92d98-125">Nome del gruppo di risorse in cui è presente il cluster.</span><span class="sxs-lookup"><span data-stu-id="92d98-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="92d98-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92d98-126">-ResourceId</span></span>
<span data-ttu-id="92d98-127">Kusto cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="92d98-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="92d98-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="92d98-128">-SkuName</span></span>
<span data-ttu-id="92d98-129">Nome dell'USK usato per creare il cluster</span><span class="sxs-lookup"><span data-stu-id="92d98-129">Name of the Sku used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d98-130">-Tier</span><span class="sxs-lookup"><span data-stu-id="92d98-130">-Tier</span></span>
<span data-ttu-id="92d98-131">Nome del livello usato per creare il cluster</span><span class="sxs-lookup"><span data-stu-id="92d98-131">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d98-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="92d98-132">-Confirm</span></span>
<span data-ttu-id="92d98-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92d98-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92d98-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92d98-134">-WhatIf</span></span>
<span data-ttu-id="92d98-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92d98-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92d98-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92d98-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92d98-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d98-137">CommonParameters</span></span>
<span data-ttu-id="92d98-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92d98-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d98-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92d98-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d98-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92d98-140">INPUTS</span></span>

### <span data-ttu-id="92d98-141">System. String</span><span class="sxs-lookup"><span data-stu-id="92d98-141">System.String</span></span>

### <span data-ttu-id="92d98-142">Microsoft. Azure. Commands. kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="92d98-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="92d98-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92d98-143">OUTPUTS</span></span>

### <span data-ttu-id="92d98-144">Microsoft. Azure. Commands. kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="92d98-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="92d98-145">Note</span><span class="sxs-lookup"><span data-stu-id="92d98-145">NOTES</span></span>

## <span data-ttu-id="92d98-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92d98-146">RELATED LINKS</span></span>