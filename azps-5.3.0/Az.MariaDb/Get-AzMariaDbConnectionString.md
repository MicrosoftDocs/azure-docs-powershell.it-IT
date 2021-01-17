---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380729"
---
# <span data-ttu-id="5254a-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="5254a-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="5254a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5254a-102">SYNOPSIS</span></span>
<span data-ttu-id="5254a-103">Ottenere una stringa di connessione di un MariaDB in un Framework specifico.</span><span class="sxs-lookup"><span data-stu-id="5254a-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="5254a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5254a-104">SYNTAX</span></span>

### <span data-ttu-id="5254a-105">Nomeserver (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5254a-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5254a-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="5254a-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5254a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5254a-107">DESCRIPTION</span></span>
<span data-ttu-id="5254a-108">Ottenere una stringa di connessione di un MariaDB in un Framework specifico.</span><span class="sxs-lookup"><span data-stu-id="5254a-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="5254a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5254a-109">EXAMPLES</span></span>

### <span data-ttu-id="5254a-110">Esempio 1: ottenere una stringa di connessione di MariaDB</span><span class="sxs-lookup"><span data-stu-id="5254a-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="5254a-111">Questo comando ottiene una stringa di connessione di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="5254a-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="5254a-112">Esempio 2: ottenere una stringa di connessione di MariaDB</span><span class="sxs-lookup"><span data-stu-id="5254a-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="5254a-113">Questo comando ottiene una stringa di connessione di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="5254a-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="5254a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5254a-114">PARAMETERS</span></span>

### <span data-ttu-id="5254a-115">-Client</span><span class="sxs-lookup"><span data-stu-id="5254a-115">-Client</span></span>
<span data-ttu-id="5254a-116">Connettere il tipo di client</span><span class="sxs-lookup"><span data-stu-id="5254a-116">Connect client type</span></span>

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

### <span data-ttu-id="5254a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5254a-117">-DefaultProfile</span></span>
<span data-ttu-id="5254a-118">Region DefaultParameters le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5254a-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5254a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5254a-119">-InputObject</span></span>
<span data-ttu-id="5254a-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5254a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5254a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5254a-121">-Name</span></span>
<span data-ttu-id="5254a-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="5254a-122">The name of the server.</span></span>

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

### <span data-ttu-id="5254a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5254a-123">-ResourceGroupName</span></span>
<span data-ttu-id="5254a-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5254a-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="5254a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5254a-125">-SubscriptionId</span></span>
<span data-ttu-id="5254a-126">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio</span><span class="sxs-lookup"><span data-stu-id="5254a-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="5254a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5254a-127">CommonParameters</span></span>
<span data-ttu-id="5254a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5254a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5254a-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5254a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5254a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5254a-130">INPUTS</span></span>

### <span data-ttu-id="5254a-131">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="5254a-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="5254a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5254a-132">OUTPUTS</span></span>

### <span data-ttu-id="5254a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5254a-133">System.String</span></span>

## <span data-ttu-id="5254a-134">Note</span><span class="sxs-lookup"><span data-stu-id="5254a-134">NOTES</span></span>

<span data-ttu-id="5254a-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5254a-135">ALIASES</span></span>

<span data-ttu-id="5254a-136">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5254a-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5254a-137">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5254a-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5254a-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5254a-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5254a-139">INPUTOBJECT <IServer> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5254a-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="5254a-140">`Location <String>`: La posizione in cui risiede la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5254a-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="5254a-141">`[Tag <ITrackedResourceTags>]`: Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="5254a-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="5254a-142">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="5254a-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5254a-143">`[AdministratorLogin <String>]`: Nome di accesso dell'amministratore di un server.</span><span class="sxs-lookup"><span data-stu-id="5254a-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="5254a-144">Può essere specificato solo quando il server viene creato (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="5254a-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="5254a-145">`[EarliestRestoreDate <DateTime?>]`: Ora di creazione del punto di ripristino più iniziale (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="5254a-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="5254a-146">`[FullyQualifiedDomainName <String>]`: Il nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="5254a-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="5254a-147">`[IdentityType <IdentityType?>]`: Il tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="5254a-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="5254a-148">Imposta questa opzione su' SystemAssigned ' per creare e assegnare automaticamente un Principal di Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5254a-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="5254a-149">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="5254a-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="5254a-150">`[ReplicaCapacity <Int32?>]`: Il numero massimo di repliche che un server master può avere.</span><span class="sxs-lookup"><span data-stu-id="5254a-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="5254a-151">`[ReplicationRole <String>]`: Il ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="5254a-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="5254a-152">`[SkuCapacity <Int32?>]`: La capacità di scala su/fuori, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="5254a-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="5254a-153">`[SkuFamily <String>]`: La famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="5254a-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="5254a-154">`[SkuName <String>]`: Nome della SKU, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="5254a-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="5254a-155">`[SkuSize <String>]`: Il codice delle dimensioni, che deve essere interpretato dalla risorsa in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="5254a-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="5254a-156">`[SkuTier <SkuTier?>]`: Il livello del particolare SKU, ad esempio Basic.</span><span class="sxs-lookup"><span data-stu-id="5254a-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="5254a-157">`[SslEnforcement <SslEnforcementEnum?>]`: Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="5254a-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="5254a-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="5254a-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="5254a-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Abilitare il backup Geo-ridondante o meno per il server.</span><span class="sxs-lookup"><span data-stu-id="5254a-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="5254a-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5254a-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="5254a-161">`[StorageProfileStorageMb <Int32?>]`: Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="5254a-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="5254a-162">`[UserVisibleState <ServerState?>]`: Uno stato di un server visibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="5254a-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="5254a-163">`[Version <ServerVersion?>]`: Versione server.</span><span class="sxs-lookup"><span data-stu-id="5254a-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="5254a-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5254a-164">RELATED LINKS</span></span>

