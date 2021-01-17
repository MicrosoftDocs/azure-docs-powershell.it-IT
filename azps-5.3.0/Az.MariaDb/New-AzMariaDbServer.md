---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476128"
---
# <span data-ttu-id="2192b-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="2192b-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="2192b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2192b-102">SYNOPSIS</span></span>
<span data-ttu-id="2192b-103">Crea un nuovo MariaDB.</span><span class="sxs-lookup"><span data-stu-id="2192b-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="2192b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2192b-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2192b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2192b-105">DESCRIPTION</span></span>
<span data-ttu-id="2192b-106">Crea un nuovo MariaDB.</span><span class="sxs-lookup"><span data-stu-id="2192b-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="2192b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2192b-107">EXAMPLES</span></span>

### <span data-ttu-id="2192b-108">Esempio 1: creare un nuovo MariaDB</span><span class="sxs-lookup"><span data-stu-id="2192b-108">Example 1: Create a new MariaDB</span></span>
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

<span data-ttu-id="2192b-109">Questo comando crea un nuovo MariaDB.</span><span class="sxs-lookup"><span data-stu-id="2192b-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="2192b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2192b-110">PARAMETERS</span></span>

### <span data-ttu-id="2192b-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="2192b-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="2192b-112">La password di amministratore deve essere SecureString.</span><span class="sxs-lookup"><span data-stu-id="2192b-112">Password of administrator, should be SecureString.</span></span>

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

### <span data-ttu-id="2192b-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="2192b-113">-AdministratorUsername</span></span>
<span data-ttu-id="2192b-114">Nome utente di Administrator.</span><span class="sxs-lookup"><span data-stu-id="2192b-114">Username of administrator.</span></span>

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

### <span data-ttu-id="2192b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2192b-115">-AsJob</span></span>
<span data-ttu-id="2192b-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="2192b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2192b-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="2192b-117">-BackupRetentionDay</span></span>
<span data-ttu-id="2192b-118">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="2192b-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="2192b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2192b-119">-DefaultProfile</span></span>
<span data-ttu-id="2192b-120">Region DefaultParameters le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2192b-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2192b-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="2192b-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="2192b-122">Abilitare il backup Geo-ridondante o meno per il server.</span><span class="sxs-lookup"><span data-stu-id="2192b-122">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="2192b-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2192b-123">-Location</span></span>
<span data-ttu-id="2192b-124">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2192b-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="2192b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2192b-125">-Name</span></span>
<span data-ttu-id="2192b-126">Nome del server MariaDB.</span><span class="sxs-lookup"><span data-stu-id="2192b-126">MariaDB server name.</span></span>

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

### <span data-ttu-id="2192b-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="2192b-127">-NoWait</span></span>
<span data-ttu-id="2192b-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="2192b-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2192b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2192b-129">-ResourceGroupName</span></span>
<span data-ttu-id="2192b-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2192b-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="2192b-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="2192b-131">-Sku</span></span>
<span data-ttu-id="2192b-132">Nome dell'USK, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="2192b-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="2192b-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="2192b-133">-SslEnforcement</span></span>
<span data-ttu-id="2192b-134">Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="2192b-134">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="2192b-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="2192b-135">-StorageAutogrow</span></span>
<span data-ttu-id="2192b-136">Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2192b-136">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="2192b-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="2192b-137">-StorageInMb</span></span>
<span data-ttu-id="2192b-138">Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="2192b-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="2192b-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2192b-139">-SubscriptionId</span></span>
<span data-ttu-id="2192b-140">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio</span><span class="sxs-lookup"><span data-stu-id="2192b-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="2192b-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="2192b-141">-Tag</span></span>
<span data-ttu-id="2192b-142">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="2192b-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="2192b-143">-Versione</span><span class="sxs-lookup"><span data-stu-id="2192b-143">-Version</span></span>
<span data-ttu-id="2192b-144">Versione del server.</span><span class="sxs-lookup"><span data-stu-id="2192b-144">Server version.</span></span>

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

### <span data-ttu-id="2192b-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2192b-145">-Confirm</span></span>
<span data-ttu-id="2192b-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2192b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2192b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2192b-147">-WhatIf</span></span>
<span data-ttu-id="2192b-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2192b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2192b-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2192b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2192b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2192b-150">CommonParameters</span></span>
<span data-ttu-id="2192b-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2192b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2192b-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2192b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2192b-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2192b-153">INPUTS</span></span>

## <span data-ttu-id="2192b-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2192b-154">OUTPUTS</span></span>

### <span data-ttu-id="2192b-155">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="2192b-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="2192b-156">Note</span><span class="sxs-lookup"><span data-stu-id="2192b-156">NOTES</span></span>

<span data-ttu-id="2192b-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2192b-157">ALIASES</span></span>

## <span data-ttu-id="2192b-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2192b-158">RELATED LINKS</span></span>

