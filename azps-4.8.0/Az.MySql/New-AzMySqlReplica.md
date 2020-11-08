---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 5e5d83266dd86ccaf0bd5037c6af01f8b1846a69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031637"
---
# <span data-ttu-id="b35f1-101">New-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="b35f1-101">New-AzMySqlReplica</span></span>

## <span data-ttu-id="b35f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b35f1-102">SYNOPSIS</span></span>
<span data-ttu-id="b35f1-103">Crea una nuova replica da un database esistente.</span><span class="sxs-lookup"><span data-stu-id="b35f1-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="b35f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b35f1-104">SYNTAX</span></span>

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b35f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b35f1-105">DESCRIPTION</span></span>
<span data-ttu-id="b35f1-106">Crea una nuova replica da un database esistente.</span><span class="sxs-lookup"><span data-stu-id="b35f1-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="b35f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b35f1-107">EXAMPLES</span></span>

### <span data-ttu-id="b35f1-108">Esempio 1: creare una nuova replica del server MySql</span><span class="sxs-lookup"><span data-stu-id="b35f1-108">Example 1: Create a new MySql server replica</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="b35f1-109">Questo cmdlet crea una nuova replica del server MySql.</span><span class="sxs-lookup"><span data-stu-id="b35f1-109">This cmdlet creates a new MySql server replica.</span></span>

### <span data-ttu-id="b35f1-110">Esempio 2: creare una nuova replica del server MySql</span><span class="sxs-lookup"><span data-stu-id="b35f1-110">Example 2: Create a new MySql server replica</span></span>
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="b35f1-111">Questo cmdlet con parameter Master (InputObject) crea una nuova replica del server MySql.</span><span class="sxs-lookup"><span data-stu-id="b35f1-111">This cmdlet with parameter master(inputobject) creates a new MySql server replica.</span></span>

## <span data-ttu-id="b35f1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b35f1-112">PARAMETERS</span></span>

### <span data-ttu-id="b35f1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b35f1-113">-AsJob</span></span>
<span data-ttu-id="b35f1-114">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="b35f1-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="b35f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35f1-115">-DefaultProfile</span></span>
<span data-ttu-id="b35f1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b35f1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b35f1-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b35f1-117">-Location</span></span>
<span data-ttu-id="b35f1-118">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b35f1-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="b35f1-119">-Master</span><span class="sxs-lookup"><span data-stu-id="b35f1-119">-Master</span></span>
<span data-ttu-id="b35f1-120">Oggetto server di origine per cui creare la replica.</span><span class="sxs-lookup"><span data-stu-id="b35f1-120">The source server object to create replica from.</span></span>
<span data-ttu-id="b35f1-121">Per costruire, vedere la sezione Note per le proprietà MASTER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b35f1-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="b35f1-122">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="b35f1-122">-NoWait</span></span>
<span data-ttu-id="b35f1-123">Esegui il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="b35f1-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b35f1-124">-Replica</span><span class="sxs-lookup"><span data-stu-id="b35f1-124">-Replica</span></span>
<span data-ttu-id="b35f1-125">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-125">The name of the server.</span></span>

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

### <span data-ttu-id="b35f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b35f1-126">-ResourceGroupName</span></span>
<span data-ttu-id="b35f1-127">Nome del gruppo di risorse che contiene la risorsa, è possibile ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b35f1-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b35f1-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="b35f1-128">-Sku</span></span>
<span data-ttu-id="b35f1-129">Nome dell'USK, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="b35f1-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="b35f1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b35f1-130">-SubscriptionId</span></span>
<span data-ttu-id="b35f1-131">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="b35f1-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b35f1-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b35f1-132">-Confirm</span></span>
<span data-ttu-id="b35f1-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b35f1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b35f1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b35f1-134">-WhatIf</span></span>
<span data-ttu-id="b35f1-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b35f1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b35f1-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b35f1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b35f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35f1-137">CommonParameters</span></span>
<span data-ttu-id="b35f1-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b35f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35f1-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b35f1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35f1-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b35f1-140">INPUTS</span></span>

### <span data-ttu-id="b35f1-141">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="b35f1-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="b35f1-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b35f1-142">OUTPUTS</span></span>

### <span data-ttu-id="b35f1-143">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="b35f1-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="b35f1-144">Note</span><span class="sxs-lookup"><span data-stu-id="b35f1-144">NOTES</span></span>

<span data-ttu-id="b35f1-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b35f1-145">ALIASES</span></span>

<span data-ttu-id="b35f1-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b35f1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b35f1-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b35f1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b35f1-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b35f1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b35f1-149">MASTER <IServer> : oggetto server di origine da cui creare la replica.</span><span class="sxs-lookup"><span data-stu-id="b35f1-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="b35f1-150">`Location <String>`: La posizione in cui risiede la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b35f1-150">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="b35f1-151">`[Tag <ITrackedResourceTags>]`: Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="b35f1-151">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="b35f1-152">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="b35f1-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b35f1-153">`[AdministratorLogin <String>]`: Nome di accesso dell'amministratore di un server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="b35f1-154">Può essere specificato solo quando il server viene creato (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="b35f1-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="b35f1-155">`[EarliestRestoreDate <DateTime?>]`: Ora di creazione del punto di ripristino più iniziale (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="b35f1-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="b35f1-156">`[FullyQualifiedDomainName <String>]`: Il nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="b35f1-157">`[IdentityType <IdentityType?>]`: Il tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="b35f1-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="b35f1-158">Imposta questa opzione su' SystemAssigned ' per creare e assegnare automaticamente un Principal di Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b35f1-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="b35f1-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Stato che indica se il server ha abilitato la crittografia dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="b35f1-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="b35f1-160">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="b35f1-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="b35f1-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Applicare una versione TLS minima per il server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="b35f1-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se l'accesso alla rete pubblica è consentito per il server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="b35f1-163">Il valore è facoltativo ma, se passato, deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="b35f1-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="b35f1-164">`[ReplicaCapacity <Int32?>]`: Il numero massimo di repliche che un server master può avere.</span><span class="sxs-lookup"><span data-stu-id="b35f1-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="b35f1-165">`[ReplicationRole <String>]`: Il ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="b35f1-166">`[SkuCapacity <Int32?>]`: La capacità di scala su/fuori, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="b35f1-167">`[SkuFamily <String>]`: La famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="b35f1-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="b35f1-168">`[SkuName <String>]`: Nome della SKU, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="b35f1-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="b35f1-169">`[SkuSize <String>]`: Il codice delle dimensioni, che deve essere interpretato dalla risorsa in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="b35f1-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="b35f1-170">`[SkuTier <SkuTier?>]`: Il livello del particolare SKU, ad esempio Basic.</span><span class="sxs-lookup"><span data-stu-id="b35f1-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="b35f1-171">`[SslEnforcement <SslEnforcementEnum?>]`: Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="b35f1-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="b35f1-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Abilitare il backup Geo-ridondante o meno per il server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="b35f1-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b35f1-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="b35f1-175">`[StorageProfileStorageMb <Int32?>]`: Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="b35f1-176">`[UserVisibleState <ServerState?>]`: Uno stato di un server visibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="b35f1-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="b35f1-177">`[Version <ServerVersion?>]`: Versione server.</span><span class="sxs-lookup"><span data-stu-id="b35f1-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="b35f1-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b35f1-178">RELATED LINKS</span></span>

