---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: c4a082847c8d86271d7ded5d03f9c7c27c00501b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019679"
---
# <span data-ttu-id="0a945-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0a945-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="0a945-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a945-102">SYNOPSIS</span></span>
<span data-ttu-id="0a945-103">Creare un nuovo servizio tessuto servizio nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="0a945-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="0a945-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a945-104">SYNTAX</span></span>

### <span data-ttu-id="0a945-105">Stateless-Singleton (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a945-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a945-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="0a945-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a945-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="0a945-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a945-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="0a945-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a945-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="0a945-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a945-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="0a945-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a945-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a945-111">DESCRIPTION</span></span>
<span data-ttu-id="0a945-112">Questo cmdlet consente di creare servizi apolidi o con stato nell'applicazione specificata.</span><span class="sxs-lookup"><span data-stu-id="0a945-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="0a945-113">Il servizio deve uscire nel manifesto dell'applicazione e il tipo deve essere uguale a quello del manifesto.</span><span class="sxs-lookup"><span data-stu-id="0a945-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="0a945-114">Il nome dell'applicazione deve essere un prefisso del nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="0a945-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="0a945-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a945-115">EXAMPLES</span></span>

### <span data-ttu-id="0a945-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0a945-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="0a945-117">In questo esempio verrà creato un nuovo servizio senza stato "testApp ~ testService1" con il conteggio delle istanze-1 (in tutti i nodi).</span><span class="sxs-lookup"><span data-stu-id="0a945-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="0a945-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0a945-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="0a945-119">Questo esempio creerà un nuovo servizio con stato "testApp ~ testService2" con una destinazione di 5 nodi.</span><span class="sxs-lookup"><span data-stu-id="0a945-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="0a945-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a945-120">PARAMETERS</span></span>

### <span data-ttu-id="0a945-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0a945-121">-ApplicationName</span></span>
<span data-ttu-id="0a945-122">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0a945-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="0a945-123">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0a945-123">-ClusterName</span></span>
<span data-ttu-id="0a945-124">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a945-124">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="0a945-125">-DefaultMoveCost</span></span>
<span data-ttu-id="0a945-126">Specificare il costo predefinito per una trasloco.</span><span class="sxs-lookup"><span data-stu-id="0a945-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="0a945-127">I costi più elevati rendono meno probabile che il gestore delle risorse del cluster sposti la replica quando si prova a bilanciare il cluster</span><span class="sxs-lookup"><span data-stu-id="0a945-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.MoveCostEnum
Parameter Sets: (All)
Aliases:
Accepted values: Zero, Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a945-128">-DefaultProfile</span></span>
<span data-ttu-id="0a945-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a945-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a945-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="0a945-130">-InstanceCount</span></span>
<span data-ttu-id="0a945-131">Specificare il conteggio delle istanze per il servizio</span><span class="sxs-lookup"><span data-stu-id="0a945-131">Specify the instance count for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="0a945-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="0a945-133">Specificare le dimensioni del set di repliche min per il servizio</span><span class="sxs-lookup"><span data-stu-id="0a945-133">Specify the min replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a945-134">-Name</span></span>
<span data-ttu-id="0a945-135">Specificare il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="0a945-135">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="0a945-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="0a945-137">Indica che il servizio usa lo schema di partizione denominato.</span><span class="sxs-lookup"><span data-stu-id="0a945-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="0a945-138">I servizi che usano questo modello in genere hanno dati che possono essere secchi, all'interno di un set limitato.</span><span class="sxs-lookup"><span data-stu-id="0a945-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="0a945-139">Alcuni esempi comuni di campi dati usati come chiavi di partizione denominate sono le aree geografiche, i codici postali, i gruppi di clienti o altri limiti aziendali.</span><span class="sxs-lookup"><span data-stu-id="0a945-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Named, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="0a945-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="0a945-141">Indica che il servizio usa lo schema di partizione singleton.</span><span class="sxs-lookup"><span data-stu-id="0a945-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="0a945-142">Le partizioni Singleton vengono in genere usate quando il servizio non richiede alcun routing aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="0a945-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateful-Singleton
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="0a945-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="0a945-144">Indica che il servizio usa lo schema di partizione UniformInt64.</span><span class="sxs-lookup"><span data-stu-id="0a945-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="0a945-145">Questo significa che ogni partizione possiede un intervallo di chiavi Int64.</span><span class="sxs-lookup"><span data-stu-id="0a945-145">This means that each partition owns a range of int64 keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-UniformInt64Range, Stateful-UniformInt64Range
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="0a945-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="0a945-147">Specificare la durata di attesa della perdita del quorum per il servizio</span><span class="sxs-lookup"><span data-stu-id="0a945-147">Specify the quorum loss wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="0a945-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="0a945-149">Specificare la durata di attesa del riavvio della replica per il servizio</span><span class="sxs-lookup"><span data-stu-id="0a945-149">Specify the replica restart wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a945-150">-ResourceGroupName</span></span>
<span data-ttu-id="0a945-151">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a945-151">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0a945-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="0a945-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="0a945-153">Specificare la durata della replica in standby per il servizio</span><span class="sxs-lookup"><span data-stu-id="0a945-153">Specify the stand by replica duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-154">-Con stato</span><span class="sxs-lookup"><span data-stu-id="0a945-154">-Stateful</span></span>
<span data-ttu-id="0a945-155">Usare per il servizio con stato</span><span class="sxs-lookup"><span data-stu-id="0a945-155">Use for stateful service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-156">-Apolide</span><span class="sxs-lookup"><span data-stu-id="0a945-156">-Stateless</span></span>
<span data-ttu-id="0a945-157">Uso per il servizio apolidi</span><span class="sxs-lookup"><span data-stu-id="0a945-157">Use for stateless service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="0a945-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="0a945-159">Specificare le dimensioni del set di repliche di destinazione per il servizio</span><span class="sxs-lookup"><span data-stu-id="0a945-159">Specify the target replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-160">-Digitare</span><span class="sxs-lookup"><span data-stu-id="0a945-160">-Type</span></span>
<span data-ttu-id="0a945-161">Specifica il nome del tipo di servizio dell'applicazione, deve esistere nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0a945-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a945-162">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0a945-162">-Confirm</span></span>
<span data-ttu-id="0a945-163">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a945-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a945-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a945-164">-WhatIf</span></span>
<span data-ttu-id="0a945-165">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a945-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a945-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a945-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a945-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a945-167">CommonParameters</span></span>
<span data-ttu-id="0a945-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a945-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a945-169">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a945-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a945-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a945-170">INPUTS</span></span>

### <span data-ttu-id="0a945-171">System. String</span><span class="sxs-lookup"><span data-stu-id="0a945-171">System.String</span></span>

## <span data-ttu-id="0a945-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a945-172">OUTPUTS</span></span>

### <span data-ttu-id="0a945-173">Microsoft. Azure. Commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="0a945-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="0a945-174">Note</span><span class="sxs-lookup"><span data-stu-id="0a945-174">NOTES</span></span>

## <span data-ttu-id="0a945-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a945-175">RELATED LINKS</span></span>
