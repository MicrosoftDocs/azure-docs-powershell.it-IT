---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: 65eb0d924391e6e12b3b81ac487b746e1b91fa94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192158"
---
# <span data-ttu-id="0f96d-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="0f96d-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="0f96d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f96d-102">SYNOPSIS</span></span>
<span data-ttu-id="0f96d-103">Ottenere la stringa di connessione in base al provider di connessione client.</span><span class="sxs-lookup"><span data-stu-id="0f96d-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="0f96d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f96d-104">SYNTAX</span></span>

### <span data-ttu-id="0f96d-105">Ottieni (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f96d-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0f96d-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0f96d-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f96d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f96d-107">DESCRIPTION</span></span>
<span data-ttu-id="0f96d-108">Ottenere la stringa di connessione in base al provider di connessione client.</span><span class="sxs-lookup"><span data-stu-id="0f96d-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="0f96d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f96d-109">EXAMPLES</span></span>

### <span data-ttu-id="0f96d-110">Esempio 1: Ottenere la stringa di connessione del server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="0f96d-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="0f96d-111">Questo cmdlet ottiene la stringa di connessione del server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="0f96d-112">Esempio 2: Ottenere la stringa di connessione del server MySql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="0f96d-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="0f96d-113">Questo cmdlet ottiene la stringa di connessione del server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="0f96d-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="0f96d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f96d-114">PARAMETERS</span></span>

### <span data-ttu-id="0f96d-115">-Client</span><span class="sxs-lookup"><span data-stu-id="0f96d-115">-Client</span></span>
<span data-ttu-id="0f96d-116">Provider di connessione client.</span><span class="sxs-lookup"><span data-stu-id="0f96d-116">Client connection provider.</span></span>

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

### <span data-ttu-id="0f96d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f96d-117">-DefaultProfile</span></span>
<span data-ttu-id="0f96d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f96d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f96d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f96d-119">-InputObject</span></span>
<span data-ttu-id="0f96d-120">Server per la stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="0f96d-120">The server for the connection string.</span></span>
<span data-ttu-id="0f96d-121">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0f96d-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f96d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0f96d-122">-Name</span></span>
<span data-ttu-id="0f96d-123">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-123">The name of the server.</span></span>

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

### <span data-ttu-id="0f96d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f96d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f96d-125">Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="0f96d-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0f96d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f96d-126">-SubscriptionId</span></span>
<span data-ttu-id="0f96d-127">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0f96d-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="0f96d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f96d-128">CommonParameters</span></span>
<span data-ttu-id="0f96d-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f96d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f96d-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f96d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f96d-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f96d-131">INPUTS</span></span>

### <span data-ttu-id="0f96d-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="0f96d-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0f96d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f96d-133">OUTPUTS</span></span>

### <span data-ttu-id="0f96d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0f96d-134">System.String</span></span>

## <span data-ttu-id="0f96d-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f96d-135">NOTES</span></span>

<span data-ttu-id="0f96d-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0f96d-136">ALIASES</span></span>

<span data-ttu-id="0f96d-137">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0f96d-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0f96d-138">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0f96d-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f96d-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f96d-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0f96d-140"><IServer>INPUTOBJECT: server per la stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="0f96d-140">INPUTOBJECT <IServer>: The server for the connection string.</span></span>
  - <span data-ttu-id="0f96d-141">`Location <String>`: posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="0f96d-141">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="0f96d-142">`[Tag <ITrackedResourceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f96d-142">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="0f96d-143">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0f96d-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0f96d-144">`[AdministratorLogin <String>]`: nome di accesso di un server da parte dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="0f96d-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="0f96d-145">Può essere specificato solo durante la creazione del server (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="0f96d-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="0f96d-146">`[EarliestRestoreDate <DateTime?>]`: il primo momento di creazione del punto di ripristino (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="0f96d-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="0f96d-147">`[FullyQualifiedDomainName <String>]`: nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="0f96d-148">`[IdentityType <IdentityType?>]`: tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="0f96d-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="0f96d-149">Impostare questo valore su "SystemAssigned" per creare e assegnare automaticamente un'entità Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f96d-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="0f96d-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: stato che indica se la crittografia dell'infrastruttura abilitata per il server è abilitata.</span><span class="sxs-lookup"><span data-stu-id="0f96d-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="0f96d-151">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="0f96d-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="0f96d-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: consente di applicare una versione minima di Tls per il server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="0f96d-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: indica se l'accesso alla rete pubblica è consentito o meno per questo server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="0f96d-154">Il valore è facoltativo ma, se passato, deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="0f96d-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="0f96d-155">`[ReplicaCapacity <Int32?>]`: numero massimo di replica consentite a un server master.</span><span class="sxs-lookup"><span data-stu-id="0f96d-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="0f96d-156">`[ReplicationRole <String>]`: ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="0f96d-157">`[SkuCapacity <Int32?>]`: la capacità di scalabilità in orizzontale, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="0f96d-158">`[SkuFamily <String>]`: famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="0f96d-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="0f96d-159">`[SkuName <String>]`: il nome della SKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0f96d-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="0f96d-160">`[SkuSize <String>]`: il codice delle dimensioni, che deve essere interpretato dalla risorsa nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="0f96d-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="0f96d-161">`[SkuTier <SkuTier?>]`: il livello dello specifico SKU, ad esempio Di base.</span><span class="sxs-lookup"><span data-stu-id="0f96d-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="0f96d-162">`[SslEnforcement <SslEnforcementEnum?>]`: per abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="0f96d-163">`[StorageProfileBackupRetentionDay <Int32?>]`: giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="0f96d-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="0f96d-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: per abilitare l'estensione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0f96d-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="0f96d-166">`[StorageProfileStorageMb <Int32?>]`: spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="0f96d-167">`[UserVisibleState <ServerState?>]`: stato di un server visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="0f96d-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="0f96d-168">`[Version <ServerVersion?>]`: versione del server.</span><span class="sxs-lookup"><span data-stu-id="0f96d-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="0f96d-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f96d-169">RELATED LINKS</span></span>

