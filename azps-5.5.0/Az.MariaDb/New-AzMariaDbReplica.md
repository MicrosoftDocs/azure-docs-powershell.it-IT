---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185127"
---
# <span data-ttu-id="12446-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="12446-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="12446-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12446-102">SYNOPSIS</span></span>
<span data-ttu-id="12446-103">Crea una replica di un server MariaDB.</span><span class="sxs-lookup"><span data-stu-id="12446-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="12446-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12446-104">SYNTAX</span></span>

### <span data-ttu-id="12446-105">ServerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12446-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12446-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="12446-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="12446-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="12446-107">DESCRIPTION</span></span>
<span data-ttu-id="12446-108">Crea una replica di un server MariaDB.</span><span class="sxs-lookup"><span data-stu-id="12446-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="12446-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12446-109">EXAMPLES</span></span>

### <span data-ttu-id="12446-110">Esempio 1: Creare un db replica per un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="12446-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="12446-111">Questo comando crea un db replica per un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="12446-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="12446-112">Esempio 2: Creare un db replica per un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="12446-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="12446-113">Questo comando crea un db replica per un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="12446-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="12446-114">Esempio 3: Creare un db replica per un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="12446-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="12446-115">Questo comando con il parametro inputobject crea un db replica con il parametro inputobject per un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="12446-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="12446-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12446-116">PARAMETERS</span></span>

### <span data-ttu-id="12446-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12446-117">-AsJob</span></span>
<span data-ttu-id="12446-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="12446-118">Run the command as a job</span></span>

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

### <span data-ttu-id="12446-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12446-119">-DefaultProfile</span></span>
<span data-ttu-id="12446-120">region DefaultParameters Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="12446-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12446-121">-Location</span><span class="sxs-lookup"><span data-stu-id="12446-121">-Location</span></span>
<span data-ttu-id="12446-122">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="12446-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="12446-123">-Master</span><span class="sxs-lookup"><span data-stu-id="12446-123">-Master</span></span>
<span data-ttu-id="12446-124">Oggetto server di origine da cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="12446-124">The source server object to restore from.</span></span>
<span data-ttu-id="12446-125">Per creare, vedere la sezione NOTE relativa alle proprietà MASTER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="12446-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12446-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="12446-126">-MasterName</span></span>
<span data-ttu-id="12446-127">Nome del server MariaDB.</span><span class="sxs-lookup"><span data-stu-id="12446-127">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12446-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="12446-128">-NoWait</span></span>
<span data-ttu-id="12446-129">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="12446-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="12446-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="12446-130">-ReplicaName</span></span>
<span data-ttu-id="12446-131">Nome replica.</span><span class="sxs-lookup"><span data-stu-id="12446-131">Replica name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12446-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12446-132">-ResourceGroupName</span></span>
<span data-ttu-id="12446-133">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="12446-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12446-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="12446-134">-Sku</span></span>
<span data-ttu-id="12446-135">Il nome della sKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="12446-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="12446-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12446-136">-SubscriptionId</span></span>
<span data-ttu-id="12446-137">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="12446-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="12446-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="12446-138">-Tag</span></span>
<span data-ttu-id="12446-139">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="12446-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="12446-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12446-140">-Confirm</span></span>
<span data-ttu-id="12446-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12446-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12446-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12446-142">-WhatIf</span></span>
<span data-ttu-id="12446-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12446-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12446-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12446-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12446-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12446-145">CommonParameters</span></span>
<span data-ttu-id="12446-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12446-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12446-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="12446-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12446-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="12446-148">INPUTS</span></span>

### <span data-ttu-id="12446-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="12446-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="12446-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12446-150">OUTPUTS</span></span>

### <span data-ttu-id="12446-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="12446-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="12446-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="12446-152">NOTES</span></span>

<span data-ttu-id="12446-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="12446-153">ALIASES</span></span>

<span data-ttu-id="12446-154">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="12446-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12446-155">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="12446-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12446-156">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12446-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12446-157">MASTER: <IServer> oggetto server di origine da cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="12446-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="12446-158">`Location <String>`: la posizione in cui risiede la risorsa.</span><span class="sxs-lookup"><span data-stu-id="12446-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="12446-159">`[Tag <ITrackedResourceTags>]`: metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="12446-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="12446-160">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="12446-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="12446-161">`[AdministratorLogin <String>]`: nome di accesso di un server da parte dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="12446-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="12446-162">Può essere specificato solo durante la creazione del server (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="12446-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="12446-163">`[EarliestRestoreDate <DateTime?>]`: il primo momento di creazione del punto di ripristino (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="12446-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="12446-164">`[FullyQualifiedDomainName <String>]`: nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="12446-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="12446-165">`[IdentityType <IdentityType?>]`: tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="12446-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="12446-166">Impostare questo valore su "SystemAssigned" per creare e assegnare automaticamente un'entità Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="12446-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="12446-167">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="12446-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="12446-168">`[ReplicaCapacity <Int32?>]`: numero massimo di replica consentite a un server master.</span><span class="sxs-lookup"><span data-stu-id="12446-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="12446-169">`[ReplicationRole <String>]`: ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="12446-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="12446-170">`[SkuCapacity <Int32?>]`: la capacità di scalabilità in orizzontale, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="12446-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="12446-171">`[SkuFamily <String>]`: famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="12446-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="12446-172">`[SkuName <String>]`: il nome della SKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="12446-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="12446-173">`[SkuSize <String>]`: il codice delle dimensioni, che deve essere interpretato dalla risorsa nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="12446-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="12446-174">`[SkuTier <SkuTier?>]`: il livello dello specifico SKU, ad esempio Di base.</span><span class="sxs-lookup"><span data-stu-id="12446-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="12446-175">`[SslEnforcement <SslEnforcementEnum?>]`: per abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="12446-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="12446-176">`[StorageProfileBackupRetentionDay <Int32?>]`: giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="12446-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="12446-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="12446-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="12446-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: per abilitare l'estensione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="12446-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="12446-179">`[StorageProfileStorageMb <Int32?>]`: spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="12446-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="12446-180">`[UserVisibleState <ServerState?>]`: stato di un server visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="12446-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="12446-181">`[Version <ServerVersion?>]`: versione del server.</span><span class="sxs-lookup"><span data-stu-id="12446-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="12446-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12446-182">RELATED LINKS</span></span>

