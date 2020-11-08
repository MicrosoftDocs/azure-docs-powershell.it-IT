---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: f0d8486bc26043ee4f2cb2126c7ffdc64829a7cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193298"
---
# <span data-ttu-id="304ab-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="304ab-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="304ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="304ab-102">SYNOPSIS</span></span>
<span data-ttu-id="304ab-103">Crea un'istanza del provider per l'abbonamento, il gruppo di risorse, il nome SapMonitor e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="304ab-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="304ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="304ab-104">SYNTAX</span></span>

### <span data-ttu-id="304ab-105">ByString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="304ab-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="304ab-106">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="304ab-106">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="304ab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="304ab-107">DESCRIPTION</span></span>
<span data-ttu-id="304ab-108">Crea un'istanza del provider per l'abbonamento, il gruppo di risorse, il nome SapMonitor e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="304ab-108">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="304ab-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="304ab-109">EXAMPLES</span></span>

### <span data-ttu-id="304ab-110">Esempio 1: creare un'istanza di SAP monitor by String per HANA</span><span class="sxs-lookup"><span data-stu-id="304ab-110">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="304ab-111">Questo comando crea un'istanza di SAP monitor by String per HANA.</span><span class="sxs-lookup"><span data-stu-id="304ab-111">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="304ab-112">Esempio 2: creare un'istanza di SAP monitor per Key Vault per HANA</span><span class="sxs-lookup"><span data-stu-id="304ab-112">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="304ab-113">Questo comando crea un'istanza di SAP monitor per Key Vault per HANA.</span><span class="sxs-lookup"><span data-stu-id="304ab-113">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

## <span data-ttu-id="304ab-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="304ab-114">PARAMETERS</span></span>

### <span data-ttu-id="304ab-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="304ab-115">-AsJob</span></span>
<span data-ttu-id="304ab-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="304ab-116">Run the command as a job</span></span>

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

### <span data-ttu-id="304ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304ab-117">-DefaultProfile</span></span>
<span data-ttu-id="304ab-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="304ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="304ab-119">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="304ab-119">-HanaDatabaseName</span></span>
<span data-ttu-id="304ab-120">Nome del database dell'istanza di SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="304ab-120">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304ab-121">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="304ab-121">-HanaDatabasePassword</span></span>
<span data-ttu-id="304ab-122">La password del database dell'istanza di SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="304ab-122">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="304ab-123">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="304ab-123">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="304ab-124">ID risorsa del Vault chiave che contiene le credenziali HANA.</span><span class="sxs-lookup"><span data-stu-id="304ab-124">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="304ab-125">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="304ab-125">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="304ab-126">Identificatore segreto per il segreto del Vault chiave che contiene le credenziali HANA.</span><span class="sxs-lookup"><span data-stu-id="304ab-126">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="304ab-127">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="304ab-127">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="304ab-128">La porta SQL del database dell'istanza di SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="304ab-128">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304ab-129">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="304ab-129">-HanaDatabaseUsername</span></span>
<span data-ttu-id="304ab-130">Nome utente del database dell'istanza di SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="304ab-130">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304ab-131">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="304ab-131">-HanaHostname</span></span>
<span data-ttu-id="304ab-132">Il nome host dell'istanza di SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="304ab-132">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="304ab-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="304ab-133">-Metadata</span></span>
<span data-ttu-id="304ab-134">Stringa JSON contenente metadati dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="304ab-134">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="304ab-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="304ab-135">-Name</span></span>
<span data-ttu-id="304ab-136">Nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="304ab-136">Name of the provider instance.</span></span>

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

### <span data-ttu-id="304ab-137">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="304ab-137">-NoWait</span></span>
<span data-ttu-id="304ab-138">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="304ab-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="304ab-139">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="304ab-139">-ProviderType</span></span>
<span data-ttu-id="304ab-140">Tipo di istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="304ab-140">The type of provider instance.</span></span>
<span data-ttu-id="304ab-141">I valori supportati sono: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="304ab-141">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="304ab-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="304ab-142">-ResourceGroupName</span></span>
<span data-ttu-id="304ab-143">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="304ab-143">Name of the resource group.</span></span>

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

### <span data-ttu-id="304ab-144">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="304ab-144">-SapMonitorName</span></span>
<span data-ttu-id="304ab-145">Nome della risorsa monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="304ab-145">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="304ab-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="304ab-146">-SubscriptionId</span></span>
<span data-ttu-id="304ab-147">ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="304ab-147">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="304ab-148">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="304ab-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="304ab-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="304ab-149">-Confirm</span></span>
<span data-ttu-id="304ab-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="304ab-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="304ab-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="304ab-151">-WhatIf</span></span>
<span data-ttu-id="304ab-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="304ab-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="304ab-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="304ab-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="304ab-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304ab-154">CommonParameters</span></span>
<span data-ttu-id="304ab-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="304ab-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304ab-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="304ab-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304ab-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="304ab-157">INPUTS</span></span>

## <span data-ttu-id="304ab-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="304ab-158">OUTPUTS</span></span>

### <span data-ttu-id="304ab-159">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="304ab-159">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="304ab-160">Note</span><span class="sxs-lookup"><span data-stu-id="304ab-160">NOTES</span></span>

<span data-ttu-id="304ab-161">ALIAS</span><span class="sxs-lookup"><span data-stu-id="304ab-161">ALIASES</span></span>

## <span data-ttu-id="304ab-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="304ab-162">RELATED LINKS</span></span>

