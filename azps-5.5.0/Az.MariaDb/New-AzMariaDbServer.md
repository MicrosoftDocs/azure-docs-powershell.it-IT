---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207187"
---
# <span data-ttu-id="cf615-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="cf615-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="cf615-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf615-102">SYNOPSIS</span></span>
<span data-ttu-id="cf615-103">Crea una nuova mariaDB.</span><span class="sxs-lookup"><span data-stu-id="cf615-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="cf615-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf615-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf615-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cf615-105">DESCRIPTION</span></span>
<span data-ttu-id="cf615-106">Crea una nuova mariaDB.</span><span class="sxs-lookup"><span data-stu-id="cf615-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="cf615-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf615-107">EXAMPLES</span></span>

### <span data-ttu-id="cf615-108">Esempio 1: Creare un nuovo database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="cf615-108">Example 1: Create a new MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbServer -Name mariadb-aassd-01 -ResourceGroupName lucas-manual-test -Sku 'B_Gen5_1' -Location eastus
cmdlet New-AzMariaDbServer at command pipeline position 1
Supply values for the following parameters:
AdministratorUsername: adminuser
AdministratorLoginPassword: ************

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----             -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-aassd-01 eastus   adminuser          10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="cf615-109">Questo comando crea una nuova mariadb.</span><span class="sxs-lookup"><span data-stu-id="cf615-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="cf615-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf615-110">PARAMETERS</span></span>

### <span data-ttu-id="cf615-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="cf615-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="cf615-112">La password di amministratore dovrebbe essere SecureString.</span><span class="sxs-lookup"><span data-stu-id="cf615-112">Password of administrator, should be SecureString.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf615-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="cf615-113">-AdministratorUsername</span></span>
<span data-ttu-id="cf615-114">Nome utente dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="cf615-114">Username of administrator.</span></span>

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

### <span data-ttu-id="cf615-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf615-115">-AsJob</span></span>
<span data-ttu-id="cf615-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="cf615-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cf615-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="cf615-117">-BackupRetentionDay</span></span>
<span data-ttu-id="cf615-118">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="cf615-118">Backup retention days for the server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf615-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf615-119">-DefaultProfile</span></span>
<span data-ttu-id="cf615-120">region DefaultParameters Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf615-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf615-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="cf615-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="cf615-122">Abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="cf615-122">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf615-123">-Location</span><span class="sxs-lookup"><span data-stu-id="cf615-123">-Location</span></span>
<span data-ttu-id="cf615-124">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cf615-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="cf615-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cf615-125">-Name</span></span>
<span data-ttu-id="cf615-126">Nome del server MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cf615-126">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf615-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cf615-127">-NoWait</span></span>
<span data-ttu-id="cf615-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="cf615-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cf615-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf615-129">-ResourceGroupName</span></span>
<span data-ttu-id="cf615-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cf615-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="cf615-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="cf615-131">-Sku</span></span>
<span data-ttu-id="cf615-132">Il nome della sKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cf615-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="cf615-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="cf615-133">-SslEnforcement</span></span>
<span data-ttu-id="cf615-134">Abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="cf615-134">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf615-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="cf615-135">-StorageAutogrow</span></span>
<span data-ttu-id="cf615-136">Abilitare l'estensione automatica dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cf615-136">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf615-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="cf615-137">-StorageInMb</span></span>
<span data-ttu-id="cf615-138">Spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="cf615-138">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf615-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf615-139">-SubscriptionId</span></span>
<span data-ttu-id="cf615-140">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio</span><span class="sxs-lookup"><span data-stu-id="cf615-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="cf615-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="cf615-141">-Tag</span></span>
<span data-ttu-id="cf615-142">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="cf615-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="cf615-143">-Version</span><span class="sxs-lookup"><span data-stu-id="cf615-143">-Version</span></span>
<span data-ttu-id="cf615-144">Versione del server.</span><span class="sxs-lookup"><span data-stu-id="cf615-144">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf615-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf615-145">-Confirm</span></span>
<span data-ttu-id="cf615-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf615-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf615-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf615-147">-WhatIf</span></span>
<span data-ttu-id="cf615-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf615-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf615-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf615-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf615-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf615-150">CommonParameters</span></span>
<span data-ttu-id="cf615-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf615-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf615-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cf615-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf615-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="cf615-153">INPUTS</span></span>

## <span data-ttu-id="cf615-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf615-154">OUTPUTS</span></span>

### <span data-ttu-id="cf615-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="cf615-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="cf615-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="cf615-156">NOTES</span></span>

<span data-ttu-id="cf615-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cf615-157">ALIASES</span></span>

## <span data-ttu-id="cf615-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf615-158">RELATED LINKS</span></span>

