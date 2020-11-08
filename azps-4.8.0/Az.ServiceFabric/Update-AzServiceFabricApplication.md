---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: 779561ee3ff0a0b687104bd828890c314612f100
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191259"
---
# <span data-ttu-id="3c034-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3c034-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="3c034-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c034-102">SYNOPSIS</span></span>
<span data-ttu-id="3c034-103">Aggiornare un'applicazione fabric di servizi.</span><span class="sxs-lookup"><span data-stu-id="3c034-103">Update a service fabric application.</span></span> <span data-ttu-id="3c034-104">Questo consente di aggiornare i parametri dell'applicazione e/o aggiornare la versione del tipo di applicazione che attiverà un aggiornamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c034-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

## <span data-ttu-id="3c034-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c034-105">SYNTAX</span></span>

### <span data-ttu-id="3c034-106">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c034-106">ByResourceGroup (Default)</span></span>
```
Update-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-ForceRestart] [-UpgradeReplicaSetCheckTimeoutSec <Int32>]
 [-FailureAction <FailureAction>] [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c034-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c034-107">ByResourceId</span></span>
```
Update-AzServiceFabricApplication [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>]
 [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-ForceRestart]
 [-UpgradeReplicaSetCheckTimeoutSec <Int32>] [-FailureAction <FailureAction>]
 [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c034-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3c034-108">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c034-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c034-109">DESCRIPTION</span></span>
<span data-ttu-id="3c034-110">Questo cmdlet può essere usato per aggiornare i parametri dell'applicazione e aggiornare la versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c034-110">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="3c034-111">L'aggiornamento del parametro cambierà solo il modello in ARM Side, solo quando viene usata una nuova versione del tipo, il comando attiverà un aggiornamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c034-111">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="3c034-112">La versione del tipo specificata deve essere già creata nel cluster tramite **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="3c034-112">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="3c034-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c034-113">EXAMPLES</span></span>

### <span data-ttu-id="3c034-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3c034-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="3c034-115">Questo esempio avvia un'applicazione di aggiornamento per aggiornare la versione di tipo a "V2" creata con **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="3c034-115">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="3c034-116">I parametri dell'applicazione usati devono essere definiti nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c034-116">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="3c034-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3c034-117">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="3c034-118">Questo esempio aggiornerà il numero minimo e massimo di restrizioni dei nodi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c034-118">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="3c034-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3c034-119">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="3c034-120">Questo esempio avvia un'applicazione di aggiornamento per aggiornare la versione di tipo a "V2" e imposta anche alcuni parametri dei criteri di aggiornamento che avranno effetto dall'aggiornamento corrente.</span><span class="sxs-lookup"><span data-stu-id="3c034-120">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="3c034-121">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="3c034-121">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="3c034-122">Questo esempio aggiorna i parametri dell'applicazione, ma le modifiche avranno effetto solo fino all'aggiornamento della versione successiva all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c034-122">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="3c034-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c034-123">PARAMETERS</span></span>

### <span data-ttu-id="3c034-124">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="3c034-124">-ApplicationParameter</span></span>
<span data-ttu-id="3c034-125">Specificare i parametri dell'applicazione come coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="3c034-125">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="3c034-126">Questi parametri devono essere presenti nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c034-126">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-127">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3c034-127">-ApplicationTypeVersion</span></span>
<span data-ttu-id="3c034-128">Specificare la versione del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="3c034-128">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-129">-Clustername</span><span class="sxs-lookup"><span data-stu-id="3c034-129">-ClusterName</span></span>
<span data-ttu-id="3c034-130">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="3c034-130">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-131">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="3c034-131">-ConsiderWarningAsError</span></span>
<span data-ttu-id="3c034-132">Indica se trattare un evento di stato di avviso come evento di errore durante la valutazione dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="3c034-132">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c034-133">-DefaultProfile</span></span>
<span data-ttu-id="3c034-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c034-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c034-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="3c034-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="3c034-136">Specifica la percentuale massima di partizioni unhelthy per servizio consentite dai criteri di integrità per il tipo di servizio predefinito da usare per l'aggiornamento monitorato.</span><span class="sxs-lookup"><span data-stu-id="3c034-136">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="3c034-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="3c034-138">Specifica la percentuale massima di repliche unhelthy per servizio consentito dai criteri di integrità per il tipo di servizio predefinito da usare per l'aggiornamento monitorato.</span><span class="sxs-lookup"><span data-stu-id="3c034-138">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="3c034-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="3c034-140">Specifica la percentuale massima di servizi di unhelthy consentiti dai criteri di integrità per il tipo di servizio predefinito da usare per l'aggiornamento monitorato.</span><span class="sxs-lookup"><span data-stu-id="3c034-140">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-141">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="3c034-141">-FailureAction</span></span>
<span data-ttu-id="3c034-142">Specifica l'azione da eseguire se l'aggiornamento monitorato non riesce.</span><span class="sxs-lookup"><span data-stu-id="3c034-142">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="3c034-143">I valori accettabili per questo parametro sono rollback o Manual.</span><span class="sxs-lookup"><span data-stu-id="3c034-143">The acceptable values for this parameter are Rollback or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.FailureAction
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:
Accepted values: Rollback, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-144">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="3c034-144">-ForceRestart</span></span>
<span data-ttu-id="3c034-145">Indica che l'host del servizio viene riavviato anche se l'aggiornamento è una modifica di sola configurazione.</span><span class="sxs-lookup"><span data-stu-id="3c034-145">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-146">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3c034-146">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="3c034-147">Specifica la durata, in secondi, dopo la quale il tessuto di servizio ritenta il controllo integrità se il controllo integrità precedente non riesce.</span><span class="sxs-lookup"><span data-stu-id="3c034-147">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-148">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="3c034-148">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="3c034-149">Specifica la durata, in secondi, che il tessuto del servizio attende per verificare che l'applicazione sia stabile prima di passare al dominio di aggiornamento successivo o completare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3c034-149">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="3c034-150">Questa durata di attesa impedisce le modifiche non rilevate dell'integrità subito dopo l'esecuzione del controllo dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="3c034-150">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-151">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="3c034-151">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="3c034-152">Specifica la durata, in secondi, in cui il tessuto del servizio attende prima di eseguire il controllo integrità iniziale dopo il completamento dell'aggiornamento nel dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3c034-152">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c034-153">-InputObject</span></span>
<span data-ttu-id="3c034-154">Risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c034-154">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-155">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="3c034-155">-MaximumNodeCount</span></span>
<span data-ttu-id="3c034-156">Specifica il numero massimo di nodi in cui inserire un'applicazione</span><span class="sxs-lookup"><span data-stu-id="3c034-156">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-157">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="3c034-157">-MinimumNodeCount</span></span>
<span data-ttu-id="3c034-158">Specifica il numero minimo di nodi in cui il tessuto di servizio riserva la capacità per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="3c034-158">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c034-159">-Name</span></span>
<span data-ttu-id="3c034-160">Specificare il nome dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="3c034-160">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c034-161">-ResourceGroupName</span></span>
<span data-ttu-id="3c034-162">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c034-162">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-163">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c034-163">-ResourceId</span></span>
<span data-ttu-id="3c034-164">ARM ResourceId dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c034-164">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="3c034-165">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="3c034-165">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="3c034-166">Specifica la mappa dei criteri di integrità da usare per i diversi tipi di servizio come tabella hash con il formato seguente: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="3c034-166">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="3c034-167">Ad esempio: @ {"ServiceTypeName01" = "5, 10, 5"; "ServiceTypeName02" = "5; 5,5"}</span><span class="sxs-lookup"><span data-stu-id="3c034-167">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-168">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="3c034-168">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="3c034-169">Specifica la percentuale massima delle istanze dell'applicazione distribuite nei nodi del cluster che hanno uno stato di integrità di errore prima che lo stato di integrità dell'applicazione per il cluster sia un errore.</span><span class="sxs-lookup"><span data-stu-id="3c034-169">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-170">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3c034-170">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="3c034-171">Specifica il tempo massimo, in secondi, che il tessuto del servizio impiega per aggiornare un singolo dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3c034-171">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="3c034-172">Dopo questo periodo, l'aggiornamento non riesce.</span><span class="sxs-lookup"><span data-stu-id="3c034-172">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-173">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3c034-173">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="3c034-174">Specifica il tempo massimo in cui il tessuto del servizio attende che un servizio venga riconfigurato in uno stato sicuro, se non è già in stato di sicurezza, prima che il tessuto del servizio proceda all'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3c034-174">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-175">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3c034-175">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="3c034-176">Specifica il tempo massimo, in secondi, che il tessuto del servizio richiede per l'intero aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3c034-176">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="3c034-177">Dopo questo periodo, l'aggiornamento non riesce.</span><span class="sxs-lookup"><span data-stu-id="3c034-177">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c034-178">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c034-178">-Confirm</span></span>
<span data-ttu-id="3c034-179">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c034-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c034-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c034-180">-WhatIf</span></span>
<span data-ttu-id="3c034-181">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c034-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c034-182">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c034-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c034-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c034-183">CommonParameters</span></span>
<span data-ttu-id="3c034-184">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c034-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c034-185">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c034-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c034-186">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c034-186">INPUTS</span></span>

### <span data-ttu-id="3c034-187">System. String</span><span class="sxs-lookup"><span data-stu-id="3c034-187">System.String</span></span>

### <span data-ttu-id="3c034-188">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="3c034-188">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="3c034-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c034-189">OUTPUTS</span></span>

### <span data-ttu-id="3c034-190">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="3c034-190">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="3c034-191">Note</span><span class="sxs-lookup"><span data-stu-id="3c034-191">NOTES</span></span>

## <span data-ttu-id="3c034-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c034-192">RELATED LINKS</span></span>
