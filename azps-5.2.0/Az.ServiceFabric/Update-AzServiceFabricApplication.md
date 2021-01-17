---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e53ed405c9a03e7a9ec7a7c3694a44d513a1a1ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343324"
---
# <span data-ttu-id="0ab54-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0ab54-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="0ab54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ab54-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab54-103">Aggiornare un'applicazione fabric di servizi.</span><span class="sxs-lookup"><span data-stu-id="0ab54-103">Update a service fabric application.</span></span> <span data-ttu-id="0ab54-104">Questo consente di aggiornare i parametri dell'applicazione e/o aggiornare la versione del tipo di applicazione che attiverà un aggiornamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ab54-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="0ab54-105">Supporta solo le applicazioni distribuite ARM.</span><span class="sxs-lookup"><span data-stu-id="0ab54-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="0ab54-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ab54-106">SYNTAX</span></span>

### <span data-ttu-id="0ab54-107">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0ab54-107">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="0ab54-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ab54-108">ByResourceId</span></span>
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

### <span data-ttu-id="0ab54-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0ab54-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ab54-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ab54-110">DESCRIPTION</span></span>
<span data-ttu-id="0ab54-111">Questo cmdlet può essere usato per aggiornare i parametri dell'applicazione e aggiornare la versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ab54-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="0ab54-112">L'aggiornamento del parametro cambierà solo il modello in ARM Side, solo quando viene usata una nuova versione del tipo, il comando attiverà un aggiornamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ab54-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="0ab54-113">La versione del tipo specificata deve essere già creata nel cluster tramite **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="0ab54-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="0ab54-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ab54-114">EXAMPLES</span></span>

### <span data-ttu-id="0ab54-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0ab54-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="0ab54-116">Questo esempio avvia un'applicazione di aggiornamento per aggiornare la versione di tipo a "V2" creata con **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="0ab54-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="0ab54-117">I parametri dell'applicazione usati devono essere definiti nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ab54-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="0ab54-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0ab54-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="0ab54-119">Questo esempio aggiornerà il numero minimo e massimo di restrizioni dei nodi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ab54-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="0ab54-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0ab54-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="0ab54-121">Questo esempio avvia un'applicazione di aggiornamento per aggiornare la versione di tipo a "V2" e imposta anche alcuni parametri dei criteri di aggiornamento che avranno effetto dall'aggiornamento corrente.</span><span class="sxs-lookup"><span data-stu-id="0ab54-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="0ab54-122">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="0ab54-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="0ab54-123">Questo esempio aggiorna i parametri dell'applicazione, ma le modifiche avranno effetto solo fino all'aggiornamento della versione successiva all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ab54-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="0ab54-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ab54-124">PARAMETERS</span></span>

### <span data-ttu-id="0ab54-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="0ab54-125">-ApplicationParameter</span></span>
<span data-ttu-id="0ab54-126">Specificare i parametri dell'applicazione come coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="0ab54-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="0ab54-127">Questi parametri devono essere presenti nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ab54-127">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="0ab54-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0ab54-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="0ab54-129">Specificare la versione del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="0ab54-129">Specify the application type version</span></span>

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

### <span data-ttu-id="0ab54-130">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0ab54-130">-ClusterName</span></span>
<span data-ttu-id="0ab54-131">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="0ab54-131">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0ab54-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="0ab54-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="0ab54-133">Indica se trattare un evento di stato di avviso come evento di errore durante la valutazione dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="0ab54-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="0ab54-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab54-134">-DefaultProfile</span></span>
<span data-ttu-id="0ab54-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab54-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ab54-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="0ab54-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="0ab54-137">Specifica la percentuale massima di partizioni unhelthy per servizio consentite dai criteri di integrità per il tipo di servizio predefinito da usare per l'aggiornamento monitorato.</span><span class="sxs-lookup"><span data-stu-id="0ab54-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="0ab54-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="0ab54-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="0ab54-139">Specifica la percentuale massima di repliche unhelthy per servizio consentito dai criteri di integrità per il tipo di servizio predefinito da usare per l'aggiornamento monitorato.</span><span class="sxs-lookup"><span data-stu-id="0ab54-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="0ab54-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="0ab54-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="0ab54-141">Specifica la percentuale massima di servizi di unhelthy consentiti dai criteri di integrità per il tipo di servizio predefinito da usare per l'aggiornamento monitorato.</span><span class="sxs-lookup"><span data-stu-id="0ab54-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="0ab54-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="0ab54-142">-FailureAction</span></span>
<span data-ttu-id="0ab54-143">Specifica l'azione da eseguire se l'aggiornamento monitorato non riesce.</span><span class="sxs-lookup"><span data-stu-id="0ab54-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="0ab54-144">I valori accettabili per questo parametro sono rollback o Manual.</span><span class="sxs-lookup"><span data-stu-id="0ab54-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="0ab54-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="0ab54-145">-ForceRestart</span></span>
<span data-ttu-id="0ab54-146">Indica che l'host del servizio viene riavviato anche se l'aggiornamento è una modifica di sola configurazione.</span><span class="sxs-lookup"><span data-stu-id="0ab54-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="0ab54-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="0ab54-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="0ab54-148">Specifica la durata, in secondi, dopo la quale il tessuto di servizio ritenta il controllo integrità se il controllo integrità precedente non riesce.</span><span class="sxs-lookup"><span data-stu-id="0ab54-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="0ab54-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="0ab54-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="0ab54-150">Specifica la durata, in secondi, che il tessuto del servizio attende per verificare che l'applicazione sia stabile prima di passare al dominio di aggiornamento successivo o completare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0ab54-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="0ab54-151">Questa durata di attesa impedisce le modifiche non rilevate dell'integrità subito dopo l'esecuzione del controllo dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="0ab54-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="0ab54-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="0ab54-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="0ab54-153">Specifica la durata, in secondi, in cui il tessuto del servizio attende prima di eseguire il controllo integrità iniziale dopo il completamento dell'aggiornamento nel dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0ab54-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="0ab54-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ab54-154">-InputObject</span></span>
<span data-ttu-id="0ab54-155">Risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ab54-155">The application resource.</span></span>

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

