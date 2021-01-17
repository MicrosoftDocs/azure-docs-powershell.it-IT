---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351124"
---
# <span data-ttu-id="c1eed-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="c1eed-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="c1eed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1eed-102">SYNOPSIS</span></span>
<span data-ttu-id="c1eed-103">Crea una replica di un server MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c1eed-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="c1eed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1eed-104">SYNTAX</span></span>

### <span data-ttu-id="c1eed-105">Nomeserver (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1eed-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c1eed-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="c1eed-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c1eed-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1eed-107">DESCRIPTION</span></span>
<span data-ttu-id="c1eed-108">Crea una replica di un server MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c1eed-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="c1eed-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1eed-109">EXAMPLES</span></span>

### <span data-ttu-id="c1eed-110">Esempio 1: creare un DB della replica per un MariaDB</span><span class="sxs-lookup"><span data-stu-id="c1eed-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c1eed-111">Questo comando crea un DB della replica per un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c1eed-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="c1eed-112">Esempio 2: creare un DB della replica per un MariaDB</span><span class="sxs-lookup"><span data-stu-id="c1eed-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c1eed-113">Questo comando crea un DB della replica per un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c1eed-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="c1eed-114">Esempio 3: creare un DB della replica per un MariaDB</span><span class="sxs-lookup"><span data-stu-id="c1eed-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c1eed-115">Questo comando con il parametro InputObject crea un DB della replica con il parametro InputObject per un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c1eed-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="c1eed-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1eed-116">PARAMETERS</span></span>

### <span data-ttu-id="c1eed-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1eed-117">-AsJob</span></span>
<span data-ttu-id="c1eed-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c1eed-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c1eed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1eed-119">-DefaultProfile</span></span>
<span data-ttu-id="c1eed-120">Region DefaultParameters le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1eed-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1eed-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c1eed-121">-Location</span></span>
<span data-ttu-id="c1eed-122">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c1eed-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="c1eed-123">-Master</span><span class="sxs-lookup"><span data-stu-id="c1eed-123">-Master</span></span>
<span data-ttu-id="c1eed-124">Oggetto server di origine da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="c1eed-124">The source server object to restore from.</span></span>
<span data-ttu-id="c1eed-125">Per costruire, vedere la sezione Note per le proprietà MASTER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c1eed-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="c1eed-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="c1eed-126">-MasterName</span></span>
<span data-ttu-id="c1eed-127">Nome del server MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c1eed-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="c1eed-128">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="c1eed-128">-NoWait</span></span>
<span data-ttu-id="c1eed-129">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c1eed-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c1eed-130">-Replicaname</span><span class="sxs-lookup"><span data-stu-id="c1eed-130">-ReplicaName</span></span>
<span data-ttu-id="c1eed-131">Nome replica.</span><span class="sxs-lookup"><span data-stu-id="c1eed-131">Replica name.</span></span>

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

### <span data-ttu-id="c1eed-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1eed-132">-ResourceGroupName</span></span>
<span data-ttu-id="c1eed-133">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="c1eed-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c1eed-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="c1eed-134">-Sku</span></span>
<span data-ttu-id="c1eed-135">Nome dell'USK, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="c1eed-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="c1eed-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1eed-136">-SubscriptionId</span></span>
<span data-ttu-id="c1eed-137">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c1eed-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c1eed-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1eed-138">-Tag</span></span>
<span data-ttu-id="c1eed-139">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="c1eed-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="c1eed-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c1eed-140">-Confirm</span></span>
<span data-ttu-id="c1eed-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1eed-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1eed-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1eed-142">-WhatIf</span></span>
<span data-ttu-id="c1eed-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1eed-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1eed-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1eed-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1eed-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1eed-145">CommonParameters</span></span>
<span data-ttu-id="c1eed-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1eed-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1eed-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1eed-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1eed-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1eed-148">INPUTS</span></span>

### <span data-ttu-id="c1eed-149">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="c1eed-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="c1eed-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1eed-150">OUTPUTS</span></span>

### <span data-ttu-id="c1eed-151">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="c1eed-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="c1eed-152">Note</span><span class="sxs-lookup"><span data-stu-id="c1eed-152">NOTES</span></span>

<span data-ttu-id="c1eed-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c1eed-153">ALIASES</span></span>

<span data-ttu-id="c1eed-154">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1eed-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c1eed-155">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c1eed-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1eed-156">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c1eed-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c1eed-157">MASTER <IServer> : oggetto server di origine da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="c1eed-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="c1eed-158">`Location <String>`: La posizione in cui risiede la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c1eed-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="c1eed-159">`[Tag <ITrackedResourceTags>]`: Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="c1eed-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="c1eed-160">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c1eed-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c1eed-161">`[AdministratorLogin <String>]`: Nome di accesso dell'amministratore di un server.</span><span class="sxs-lookup"><span data-stu-id="c1eed-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="c1eed-162">Può essere specificato solo quando il server viene creato (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="c1eed-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="c1eed-163">`[EarliestRestoreDate <DateTime?>]`: Ora di creazione del punto di ripristino più iniziale (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="c1eed-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="c1eed-164">`[FullyQualifiedDomainName <String>]`: Il nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="c1eed-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="c1eed-165">`[IdentityType <IdentityType?>]`: Il tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="c1eed-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="c1eed-166">Imposta questa opzione su' SystemAssigned ' per creare e assegnare automaticamente un Principal di Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c1eed-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="c1eed-167">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="c1eed-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="c1eed-168">`[ReplicaCapacity <Int32?>]`: Il numero massimo di repliche che un server master può avere.</span><span class="sxs-lookup"><span data-stu-id="c1eed-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="c1eed-169">`[ReplicationRole <String>]`: Il ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="c1eed-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="c1eed-170">`[SkuCapacity <Int32?>]`: La capacità di scala su/fuori, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="c1eed-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="c1eed-171">`[SkuFamily <String>]`: La famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="c1eed-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="c1eed-172">`[SkuName <String>]`: Nome della SKU, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="c1eed-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="c1eed-173">`[SkuSize <String>]`: Il codice delle dimensioni, che deve essere interpretato dalla risorsa in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="c1eed-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="c1eed-174">`[SkuTier <SkuTier?>]`: Il livello del particolare SKU, ad esempio Basic.</span><span class="sxs-lookup"><span data-stu-id="c1eed-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="c1eed-175">`[SslEnforcement <SslEnforcementEnum?>]`: Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="c1eed-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="c1eed-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="c1eed-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="c1eed-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Abilitare il backup Geo-ridondante o meno per il server.</span><span class="sxs-lookup"><span data-stu-id="c1eed-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="c1eed-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c1eed-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="c1eed-179">`[StorageProfileStorageMb <Int32?>]`: Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="c1eed-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="c1eed-180">`[UserVisibleState <ServerState?>]`: Uno stato di un server visibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="c1eed-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="c1eed-181">`[Version <ServerVersion?>]`: Versione server.</span><span class="sxs-lookup"><span data-stu-id="c1eed-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="c1eed-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1eed-182">RELATED LINKS</span></span>

