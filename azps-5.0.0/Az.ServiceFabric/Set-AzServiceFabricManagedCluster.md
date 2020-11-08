---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200483"
---
# <span data-ttu-id="74561-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="74561-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="74561-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74561-102">SYNOPSIS</span></span>
<span data-ttu-id="74561-103">Impostare le proprietà delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="74561-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="74561-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74561-104">SYNTAX</span></span>

### <span data-ttu-id="74561-105">ByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="74561-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74561-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="74561-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74561-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="74561-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74561-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74561-108">DESCRIPTION</span></span>
<span data-ttu-id="74561-109">Impostare le proprietà delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="74561-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="74561-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74561-110">EXAMPLES</span></span>

### <span data-ttu-id="74561-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="74561-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="74561-112">Aggiornare il nome DNS e la porta di connessione client per il cluster.</span><span class="sxs-lookup"><span data-stu-id="74561-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="74561-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="74561-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="74561-114">Aggiornare il nome DNS e la porta di connessione client per il cluster con piping.</span><span class="sxs-lookup"><span data-stu-id="74561-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="74561-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74561-115">PARAMETERS</span></span>

### <span data-ttu-id="74561-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74561-116">-AsJob</span></span>
<span data-ttu-id="74561-117">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="74561-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="74561-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="74561-118">-ClientConnectionPort</span></span>
<span data-ttu-id="74561-119">Porta usata per le connessioni client al cluster.</span><span class="sxs-lookup"><span data-stu-id="74561-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="74561-120">Impostazione predefinita: 19000.</span><span class="sxs-lookup"><span data-stu-id="74561-120">Default: 19000.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74561-121">-Codeversion</span><span class="sxs-lookup"><span data-stu-id="74561-121">-CodeVersion</span></span>
<span data-ttu-id="74561-122">Versione del codice del cluster.</span><span class="sxs-lookup"><span data-stu-id="74561-122">Cluster code version.</span></span> <span data-ttu-id="74561-123">Usare solo se la modalità di aggiornamento è manuale.</span><span class="sxs-lookup"><span data-stu-id="74561-123">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74561-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74561-124">-DefaultProfile</span></span>
<span data-ttu-id="74561-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74561-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74561-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="74561-126">-DnsName</span></span>
<span data-ttu-id="74561-127">Nome DNS del cluster.</span><span class="sxs-lookup"><span data-stu-id="74561-127">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74561-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="74561-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="74561-129">Porta usata per le connessioni HTTP al cluster.</span><span class="sxs-lookup"><span data-stu-id="74561-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="74561-130">Impostazione predefinita: 19080.</span><span class="sxs-lookup"><span data-stu-id="74561-130">Default: 19080.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74561-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74561-131">-InputObject</span></span>
<span data-ttu-id="74561-132">Risorsa cluster gestito</span><span class="sxs-lookup"><span data-stu-id="74561-132">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74561-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="74561-133">-Name</span></span>
<span data-ttu-id="74561-134">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="74561-134">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74561-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74561-135">-ResourceGroupName</span></span>
<span data-ttu-id="74561-136">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="74561-136">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74561-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74561-137">-ResourceId</span></span>
<span data-ttu-id="74561-138">ID risorsa cluster gestito</span><span class="sxs-lookup"><span data-stu-id="74561-138">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74561-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="74561-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="74561-140">Endpoint usato dal proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="74561-140">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74561-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="74561-141">-UpgradeMode</span></span>
<span data-ttu-id="74561-142">Modalità di aggiornamento della versione del codice cluster.</span><span class="sxs-lookup"><span data-stu-id="74561-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="74561-143">Automatica o manuale.</span><span class="sxs-lookup"><span data-stu-id="74561-143">Automatic or Manual.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode]
Parameter Sets: WithPramsByName, ByNameById
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74561-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="74561-144">-Confirm</span></span>
<span data-ttu-id="74561-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74561-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74561-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74561-146">-WhatIf</span></span>
<span data-ttu-id="74561-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74561-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74561-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74561-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74561-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74561-149">CommonParameters</span></span>
<span data-ttu-id="74561-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74561-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74561-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74561-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74561-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74561-152">INPUTS</span></span>

### <span data-ttu-id="74561-153">System. String</span><span class="sxs-lookup"><span data-stu-id="74561-153">System.String</span></span>

## <span data-ttu-id="74561-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74561-154">OUTPUTS</span></span>

### <span data-ttu-id="74561-155">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="74561-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="74561-156">Note</span><span class="sxs-lookup"><span data-stu-id="74561-156">NOTES</span></span>

## <span data-ttu-id="74561-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74561-157">RELATED LINKS</span></span>
