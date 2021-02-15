---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207178"
---
# <span data-ttu-id="0a6af-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="0a6af-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="0a6af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a6af-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6af-103">Ripristinare un database mariadb da un database di MariaDB esistente.</span><span class="sxs-lookup"><span data-stu-id="0a6af-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="0a6af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a6af-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0a6af-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0a6af-105">DESCRIPTION</span></span>
<span data-ttu-id="0a6af-106">Ripristinare un database mariadb da un database di MariaDB esistente.</span><span class="sxs-lookup"><span data-stu-id="0a6af-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="0a6af-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a6af-107">EXAMPLES</span></span>

### <span data-ttu-id="0a6af-108">Esempio 1: Ripristinare un database di PointInTime in base al nome del server.</span><span class="sxs-lookup"><span data-stu-id="0a6af-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0a6af-109">Questo comando consente di ripristinare un database di PointInTime in base al nome del server.</span><span class="sxs-lookup"><span data-stu-id="0a6af-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="0a6af-110">Esempio 2: Ripristinare un database di PointInTime in base a un oggetto server</span><span class="sxs-lookup"><span data-stu-id="0a6af-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0a6af-111">Questo comando consente di ripristinare un oggetto server di PointInTime MariaDB.</span><span class="sxs-lookup"><span data-stu-id="0a6af-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="0a6af-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a6af-112">PARAMETERS</span></span>

### <span data-ttu-id="0a6af-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a6af-113">-AsJob</span></span>
<span data-ttu-id="0a6af-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="0a6af-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0a6af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6af-115">-DefaultProfile</span></span>
<span data-ttu-id="0a6af-116">region DefaultParameters Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6af-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a6af-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a6af-117">-InputObject</span></span>
<span data-ttu-id="0a6af-118">Oggetto server di origine da cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="0a6af-118">The source server object to restore from.</span></span>
<span data-ttu-id="0a6af-119">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0a6af-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6af-120">-Location</span><span class="sxs-lookup"><span data-stu-id="0a6af-120">-Location</span></span>
<span data-ttu-id="0a6af-121">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a6af-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="0a6af-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0a6af-122">-Name</span></span>
<span data-ttu-id="0a6af-123">Nome del server da cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="0a6af-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="0a6af-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0a6af-124">-NoWait</span></span>
<span data-ttu-id="0a6af-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="0a6af-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0a6af-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6af-126">-ResourceGroupName</span></span>
<span data-ttu-id="0a6af-127">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a6af-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0a6af-128">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="0a6af-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0a6af-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="0a6af-129">-RestorePointInTime</span></span>
<span data-ttu-id="0a6af-130">region PointInTimeRestore La posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a6af-130">region PointInTimeRestore The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6af-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0a6af-131">-ServerName</span></span>
<span data-ttu-id="0a6af-132">Nome del server di origine da cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="0a6af-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="0a6af-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a6af-133">-SubscriptionId</span></span>
<span data-ttu-id="0a6af-134">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6af-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0a6af-135">L'ID sottoscrizione fa parte dell'URI di ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0a6af-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0a6af-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a6af-136">-Tag</span></span>
<span data-ttu-id="0a6af-137">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="0a6af-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="0a6af-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a6af-138">-Confirm</span></span>
<span data-ttu-id="0a6af-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a6af-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a6af-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a6af-140">-WhatIf</span></span>
<span data-ttu-id="0a6af-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a6af-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a6af-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a6af-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a6af-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6af-143">CommonParameters</span></span>
<span data-ttu-id="0a6af-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6af-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6af-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0a6af-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6af-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="0a6af-146">INPUTS</span></span>

### <span data-ttu-id="0a6af-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="0a6af-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="0a6af-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a6af-148">OUTPUTS</span></span>

### <span data-ttu-id="0a6af-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="0a6af-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="0a6af-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="0a6af-150">NOTES</span></span>

<span data-ttu-id="0a6af-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0a6af-151">ALIASES</span></span>

<span data-ttu-id="0a6af-152">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0a6af-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a6af-153">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0a6af-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a6af-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0a6af-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a6af-155"><IServer>INPUTOBJECT: oggetto server di origine da cui eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="0a6af-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="0a6af-156">`Location <String>`: la posizione in cui risiede la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a6af-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="0a6af-157">`[Tag <ITrackedResourceTags>]`: metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="0a6af-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="0a6af-158">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0a6af-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0a6af-159">`[AdministratorLogin <String>]`: nome di accesso di un server da parte dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="0a6af-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="0a6af-160">Può essere specificato solo durante la creazione del server (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="0a6af-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="0a6af-161">`[EarliestRestoreDate <DateTime?>]`: il primo momento di creazione del punto di ripristino (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="0a6af-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="0a6af-162">`[FullyQualifiedDomainName <String>]`: nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="0a6af-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="0a6af-163">`[IdentityType <IdentityType?>]`: tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="0a6af-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="0a6af-164">Impostare questo valore su "SystemAssigned" per creare e assegnare automaticamente un'entità Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a6af-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="0a6af-165">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="0a6af-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="0a6af-166">`[ReplicaCapacity <Int32?>]`: numero massimo di replica consentite a un server master.</span><span class="sxs-lookup"><span data-stu-id="0a6af-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="0a6af-167">`[ReplicationRole <String>]`: ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="0a6af-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="0a6af-168">`[SkuCapacity <Int32?>]`: la capacità di scalabilità in orizzontale, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="0a6af-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="0a6af-169">`[SkuFamily <String>]`: famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="0a6af-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="0a6af-170">`[SkuName <String>]`: il nome della SKU, in genere livello + famiglia + core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0a6af-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="0a6af-171">`[SkuSize <String>]`: il codice delle dimensioni, che deve essere interpretato dalla risorsa nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="0a6af-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="0a6af-172">`[SkuTier <SkuTier?>]`: il livello dello specifico SKU, ad esempio Di base.</span><span class="sxs-lookup"><span data-stu-id="0a6af-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="0a6af-173">`[SslEnforcement <SslEnforcementEnum?>]`: per abilitare o meno l'applicazione del ssl quando ci si connette al server.</span><span class="sxs-lookup"><span data-stu-id="0a6af-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="0a6af-174">`[StorageProfileBackupRetentionDay <Int32?>]`: giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="0a6af-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="0a6af-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: abilitare o meno la ridondanza geografica per il backup del server.</span><span class="sxs-lookup"><span data-stu-id="0a6af-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="0a6af-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: per abilitare l'estensione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0a6af-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="0a6af-177">`[StorageProfileStorageMb <Int32?>]`: spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="0a6af-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="0a6af-178">`[UserVisibleState <ServerState?>]`: stato di un server visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="0a6af-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="0a6af-179">`[Version <ServerVersion?>]`: versione del server.</span><span class="sxs-lookup"><span data-stu-id="0a6af-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="0a6af-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a6af-180">RELATED LINKS</span></span>

