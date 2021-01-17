---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: c9ba83218e8be82716f4804444b7c52371fe764c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476225"
---
# <span data-ttu-id="58fcc-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="58fcc-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="58fcc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="58fcc-103">Crea un'istanza del provider per l'abbonamento, il gruppo di risorse, il nome SapMonitor e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="58fcc-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="58fcc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58fcc-104">SYNTAX</span></span>

### <span data-ttu-id="58fcc-105">ByString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58fcc-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="58fcc-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="58fcc-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="58fcc-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="58fcc-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="58fcc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58fcc-108">DESCRIPTION</span></span>
<span data-ttu-id="58fcc-109">Crea un'istanza del provider per l'abbonamento, il gruppo di risorse, il nome SapMonitor e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="58fcc-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="58fcc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58fcc-110">EXAMPLES</span></span>

### <span data-ttu-id="58fcc-111">Esempio 1: creare un'istanza di SAP monitor by String per HANA</span><span class="sxs-lookup"><span data-stu-id="58fcc-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="58fcc-112">Questo comando crea un'istanza di SAP monitor by String per HANA.</span><span class="sxs-lookup"><span data-stu-id="58fcc-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="58fcc-113">Esempio 2: creare un'istanza di SAP monitor per Key Vault per HANA</span><span class="sxs-lookup"><span data-stu-id="58fcc-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="58fcc-114">Questo comando crea un'istanza di SAP monitor per Key Vault per HANA.</span><span class="sxs-lookup"><span data-stu-id="58fcc-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="58fcc-115">Esempio 3: creare un'istanza di SAP monitor by Dictionary for PrometheusHaCluster</span><span class="sxs-lookup"><span data-stu-id="58fcc-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="58fcc-116">Questo comando crea un'istanza di SAP monitor by Dictionary for PrometheusHaCluster.</span><span class="sxs-lookup"><span data-stu-id="58fcc-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="58fcc-117">Esempio 4: creare un'istanza di SAP monitor by Dictionary for Prometeoos</span><span class="sxs-lookup"><span data-stu-id="58fcc-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="58fcc-118">Questo comando crea un'istanza di SAP monitor by Dictionary for Prometeoos.</span><span class="sxs-lookup"><span data-stu-id="58fcc-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="58fcc-119">Esempio 5: creare un'istanza di SAP monitor by Dictionary for MsSqlServer</span><span class="sxs-lookup"><span data-stu-id="58fcc-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="58fcc-120">Questo comando crea un'istanza di SAP monitor by Dictionary for MsSqlServer.</span><span class="sxs-lookup"><span data-stu-id="58fcc-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="58fcc-121">Esempio 6: creare un'istanza di SAP monitor by Dictionary for SapHana</span><span class="sxs-lookup"><span data-stu-id="58fcc-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="58fcc-122">Questo comando crea un'istanza di SAP monitor by Dictionary for SapHana.</span><span class="sxs-lookup"><span data-stu-id="58fcc-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="58fcc-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58fcc-123">PARAMETERS</span></span>

### <span data-ttu-id="58fcc-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58fcc-124">-AsJob</span></span>
<span data-ttu-id="58fcc-125">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="58fcc-125">Run the command as a job</span></span>

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

### <span data-ttu-id="58fcc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58fcc-126">-DefaultProfile</span></span>
<span data-ttu-id="58fcc-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58fcc-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="58fcc-128">-HanaDatabaseName</span></span>
<span data-ttu-id="58fcc-129">Nome del database dell'istanza di SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="58fcc-129">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="58fcc-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="58fcc-131">La password del database dell'istanza di SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="58fcc-131">The password of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByString
Aliases: HanaDbPassword

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="58fcc-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="58fcc-133">ID risorsa del Vault chiave che contiene le credenziali HANA.</span><span class="sxs-lookup"><span data-stu-id="58fcc-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordKeyVaultId, KeyVaultId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="58fcc-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="58fcc-135">Identificatore segreto per il segreto del Vault chiave che contiene le credenziali HANA.</span><span class="sxs-lookup"><span data-stu-id="58fcc-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordSecretId, SecretId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="58fcc-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="58fcc-137">La porta SQL del database dell'istanza di SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="58fcc-137">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="58fcc-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="58fcc-139">Nome utente del database dell'istanza di SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="58fcc-139">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="58fcc-140">-HanaHostname</span></span>
<span data-ttu-id="58fcc-141">Il nome host dell'istanza di SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="58fcc-141">The hostname of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="58fcc-142">-InstanceProperty</span></span>
<span data-ttu-id="58fcc-143">Proprietà dell'istanza di HANA.</span><span class="sxs-lookup"><span data-stu-id="58fcc-143">The property of HANA instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByDict
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="58fcc-144">-Metadata</span></span>
<span data-ttu-id="58fcc-145">Stringa JSON contenente metadati dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="58fcc-145">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="58fcc-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="58fcc-146">-Name</span></span>
<span data-ttu-id="58fcc-147">Nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="58fcc-147">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-148">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="58fcc-148">-NoWait</span></span>
<span data-ttu-id="58fcc-149">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="58fcc-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="58fcc-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="58fcc-150">-ProviderType</span></span>
<span data-ttu-id="58fcc-151">Tipo di istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="58fcc-151">The type of provider instance.</span></span>
<span data-ttu-id="58fcc-152">I valori supportati sono: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="58fcc-152">Supported values are: "SapHana".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58fcc-153">-ResourceGroupName</span></span>
<span data-ttu-id="58fcc-154">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58fcc-154">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="58fcc-155">-SapMonitorName</span></span>
<span data-ttu-id="58fcc-156">Nome della risorsa monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="58fcc-156">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58fcc-157">-SubscriptionId</span></span>
<span data-ttu-id="58fcc-158">ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="58fcc-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="58fcc-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="58fcc-159">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fcc-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="58fcc-160">-Confirm</span></span>
<span data-ttu-id="58fcc-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58fcc-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58fcc-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58fcc-162">-WhatIf</span></span>
<span data-ttu-id="58fcc-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58fcc-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58fcc-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58fcc-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58fcc-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58fcc-165">CommonParameters</span></span>
<span data-ttu-id="58fcc-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58fcc-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58fcc-167">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58fcc-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58fcc-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58fcc-168">INPUTS</span></span>

## <span data-ttu-id="58fcc-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58fcc-169">OUTPUTS</span></span>

### <span data-ttu-id="58fcc-170">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="58fcc-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="58fcc-171">Note</span><span class="sxs-lookup"><span data-stu-id="58fcc-171">NOTES</span></span>

<span data-ttu-id="58fcc-172">ALIAS</span><span class="sxs-lookup"><span data-stu-id="58fcc-172">ALIASES</span></span>

## <span data-ttu-id="58fcc-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58fcc-173">RELATED LINKS</span></span>

