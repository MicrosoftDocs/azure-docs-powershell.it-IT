---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e53ed405c9a03e7a9ec7a7c3694a44d513a1a1ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189079"
---
# <span data-ttu-id="01c6f-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="01c6f-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="01c6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="01c6f-103">Aggiornare un'applicazione di tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="01c6f-103">Update a service fabric application.</span></span> <span data-ttu-id="01c6f-104">In questo modo è possibile aggiornare i parametri dell'applicazione e/o aggiornare la versione del tipo di applicazione che attiverà un aggiornamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="01c6f-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="01c6f-105">Supporta solo ARM applicazioni distribuite.</span><span class="sxs-lookup"><span data-stu-id="01c6f-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="01c6f-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01c6f-106">SYNTAX</span></span>

### <span data-ttu-id="01c6f-107">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01c6f-107">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="01c6f-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="01c6f-108">ByResourceId</span></span>
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

### <span data-ttu-id="01c6f-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="01c6f-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c6f-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01c6f-110">DESCRIPTION</span></span>
<span data-ttu-id="01c6f-111">Questo cmdlet può essere usato per aggiornare i parametri dell'applicazione e la versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="01c6f-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="01c6f-112">L'aggiornamento del parametro modifica il modello solo ARM lato client, solo quando viene usata una nuova versione, il comando attiva l'aggiornamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="01c6f-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="01c6f-113">La versione del tipo specificata deve essere già creata nel cluster usando **New-AzServiceFabricApplicationTypeVersion.**</span><span class="sxs-lookup"><span data-stu-id="01c6f-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="01c6f-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01c6f-114">EXAMPLES</span></span>

### <span data-ttu-id="01c6f-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="01c6f-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="01c6f-116">Questo esempio avvia un aggiornamento dell'applicazione per aggiornare la versione del tipo a "v2", creata con **New-AzServiceFabricApplicationTypeVersion.**</span><span class="sxs-lookup"><span data-stu-id="01c6f-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="01c6f-117">I parametri dell'applicazione usati devono essere definiti nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="01c6f-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="01c6f-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="01c6f-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="01c6f-119">Questo esempio aggiornerà il numero minimo e massimo di restrizioni per i nodi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="01c6f-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="01c6f-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="01c6f-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="01c6f-121">Questo esempio avvia l'aggiornamento di un'applicazione per aggiornare la versione tipo a "v2" e imposta anche alcuni parametri dei criteri di aggiornamento che avranno effetto rispetto all'aggiornamento corrente.</span><span class="sxs-lookup"><span data-stu-id="01c6f-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="01c6f-122">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="01c6f-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="01c6f-123">Questo esempio aggiorna i parametri dell'applicazione, ma le modifiche verranno applicate solo fino alla versione successiva dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="01c6f-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="01c6f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01c6f-124">PARAMETERS</span></span>

### <span data-ttu-id="01c6f-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="01c6f-125">-ApplicationParameter</span></span>
<span data-ttu-id="01c6f-126">Specificare i parametri dell'applicazione come coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="01c6f-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="01c6f-127">Questi parametri devono essere presenti nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="01c6f-127">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="01c6f-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="01c6f-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="01c6f-129">Specificare la versione del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="01c6f-129">Specify the application type version</span></span>

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

### <span data-ttu-id="01c6f-130">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="01c6f-130">-ClusterName</span></span>
<span data-ttu-id="01c6f-131">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="01c6f-131">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="01c6f-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="01c6f-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="01c6f-133">Indica se considerare un evento di integrità di avviso come evento di errore durante la valutazione dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="01c6f-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="01c6f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c6f-134">-DefaultProfile</span></span>
<span data-ttu-id="01c6f-135">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01c6f-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01c6f-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="01c6f-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="01c6f-137">Specifica la percentuale massima di partizioni non erre per servizio consentite dai criteri di integrità per il tipo di servizio predefinito da usare per l'aggiornamento monitorato.</span><span class="sxs-lookup"><span data-stu-id="01c6f-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="01c6f-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="01c6f-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="01c6f-139">Specifica la percentuale massima di replica nonhelthy per servizio consentita dai criteri di integrità per il tipo di servizio predefinito da usare per l'aggiornamento monitorato.</span><span class="sxs-lookup"><span data-stu-id="01c6f-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="01c6f-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="01c6f-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="01c6f-141">Specifica la percentuale massima di servizi non provati consentiti dai criteri di integrità per il tipo di servizio predefinito da usare per l'aggiornamento monitorato.</span><span class="sxs-lookup"><span data-stu-id="01c6f-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="01c6f-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="01c6f-142">-FailureAction</span></span>
<span data-ttu-id="01c6f-143">Specifica l'azione da eseguire se l'aggiornamento monitorato non riesce.</span><span class="sxs-lookup"><span data-stu-id="01c6f-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="01c6f-144">I valori accettabili per questo parametro sono Rollback o Manuale.</span><span class="sxs-lookup"><span data-stu-id="01c6f-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="01c6f-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="01c6f-145">-ForceRestart</span></span>
<span data-ttu-id="01c6f-146">Indica che l'host del servizio viene riavviato anche se l'aggiornamento è una modifica di sola configurazione.</span><span class="sxs-lookup"><span data-stu-id="01c6f-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="01c6f-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="01c6f-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="01c6f-148">Specifica la durata, in secondi, dopo la quale Tessuto di servizio deve eseguire la verifica dell'integrità se la verifica dell'integrità precedente non riesce.</span><span class="sxs-lookup"><span data-stu-id="01c6f-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="01c6f-149">-HealthCheckstableDurationSec</span><span class="sxs-lookup"><span data-stu-id="01c6f-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="01c6f-150">Specifica la durata, in secondi, che Service Fabric attende per verificare che l'applicazione sia stabile prima di passare al dominio di aggiornamento successivo o di completare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="01c6f-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="01c6f-151">Questa durata di attesa impedisce modifiche non rilevate dell'integrità subito dopo l'esecuzione della verifica dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="01c6f-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="01c6f-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="01c6f-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="01c6f-153">Specifica la durata, in secondi, che Service Fabric attende prima di eseguire la verifica dell'integrità iniziale al termine dell'aggiornamento nel dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="01c6f-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="01c6f-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01c6f-154">-InputObject</span></span>
<span data-ttu-id="01c6f-155">Risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="01c6f-155">The application resource.</span></span>

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

