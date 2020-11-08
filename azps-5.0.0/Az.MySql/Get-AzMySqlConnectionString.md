---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: ab2e820ec0e1c943cfeb5f8b3d83babece38ed95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202854"
---
# <span data-ttu-id="56868-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="56868-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="56868-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56868-102">SYNOPSIS</span></span>
<span data-ttu-id="56868-103">Ottenere la stringa di connessione in base al provider di connessione client.</span><span class="sxs-lookup"><span data-stu-id="56868-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="56868-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56868-104">SYNTAX</span></span>

### <span data-ttu-id="56868-105">Get (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56868-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56868-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56868-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="56868-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56868-107">DESCRIPTION</span></span>
<span data-ttu-id="56868-108">Ottenere la stringa di connessione in base al provider di connessione client.</span><span class="sxs-lookup"><span data-stu-id="56868-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="56868-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56868-109">EXAMPLES</span></span>

### <span data-ttu-id="56868-110">Esempio 1: ottenere una stringa di connessione al server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="56868-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="56868-111">Questo cmdlet ottiene la stringa di connessione del server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="56868-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="56868-112">Esempio 2: ottenere la stringa di connessione del server MySql per identità</span><span class="sxs-lookup"><span data-stu-id="56868-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="56868-113">Questo cmdlet ottiene la stringa di connessione del server MySql per identità.</span><span class="sxs-lookup"><span data-stu-id="56868-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="56868-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56868-114">PARAMETERS</span></span>

### <span data-ttu-id="56868-115">-Client</span><span class="sxs-lookup"><span data-stu-id="56868-115">-Client</span></span>
<span data-ttu-id="56868-116">Provider di connessioni client.</span><span class="sxs-lookup"><span data-stu-id="56868-116">Client connection provider.</span></span>

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

### <span data-ttu-id="56868-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56868-117">-DefaultProfile</span></span>
<span data-ttu-id="56868-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56868-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56868-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56868-119">-InputObject</span></span>
<span data-ttu-id="56868-120">Oggetto server di origine per cui creare la replica.</span><span class="sxs-lookup"><span data-stu-id="56868-120">The source server object to create replica from.</span></span>
<span data-ttu-id="56868-121">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="56868-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56868-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="56868-122">-Name</span></span>
<span data-ttu-id="56868-123">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="56868-123">The name of the server.</span></span>

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

### <span data-ttu-id="56868-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56868-124">-ResourceGroupName</span></span>
<span data-ttu-id="56868-125">Nome del gruppo di risorse che contiene la risorsa, è possibile ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="56868-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="56868-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56868-126">-SubscriptionId</span></span>
<span data-ttu-id="56868-127">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="56868-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="56868-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56868-128">CommonParameters</span></span>
<span data-ttu-id="56868-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56868-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56868-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56868-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56868-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56868-131">INPUTS</span></span>

### <span data-ttu-id="56868-132">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="56868-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="56868-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56868-133">OUTPUTS</span></span>

### <span data-ttu-id="56868-134">System. String</span><span class="sxs-lookup"><span data-stu-id="56868-134">System.String</span></span>

## <span data-ttu-id="56868-135">Note</span><span class="sxs-lookup"><span data-stu-id="56868-135">NOTES</span></span>

<span data-ttu-id="56868-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="56868-136">ALIASES</span></span>

<span data-ttu-id="56868-137">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56868-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56868-138">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="56868-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56868-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56868-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56868-140">INPUTOBJECT <IServer> : oggetto server di origine da cui creare la replica.</span><span class="sxs-lookup"><span data-stu-id="56868-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="56868-141">`Location <String>`: La posizione in cui risiede la risorsa.</span><span class="sxs-lookup"><span data-stu-id="56868-141">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="56868-142">`[Tag <ITrackedResourceTags>]`: Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="56868-142">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="56868-143">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="56868-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="56868-144">`[AdministratorLogin <String>]`: Nome di accesso dell'amministratore di un server.</span><span class="sxs-lookup"><span data-stu-id="56868-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="56868-145">Può essere specificato solo quando il server viene creato (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="56868-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="56868-146">`[EarliestRestoreDate <DateTime?>]`: Ora di creazione del punto di ripristino più iniziale (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="56868-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="56868-147">`[FullyQualifiedDomainName <String>]`: Il nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="56868-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="56868-148">`[IdentityType <IdentityType?>]`: Il tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="56868-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="56868-149">Imposta questa opzione su' SystemAssigned ' per creare e assegnare automaticamente un Principal di Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="56868-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="56868-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stato che indica se il server ha abilitato la crittografia dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="56868-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="56868-151">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="56868-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="56868-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Applicare una versione TLS minima per il server.</span><span class="sxs-lookup"><span data-stu-id="56868-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="56868-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se l'accesso alla rete pubblica è consentito per il server.</span><span class="sxs-lookup"><span data-stu-id="56868-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="56868-154">Il valore è facoltativo ma, se passato, deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="56868-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="56868-155">`[ReplicaCapacity <Int32?>]`: Il numero massimo di repliche che un server master può avere.</span><span class="sxs-lookup"><span data-stu-id="56868-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="56868-156">`[ReplicationRole <String>]`: Il ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="56868-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="56868-157">`[SkuCapacity <Int32?>]`: La capacità di scala su/fuori, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="56868-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="56868-158">`[SkuFamily <String>]`: La famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="56868-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="56868-159">`[SkuName <String>]`: Nome della SKU, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="56868-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="56868-160">`[SkuSize <String>]`: Il codice delle dimensioni, che deve essere interpretato dalla risorsa in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="56868-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="56868-161">`[SkuTier <SkuTier?>]`: Il livello del particolare SKU, ad esempio Basic.</span><span class="sxs-lookup"><span data-stu-id="56868-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="56868-162">`[SslEnforcement <SslEnforcementEnum?>]`: Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="56868-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="56868-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="56868-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="56868-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Abilitare il backup Geo-ridondante o meno per il server.</span><span class="sxs-lookup"><span data-stu-id="56868-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="56868-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="56868-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="56868-166">`[StorageProfileStorageMb <Int32?>]`: Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="56868-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="56868-167">`[UserVisibleState <ServerState?>]`: Uno stato di un server visibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="56868-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="56868-168">`[Version <ServerVersion?>]`: Versione server.</span><span class="sxs-lookup"><span data-stu-id="56868-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="56868-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56868-169">RELATED LINKS</span></span>

