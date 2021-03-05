---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: ae0a5f2130ea4b5120fdbe78ab4cc23a7eba29a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996097"
---
# <span data-ttu-id="2329d-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="2329d-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="2329d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2329d-102">SYNOPSIS</span></span>
<span data-ttu-id="2329d-103">Ottenere la stringa di connessione in base al provider di connessione client.</span><span class="sxs-lookup"><span data-stu-id="2329d-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="2329d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2329d-104">SYNTAX</span></span>

### <span data-ttu-id="2329d-105">Ottieni (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2329d-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2329d-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2329d-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2329d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2329d-107">DESCRIPTION</span></span>
<span data-ttu-id="2329d-108">Ottenere la stringa di connessione in base al provider di connessione client.</span><span class="sxs-lookup"><span data-stu-id="2329d-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="2329d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2329d-109">EXAMPLES</span></span>

### <span data-ttu-id="2329d-110">Esempio 1: Ottenere la stringa di connessione del server PostgreSql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="2329d-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="2329d-111">Questo cmdlet ottiene la stringa di connessione PostgreSql per gruppo di risorse e nome del server.</span><span class="sxs-lookup"><span data-stu-id="2329d-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="2329d-112">Esempio 2: Ottenere la stringa di connessione del server PostgreSql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="2329d-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="2329d-113">Questo cmdlet ottiene la stringa di connessione del server PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="2329d-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="2329d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2329d-114">PARAMETERS</span></span>

### <span data-ttu-id="2329d-115">-Client</span><span class="sxs-lookup"><span data-stu-id="2329d-115">-Client</span></span>
<span data-ttu-id="2329d-116">Provider di connessione client.</span><span class="sxs-lookup"><span data-stu-id="2329d-116">Client connection provider.</span></span>

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

### <span data-ttu-id="2329d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2329d-117">-DefaultProfile</span></span>
<span data-ttu-id="2329d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2329d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2329d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2329d-119">-InputObject</span></span>
<span data-ttu-id="2329d-120">Il server per la stringa di connessione To construct, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2329d-120">The server for the connection string To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2329d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2329d-121">-Name</span></span>
<span data-ttu-id="2329d-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="2329d-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2329d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2329d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2329d-124">Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="2329d-124">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2329d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2329d-125">-SubscriptionId</span></span>
<span data-ttu-id="2329d-126">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2329d-126">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2329d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2329d-127">CommonParameters</span></span>
<span data-ttu-id="2329d-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2329d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2329d-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2329d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2329d-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="2329d-130">INPUTS</span></span>

### <span data-ttu-id="2329d-131">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="2329d-131">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="2329d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2329d-132">OUTPUTS</span></span>

### <span data-ttu-id="2329d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2329d-133">System.String</span></span>

## <span data-ttu-id="2329d-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="2329d-134">NOTES</span></span>

<span data-ttu-id="2329d-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2329d-135">ALIASES</span></span>

<span data-ttu-id="2329d-136">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="2329d-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2329d-137">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2329d-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2329d-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2329d-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2329d-139"><IServer>INPUTOBJECT: server per la stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="2329d-139">INPUTOBJECT <IServer>: The server for the connection string</span></span>
  - <span data-ttu-id="2329d-140">`Location <String>`: posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="2329d-140">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="2329d-141">`[Tag <ITrackedResourceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="2329d-141">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="2329d-142">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2329d-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2329d-143">`[AdministratorLogin <String>]`: nome di accesso di un server da parte dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="2329d-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="2329d-144">Può essere specificato solo durante la creazione del server (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="2329d-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="2329d-145">`[EarliestRestoreDate <DateTime?>]`: la prima ora di creazione del punto di ripristino (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="2329d-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="2329d-146">`[FullyQualifiedDomainName <String>]`: nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="2329d-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="2329d-147">`[IdentityType <IdentityType?>]`: tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="2329d-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="2329d-148">Impostare questo valore su "SystemAssigned" per creare e assegnare automaticamente un'entità Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2329d-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="2329d-149">`[InfrastructureEncryption <InfrastructureEncryption?>]`: stato che indica se la crittografia dell'infrastruttura abilitata per il server è abilitata.</span><span class="sxs-lookup"><span data-stu-id="2329d-149">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="2329d-150">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="2329d-150">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="2329d-151">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: consente di applicare una versione minima di Tls per il server.</span><span class="sxs-lookup"><span data-stu-id="2329d-151">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="2329d-152">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: indica se l'accesso alla rete pubblica è consentito o meno per questo server.</span><span class="sxs-lookup"><span data-stu-id="2329d-152">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="2329d-153">Il valore è facoltativo ma, se passato, deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="2329d-153">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="2329d-154">`[ReplicaCapacity <Int32?>]`: numero massimo di replica consentite a un server master.</span><span class="sxs-lookup"><span data-stu-id="2329d-154">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="2329d-155">`[ReplicationRole <String>]`: ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="2329d-155">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="2329d-156">`[SkuCapacity <Int32?>]`: la capacità di scalabilità in orizzontale e in uscita che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="2329d-156">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="2329d-157">`[SkuFamily <String>]`: famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="2329d-157">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="2329d-158">`[SkuName <String>]`: il nome della SKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="2329d-158">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="2329d-159">`[SkuSize <String>]`: il codice delle dimensioni, che deve essere interpretato dalla risorsa nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="2329d-159">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="2329d-160">`[SkuTier <SkuTier?>]`: il livello dello specifico SKU, ad esempio Di base.</span><span class="sxs-lookup"><span data-stu-id="2329d-160">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="2329d-161">`[SslEnforcement <SslEnforcementEnum?>]`: per abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="2329d-161">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="2329d-162">`[StorageProfileBackupRetentionDay <Int32?>]`: giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="2329d-162">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="2329d-163">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="2329d-163">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="2329d-164">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: per abilitare l'estensione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2329d-164">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="2329d-165">`[StorageProfileStorageMb <Int32?>]`: spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="2329d-165">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="2329d-166">`[UserVisibleState <ServerState?>]`: stato di un server visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="2329d-166">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="2329d-167">`[Version <ServerVersion?>]`: versione server.</span><span class="sxs-lookup"><span data-stu-id="2329d-167">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="2329d-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2329d-168">RELATED LINKS</span></span>