### <span data-ttu-id="01c6f-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="01c6f-156">-MaximumNodeCount</span></span>
<span data-ttu-id="01c6f-157">Specifica il numero massimo di nodi in cui inserire un'applicazione</span><span class="sxs-lookup"><span data-stu-id="01c6f-157">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="01c6f-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="01c6f-158">-MinimumNodeCount</span></span>
<span data-ttu-id="01c6f-159">Specifica il numero minimo di nodi in cui Service Fabric riserva la capacità per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="01c6f-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="01c6f-160">-Name</span><span class="sxs-lookup"><span data-stu-id="01c6f-160">-Name</span></span>
<span data-ttu-id="01c6f-161">Specificare il nome dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="01c6f-161">Specify the name of the application</span></span>

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

### <span data-ttu-id="01c6f-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c6f-162">-ResourceGroupName</span></span>
<span data-ttu-id="01c6f-163">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="01c6f-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="01c6f-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01c6f-164">-ResourceId</span></span>
<span data-ttu-id="01c6f-165">Arm ResourceId dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="01c6f-165">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="01c6f-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="01c6f-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="01c6f-167">Specifica la mappa dei criteri di integrità da usare per diversi tipi di servizio come tabella hash nel formato seguente: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="01c6f-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="01c6f-168">Ad esempio: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span><span class="sxs-lookup"><span data-stu-id="01c6f-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="01c6f-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="01c6f-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="01c6f-170">Specifica la percentuale massima di istanze dell'applicazione distribuite nei nodi nel cluster con lo stato di errore prima dell'errore dello stato di integrità dell'applicazione per il cluster.</span><span class="sxs-lookup"><span data-stu-id="01c6f-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="01c6f-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="01c6f-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="01c6f-172">Specifica il tempo massimo, in secondi, necessario a Service Fabric per aggiornare un singolo dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="01c6f-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="01c6f-173">Al termine di questo periodo, l'aggiornamento non riesce.</span><span class="sxs-lookup"><span data-stu-id="01c6f-173">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="01c6f-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="01c6f-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="01c6f-175">Specifica il tempo massimo di attesa di un servizio per la riconfigurazione in uno stato sicuro, se non è già in uno stato sicuro, prima che Service Fabric proceda con l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="01c6f-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="01c6f-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="01c6f-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="01c6f-177">Specifica il tempo massimo, in secondi, necessario a Service Fabric per l'intero aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="01c6f-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="01c6f-178">Al termine di questo periodo, l'aggiornamento non riesce.</span><span class="sxs-lookup"><span data-stu-id="01c6f-178">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="01c6f-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01c6f-179">-Confirm</span></span>
<span data-ttu-id="01c6f-180">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01c6f-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c6f-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c6f-181">-WhatIf</span></span>
<span data-ttu-id="01c6f-182">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01c6f-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c6f-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01c6f-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c6f-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c6f-184">CommonParameters</span></span>
<span data-ttu-id="01c6f-185">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c6f-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c6f-186">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01c6f-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c6f-187">INPUT</span><span class="sxs-lookup"><span data-stu-id="01c6f-187">INPUTS</span></span>

### <span data-ttu-id="01c6f-188">System.String</span><span class="sxs-lookup"><span data-stu-id="01c6f-188">System.String</span></span>

### <span data-ttu-id="01c6f-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="01c6f-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="01c6f-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01c6f-190">OUTPUTS</span></span>

### <span data-ttu-id="01c6f-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="01c6f-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="01c6f-192">NOTE</span><span class="sxs-lookup"><span data-stu-id="01c6f-192">NOTES</span></span>

## <span data-ttu-id="01c6f-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01c6f-193">RELATED LINKS</span></span>
