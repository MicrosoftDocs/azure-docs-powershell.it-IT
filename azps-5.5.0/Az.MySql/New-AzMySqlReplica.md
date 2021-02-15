---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 58158888b99a5f4662de7530576eca084f849966
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207131"
---
# <span data-ttu-id="33efd-101">New-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="33efd-101">New-AzMySqlReplica</span></span>

## <span data-ttu-id="33efd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33efd-102">SYNOPSIS</span></span>
<span data-ttu-id="33efd-103">Crea una nuova replica da un database esistente.</span><span class="sxs-lookup"><span data-stu-id="33efd-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="33efd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33efd-104">SYNTAX</span></span>

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="33efd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="33efd-105">DESCRIPTION</span></span>
<span data-ttu-id="33efd-106">Crea una nuova replica da un database esistente.</span><span class="sxs-lookup"><span data-stu-id="33efd-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="33efd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33efd-107">EXAMPLES</span></span>

### <span data-ttu-id="33efd-108">Esempio 1: Creare una nuova replica del server MySql</span><span class="sxs-lookup"><span data-stu-id="33efd-108">Example 1: Create a new MySql server replica</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="33efd-109">Questo cmdlet crea una nuova replica del server MySql.</span><span class="sxs-lookup"><span data-stu-id="33efd-109">This cmdlet creates a new MySql server replica.</span></span>

### <span data-ttu-id="33efd-110">Esempio 2: Creare una nuova replica del server MySql</span><span class="sxs-lookup"><span data-stu-id="33efd-110">Example 2: Create a new MySql server replica</span></span>
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="33efd-111">Questo cmdlet con il parametro master(inputobject) crea una nuova replica del server MySql.</span><span class="sxs-lookup"><span data-stu-id="33efd-111">This cmdlet with parameter master(inputobject) creates a new MySql server replica.</span></span>

## <span data-ttu-id="33efd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33efd-112">PARAMETERS</span></span>

### <span data-ttu-id="33efd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33efd-113">-AsJob</span></span>
<span data-ttu-id="33efd-114">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="33efd-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="33efd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33efd-115">-DefaultProfile</span></span>
<span data-ttu-id="33efd-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33efd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33efd-117">-Location</span><span class="sxs-lookup"><span data-stu-id="33efd-117">-Location</span></span>
<span data-ttu-id="33efd-118">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="33efd-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="33efd-119">-Master</span><span class="sxs-lookup"><span data-stu-id="33efd-119">-Master</span></span>
<span data-ttu-id="33efd-120">Oggetto server di origine da cui creare la replica.</span><span class="sxs-lookup"><span data-stu-id="33efd-120">The source server object to create replica from.</span></span>
<span data-ttu-id="33efd-121">Per creare, vedere la sezione NOTE relativa alle proprietà MASTER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="33efd-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33efd-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="33efd-122">-NoWait</span></span>
<span data-ttu-id="33efd-123">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="33efd-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="33efd-124">-Replica</span><span class="sxs-lookup"><span data-stu-id="33efd-124">-Replica</span></span>
<span data-ttu-id="33efd-125">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="33efd-125">The name of the server.</span></span>

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

### <span data-ttu-id="33efd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33efd-126">-ResourceGroupName</span></span>
<span data-ttu-id="33efd-127">Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="33efd-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="33efd-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="33efd-128">-Sku</span></span>
<span data-ttu-id="33efd-129">Il nome della sKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="33efd-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="33efd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33efd-130">-SubscriptionId</span></span>
<span data-ttu-id="33efd-131">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="33efd-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="33efd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33efd-132">-Confirm</span></span>
<span data-ttu-id="33efd-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33efd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33efd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33efd-134">-WhatIf</span></span>
<span data-ttu-id="33efd-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33efd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33efd-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33efd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33efd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33efd-137">CommonParameters</span></span>
<span data-ttu-id="33efd-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33efd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33efd-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="33efd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33efd-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="33efd-140">INPUTS</span></span>

### <span data-ttu-id="33efd-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="33efd-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="33efd-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33efd-142">OUTPUTS</span></span>

### <span data-ttu-id="33efd-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="33efd-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="33efd-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="33efd-144">NOTES</span></span>

<span data-ttu-id="33efd-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="33efd-145">ALIASES</span></span>

<span data-ttu-id="33efd-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="33efd-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33efd-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="33efd-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33efd-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="33efd-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33efd-149">MASTER: <IServer> oggetto server di origine da cui creare la replica.</span><span class="sxs-lookup"><span data-stu-id="33efd-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="33efd-150">`Location <String>`: posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="33efd-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="33efd-151">`[Tag <ITrackedResourceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="33efd-151">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="33efd-152">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33efd-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="33efd-153">`[AdministratorLogin <String>]`: nome di accesso di un server da parte dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="33efd-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="33efd-154">Può essere specificato solo durante la creazione del server (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="33efd-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="33efd-155">`[EarliestRestoreDate <DateTime?>]`: il primo momento di creazione del punto di ripristino (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="33efd-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="33efd-156">`[FullyQualifiedDomainName <String>]`: nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="33efd-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="33efd-157">`[IdentityType <IdentityType?>]`: tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="33efd-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="33efd-158">Impostare questo valore su "SystemAssigned" per creare e assegnare automaticamente un'entità Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="33efd-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="33efd-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: stato che indica se la crittografia dell'infrastruttura abilitata per il server è abilitata.</span><span class="sxs-lookup"><span data-stu-id="33efd-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="33efd-160">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="33efd-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="33efd-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: consente di applicare una versione minima di Tls per il server.</span><span class="sxs-lookup"><span data-stu-id="33efd-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="33efd-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: indica se l'accesso alla rete pubblica è consentito o meno per questo server.</span><span class="sxs-lookup"><span data-stu-id="33efd-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="33efd-163">Il valore è facoltativo ma, se passato, deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="33efd-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="33efd-164">`[ReplicaCapacity <Int32?>]`: numero massimo di replica consentite a un server master.</span><span class="sxs-lookup"><span data-stu-id="33efd-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="33efd-165">`[ReplicationRole <String>]`: ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="33efd-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="33efd-166">`[SkuCapacity <Int32?>]`: la capacità di scalabilità in orizzontale, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="33efd-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="33efd-167">`[SkuFamily <String>]`: famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="33efd-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="33efd-168">`[SkuName <String>]`: il nome della SKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="33efd-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="33efd-169">`[SkuSize <String>]`: il codice delle dimensioni, che deve essere interpretato dalla risorsa nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="33efd-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="33efd-170">`[SkuTier <SkuTier?>]`: il livello dello specifico SKU, ad esempio Di base.</span><span class="sxs-lookup"><span data-stu-id="33efd-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="33efd-171">`[SslEnforcement <SslEnforcementEnum?>]`: per abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="33efd-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="33efd-172">`[StorageProfileBackupRetentionDay <Int32?>]`: giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="33efd-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="33efd-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="33efd-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="33efd-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: per abilitare l'estensione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33efd-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="33efd-175">`[StorageProfileStorageMb <Int32?>]`: spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="33efd-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="33efd-176">`[UserVisibleState <ServerState?>]`: stato di un server visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="33efd-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="33efd-177">`[Version <ServerVersion?>]`: versione del server.</span><span class="sxs-lookup"><span data-stu-id="33efd-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="33efd-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33efd-178">RELATED LINKS</span></span>

