---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: 1af66eec2e67048ed85d90c0cdae2867b932b2b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193134"
---
# <span data-ttu-id="09f8b-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="09f8b-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="09f8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="09f8b-103">Crea una nuova replica da un database esistente.</span><span class="sxs-lookup"><span data-stu-id="09f8b-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="09f8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09f8b-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09f8b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="09f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="09f8b-106">Crea una nuova replica da un database esistente.</span><span class="sxs-lookup"><span data-stu-id="09f8b-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="09f8b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09f8b-107">EXAMPLES</span></span>

### <span data-ttu-id="09f8b-108">Esempio 1: Creare una nuova replica del server PostgreSql</span><span class="sxs-lookup"><span data-stu-id="09f8b-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="09f8b-109">Questo cmdlet crea una nuova replica del server PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="09f8b-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="09f8b-110">Esempio 2: Creare una nuova replica del server PostgreSql</span><span class="sxs-lookup"><span data-stu-id="09f8b-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="09f8b-111">Questo cmdlet crea una nuova replica del server PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="09f8b-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="09f8b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09f8b-112">PARAMETERS</span></span>

### <span data-ttu-id="09f8b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09f8b-113">-AsJob</span></span>
<span data-ttu-id="09f8b-114">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="09f8b-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="09f8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f8b-115">-DefaultProfile</span></span>
<span data-ttu-id="09f8b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09f8b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09f8b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="09f8b-117">-Location</span></span>
<span data-ttu-id="09f8b-118">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="09f8b-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="09f8b-119">-Master</span><span class="sxs-lookup"><span data-stu-id="09f8b-119">-Master</span></span>
<span data-ttu-id="09f8b-120">Oggetto server di origine da cui creare la replica.</span><span class="sxs-lookup"><span data-stu-id="09f8b-120">The source server object to create replica from.</span></span>
<span data-ttu-id="09f8b-121">Per creare, vedere la sezione NOTE relativa alle proprietà MASTER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="09f8b-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09f8b-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="09f8b-122">-NoWait</span></span>
<span data-ttu-id="09f8b-123">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="09f8b-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="09f8b-124">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="09f8b-124">-ReplicaName</span></span>
<span data-ttu-id="09f8b-125">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="09f8b-125">The name of the server.</span></span>

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

### <span data-ttu-id="09f8b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f8b-126">-ResourceGroupName</span></span>
<span data-ttu-id="09f8b-127">Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="09f8b-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="09f8b-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="09f8b-128">-Sku</span></span>
<span data-ttu-id="09f8b-129">Il nome della sKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="09f8b-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="09f8b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09f8b-130">-SubscriptionId</span></span>
<span data-ttu-id="09f8b-131">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="09f8b-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="09f8b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09f8b-132">-Confirm</span></span>
<span data-ttu-id="09f8b-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09f8b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09f8b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09f8b-134">-WhatIf</span></span>
<span data-ttu-id="09f8b-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09f8b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09f8b-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09f8b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09f8b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f8b-137">CommonParameters</span></span>
<span data-ttu-id="09f8b-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f8b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f8b-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="09f8b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f8b-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="09f8b-140">INPUTS</span></span>

### <span data-ttu-id="09f8b-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="09f8b-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="09f8b-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09f8b-142">OUTPUTS</span></span>

### <span data-ttu-id="09f8b-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="09f8b-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="09f8b-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="09f8b-144">NOTES</span></span>

<span data-ttu-id="09f8b-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="09f8b-145">ALIASES</span></span>

<span data-ttu-id="09f8b-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="09f8b-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09f8b-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="09f8b-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09f8b-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="09f8b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09f8b-149">MASTER: <IServer> oggetto server di origine da cui creare la replica.</span><span class="sxs-lookup"><span data-stu-id="09f8b-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="09f8b-150">`Location <String>`: posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="09f8b-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="09f8b-151">`[Tag <ITrackedResourceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="09f8b-151">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="09f8b-152">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="09f8b-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="09f8b-153">`[AdministratorLogin <String>]`: nome di accesso di un server da parte dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="09f8b-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="09f8b-154">Può essere specificato solo durante la creazione del server (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="09f8b-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="09f8b-155">`[EarliestRestoreDate <DateTime?>]`: il primo momento di creazione del punto di ripristino (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="09f8b-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="09f8b-156">`[FullyQualifiedDomainName <String>]`: nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="09f8b-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="09f8b-157">`[IdentityType <IdentityType?>]`: tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="09f8b-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="09f8b-158">Impostare questo valore su "SystemAssigned" per creare e assegnare automaticamente un'entità Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="09f8b-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="09f8b-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: stato che indica se la crittografia dell'infrastruttura abilitata per il server è abilitata.</span><span class="sxs-lookup"><span data-stu-id="09f8b-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="09f8b-160">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="09f8b-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="09f8b-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: consente di applicare una versione minima di Tls per il server.</span><span class="sxs-lookup"><span data-stu-id="09f8b-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="09f8b-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: indica se l'accesso alla rete pubblica è consentito o meno per questo server.</span><span class="sxs-lookup"><span data-stu-id="09f8b-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="09f8b-163">Il valore è facoltativo ma, se passato, deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="09f8b-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="09f8b-164">`[ReplicaCapacity <Int32?>]`: numero massimo di replica consentite a un server master.</span><span class="sxs-lookup"><span data-stu-id="09f8b-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="09f8b-165">`[ReplicationRole <String>]`: ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="09f8b-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="09f8b-166">`[SkuCapacity <Int32?>]`: la capacità di scalabilità in orizzontale, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="09f8b-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="09f8b-167">`[SkuFamily <String>]`: famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="09f8b-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="09f8b-168">`[SkuName <String>]`: il nome della SKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="09f8b-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="09f8b-169">`[SkuSize <String>]`: il codice delle dimensioni, che deve essere interpretato dalla risorsa nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="09f8b-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="09f8b-170">`[SkuTier <SkuTier?>]`: il livello dello specifico SKU, ad esempio Di base.</span><span class="sxs-lookup"><span data-stu-id="09f8b-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="09f8b-171">`[SslEnforcement <SslEnforcementEnum?>]`: per abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="09f8b-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="09f8b-172">`[StorageProfileBackupRetentionDay <Int32?>]`: giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="09f8b-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="09f8b-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="09f8b-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="09f8b-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: per abilitare l'estensione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="09f8b-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="09f8b-175">`[StorageProfileStorageMb <Int32?>]`: spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="09f8b-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="09f8b-176">`[UserVisibleState <ServerState?>]`: stato di un server visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="09f8b-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="09f8b-177">`[Version <ServerVersion?>]`: versione del server.</span><span class="sxs-lookup"><span data-stu-id="09f8b-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="09f8b-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09f8b-178">RELATED LINKS</span></span>