### <span data-ttu-id="0ab54-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="0ab54-156">-MaximumNodeCount</span></span>
<span data-ttu-id="0ab54-157">Specifica il numero massimo di nodi in cui inserire un'applicazione</span><span class="sxs-lookup"><span data-stu-id="0ab54-157">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="0ab54-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="0ab54-158">-MinimumNodeCount</span></span>
<span data-ttu-id="0ab54-159">Specifica il numero minimo di nodi in cui il tessuto di servizio riserva la capacità per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="0ab54-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="0ab54-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ab54-160">-Name</span></span>
<span data-ttu-id="0ab54-161">Specificare il nome dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="0ab54-161">Specify the name of the application</span></span>

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

### <span data-ttu-id="0ab54-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ab54-162">-ResourceGroupName</span></span>
<span data-ttu-id="0ab54-163">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ab54-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0ab54-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ab54-164">-ResourceId</span></span>
<span data-ttu-id="0ab54-165">ARM ResourceId dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0ab54-165">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="0ab54-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="0ab54-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="0ab54-167">Specifica la mappa dei criteri di integrità da usare per i diversi tipi di servizio come tabella hash con il formato seguente: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="0ab54-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="0ab54-168">Ad esempio: @ {"ServiceTypeName01" = "5, 10, 5"; "ServiceTypeName02" = "5; 5,5"}</span><span class="sxs-lookup"><span data-stu-id="0ab54-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="0ab54-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="0ab54-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="0ab54-170">Specifica la percentuale massima delle istanze dell'applicazione distribuite nei nodi del cluster che hanno uno stato di integrità di errore prima che lo stato di integrità dell'applicazione per il cluster sia un errore.</span><span class="sxs-lookup"><span data-stu-id="0ab54-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="0ab54-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="0ab54-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="0ab54-172">Specifica il tempo massimo, in secondi, che il tessuto del servizio impiega per aggiornare un singolo dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0ab54-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="0ab54-173">Dopo questo periodo, l'aggiornamento non riesce.</span><span class="sxs-lookup"><span data-stu-id="0ab54-173">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="0ab54-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="0ab54-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="0ab54-175">Specifica il tempo massimo in cui il tessuto del servizio attende che un servizio venga riconfigurato in uno stato sicuro, se non è già in stato di sicurezza, prima che il tessuto del servizio proceda all'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0ab54-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="0ab54-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="0ab54-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="0ab54-177">Specifica il tempo massimo, in secondi, che il tessuto del servizio richiede per l'intero aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0ab54-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="0ab54-178">Dopo questo periodo, l'aggiornamento non riesce.</span><span class="sxs-lookup"><span data-stu-id="0ab54-178">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="0ab54-179">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ab54-179">-Confirm</span></span>
<span data-ttu-id="0ab54-180">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ab54-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ab54-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ab54-181">-WhatIf</span></span>
<span data-ttu-id="0ab54-182">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ab54-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ab54-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ab54-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ab54-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab54-184">CommonParameters</span></span>
<span data-ttu-id="0ab54-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab54-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab54-186">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ab54-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab54-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ab54-187">INPUTS</span></span>

### <span data-ttu-id="0ab54-188">System. String</span><span class="sxs-lookup"><span data-stu-id="0ab54-188">System.String</span></span>

### <span data-ttu-id="0ab54-189">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="0ab54-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="0ab54-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ab54-190">OUTPUTS</span></span>

### <span data-ttu-id="0ab54-191">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="0ab54-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="0ab54-192">Note</span><span class="sxs-lookup"><span data-stu-id="0ab54-192">NOTES</span></span>

## <span data-ttu-id="0ab54-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ab54-193">RELATED LINKS</span></span>
