---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 6b0aad7829dc337869c26656135d039b5f74974f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983021"
---
# <span data-ttu-id="9e64f-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="9e64f-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="9e64f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e64f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e64f-103">Ottenere la stringa di connessione di un database di MariaDB in un determinato framework.</span><span class="sxs-lookup"><span data-stu-id="9e64f-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="9e64f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e64f-104">SYNTAX</span></span>

### <span data-ttu-id="9e64f-105">ServerName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e64f-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9e64f-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="9e64f-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e64f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9e64f-107">DESCRIPTION</span></span>
<span data-ttu-id="9e64f-108">Ottenere la stringa di connessione di un database di MariaDB in un determinato framework.</span><span class="sxs-lookup"><span data-stu-id="9e64f-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="9e64f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e64f-109">EXAMPLES</span></span>

### <span data-ttu-id="9e64f-110">Esempio 1: Ottenere una stringa di connessione di MariaDB</span><span class="sxs-lookup"><span data-stu-id="9e64f-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="9e64f-111">Questo comando ottiene una stringa di connessione di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="9e64f-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="9e64f-112">Esempio 2: Ottenere una stringa di connessione di MariaDB</span><span class="sxs-lookup"><span data-stu-id="9e64f-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="9e64f-113">Questo comando ottiene una stringa di connessione di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="9e64f-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="9e64f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e64f-114">PARAMETERS</span></span>

### <span data-ttu-id="9e64f-115">-Client</span><span class="sxs-lookup"><span data-stu-id="9e64f-115">-Client</span></span>
<span data-ttu-id="9e64f-116">Tipo di client Connessione</span><span class="sxs-lookup"><span data-stu-id="9e64f-116">Connect client type</span></span>

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

### <span data-ttu-id="9e64f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e64f-117">-DefaultProfile</span></span>
<span data-ttu-id="9e64f-118">region DefaultParameters Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e64f-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e64f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e64f-119">-InputObject</span></span>
<span data-ttu-id="9e64f-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9e64f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e64f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9e64f-121">-Name</span></span>
<span data-ttu-id="9e64f-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="9e64f-122">The name of the server.</span></span>

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

### <span data-ttu-id="9e64f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e64f-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e64f-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9e64f-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="9e64f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e64f-125">-SubscriptionId</span></span>
<span data-ttu-id="9e64f-126">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio</span><span class="sxs-lookup"><span data-stu-id="9e64f-126">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e64f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e64f-127">CommonParameters</span></span>
<span data-ttu-id="9e64f-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e64f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e64f-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e64f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e64f-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="9e64f-130">INPUTS</span></span>

### <span data-ttu-id="9e64f-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="9e64f-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="9e64f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e64f-132">OUTPUTS</span></span>

### <span data-ttu-id="9e64f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9e64f-133">System.String</span></span>

## <span data-ttu-id="9e64f-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="9e64f-134">NOTES</span></span>

<span data-ttu-id="9e64f-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9e64f-135">ALIASES</span></span>

<span data-ttu-id="9e64f-136">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="9e64f-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e64f-137">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9e64f-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e64f-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e64f-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e64f-139">INPUTOBJECT <IServer> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="9e64f-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="9e64f-140">`Location <String>`: la posizione in cui risiede la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9e64f-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="9e64f-141">`[Tag <ITrackedResourceTags>]`: metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="9e64f-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="9e64f-142">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e64f-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="9e64f-143">`[AdministratorLogin <String>]`: nome di accesso di un server da parte dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="9e64f-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="9e64f-144">Può essere specificato solo durante la creazione del server (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="9e64f-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="9e64f-145">`[EarliestRestoreDate <DateTime?>]`: il primo momento di creazione del punto di ripristino (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="9e64f-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="9e64f-146">`[FullyQualifiedDomainName <String>]`: nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="9e64f-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="9e64f-147">`[IdentityType <IdentityType?>]`: tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="9e64f-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="9e64f-148">Impostare questo valore su "SystemAssigned" per creare e assegnare automaticamente un'entità Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9e64f-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="9e64f-149">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="9e64f-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="9e64f-150">`[ReplicaCapacity <Int32?>]`: numero massimo di replica consentite a un server master.</span><span class="sxs-lookup"><span data-stu-id="9e64f-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="9e64f-151">`[ReplicationRole <String>]`: ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="9e64f-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="9e64f-152">`[SkuCapacity <Int32?>]`: la capacità di scalabilità in orizzontale, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="9e64f-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="9e64f-153">`[SkuFamily <String>]`: famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="9e64f-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="9e64f-154">`[SkuName <String>]`: il nome della sKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="9e64f-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="9e64f-155">`[SkuSize <String>]`: il codice delle dimensioni, che deve essere interpretato dalla risorsa nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="9e64f-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="9e64f-156">`[SkuTier <SkuTier?>]`: il livello dello specifico SKU, ad esempio Base.</span><span class="sxs-lookup"><span data-stu-id="9e64f-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="9e64f-157">`[SslEnforcement <SslEnforcementEnum?>]`: per abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="9e64f-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="9e64f-158">`[StorageProfileBackupRetentionDay <Int32?>]`: giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="9e64f-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="9e64f-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="9e64f-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="9e64f-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: per abilitare l'estensione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e64f-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="9e64f-161">`[StorageProfileStorageMb <Int32?>]`: spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="9e64f-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="9e64f-162">`[UserVisibleState <ServerState?>]`: stato di un server visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="9e64f-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="9e64f-163">`[Version <ServerVersion?>]`: versione del server.</span><span class="sxs-lookup"><span data-stu-id="9e64f-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="9e64f-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e64f-164">RELATED LINKS</span></span>

