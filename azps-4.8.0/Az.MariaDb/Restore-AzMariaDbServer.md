---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033014"
---
# <span data-ttu-id="1f4de-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="1f4de-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="1f4de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f4de-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4de-103">Ripristinare un MariaDB da un MariaDB esistente.</span><span class="sxs-lookup"><span data-stu-id="1f4de-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="1f4de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f4de-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f4de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f4de-105">DESCRIPTION</span></span>
<span data-ttu-id="1f4de-106">Ripristinare un MariaDB da un MariaDB esistente.</span><span class="sxs-lookup"><span data-stu-id="1f4de-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="1f4de-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f4de-107">EXAMPLES</span></span>

### <span data-ttu-id="1f4de-108">Esempio 1: ripristinare un PointInTime MariaDB in base al nome del server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="1f4de-109">Questo comando ripristina un PointInTime MariaDB in base al nome del server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="1f4de-110">Esempio 2: ripristinare un oggetto PointInTime MariaDB per server</span><span class="sxs-lookup"><span data-stu-id="1f4de-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="1f4de-111">Questo comando ripristina un oggetto PointInTime MariaDB per server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="1f4de-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f4de-112">PARAMETERS</span></span>

### <span data-ttu-id="1f4de-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f4de-113">-AsJob</span></span>
<span data-ttu-id="1f4de-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="1f4de-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1f4de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4de-115">-DefaultProfile</span></span>
<span data-ttu-id="1f4de-116">Region DefaultParameters le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f4de-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f4de-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f4de-117">-InputObject</span></span>
<span data-ttu-id="1f4de-118">Oggetto server di origine da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="1f4de-118">The source server object to restore from.</span></span>
<span data-ttu-id="1f4de-119">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1f4de-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1f4de-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1f4de-120">-Location</span></span>
<span data-ttu-id="1f4de-121">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f4de-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="1f4de-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f4de-122">-Name</span></span>
<span data-ttu-id="1f4de-123">Il nome del server di destinazione da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="1f4de-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="1f4de-124">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="1f4de-124">-NoWait</span></span>
<span data-ttu-id="1f4de-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="1f4de-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1f4de-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4de-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f4de-127">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f4de-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1f4de-128">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="1f4de-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1f4de-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="1f4de-129">-RestorePointInTime</span></span>
<span data-ttu-id="1f4de-130">area geografica PointInTimeRestore la posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f4de-130">region PointInTimeRestore The location the resource resides in.</span></span>

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

### <span data-ttu-id="1f4de-131">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1f4de-131">-ServerName</span></span>
<span data-ttu-id="1f4de-132">Il nome del server di origine da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="1f4de-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="1f4de-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f4de-133">-SubscriptionId</span></span>
<span data-ttu-id="1f4de-134">Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1f4de-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1f4de-135">L'ID abbonamento fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1f4de-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1f4de-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f4de-136">-Tag</span></span>
<span data-ttu-id="1f4de-137">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="1f4de-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="1f4de-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f4de-138">-Confirm</span></span>
<span data-ttu-id="1f4de-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f4de-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f4de-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f4de-140">-WhatIf</span></span>
<span data-ttu-id="1f4de-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f4de-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f4de-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f4de-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f4de-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4de-143">CommonParameters</span></span>
<span data-ttu-id="1f4de-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f4de-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4de-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f4de-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4de-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f4de-146">INPUTS</span></span>

### <span data-ttu-id="1f4de-147">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="1f4de-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="1f4de-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f4de-148">OUTPUTS</span></span>

### <span data-ttu-id="1f4de-149">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="1f4de-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="1f4de-150">Note</span><span class="sxs-lookup"><span data-stu-id="1f4de-150">NOTES</span></span>

<span data-ttu-id="1f4de-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1f4de-151">ALIASES</span></span>

<span data-ttu-id="1f4de-152">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f4de-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1f4de-153">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1f4de-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f4de-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f4de-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1f4de-155">INPUTOBJECT <IServer> : l'oggetto server di origine da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="1f4de-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="1f4de-156">`Location <String>`: La posizione in cui risiede la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f4de-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="1f4de-157">`[Tag <ITrackedResourceTags>]`: Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="1f4de-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="1f4de-158">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="1f4de-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="1f4de-159">`[AdministratorLogin <String>]`: Nome di accesso dell'amministratore di un server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="1f4de-160">Può essere specificato solo quando il server viene creato (ed è necessario per la creazione).</span><span class="sxs-lookup"><span data-stu-id="1f4de-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="1f4de-161">`[EarliestRestoreDate <DateTime?>]`: Ora di creazione del punto di ripristino più iniziale (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="1f4de-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="1f4de-162">`[FullyQualifiedDomainName <String>]`: Il nome di dominio completo di un server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="1f4de-163">`[IdentityType <IdentityType?>]`: Il tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="1f4de-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="1f4de-164">Imposta questa opzione su' SystemAssigned ' per creare e assegnare automaticamente un Principal di Azure Active Directory per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f4de-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="1f4de-165">`[MasterServerId <String>]`: ID server master di un server di replica.</span><span class="sxs-lookup"><span data-stu-id="1f4de-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="1f4de-166">`[ReplicaCapacity <Int32?>]`: Il numero massimo di repliche che un server master può avere.</span><span class="sxs-lookup"><span data-stu-id="1f4de-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="1f4de-167">`[ReplicationRole <String>]`: Il ruolo di replica del server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="1f4de-168">`[SkuCapacity <Int32?>]`: La capacità di scala su/fuori, che rappresenta le unità di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="1f4de-169">`[SkuFamily <String>]`: La famiglia di hardware.</span><span class="sxs-lookup"><span data-stu-id="1f4de-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="1f4de-170">`[SkuName <String>]`: Nome della SKU, in genere, livello + famiglia + Core, ad esempio B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="1f4de-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="1f4de-171">`[SkuSize <String>]`: Il codice delle dimensioni, che deve essere interpretato dalla risorsa in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="1f4de-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="1f4de-172">`[SkuTier <SkuTier?>]`: Il livello del particolare SKU, ad esempio Basic.</span><span class="sxs-lookup"><span data-stu-id="1f4de-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="1f4de-173">`[SslEnforcement <SslEnforcementEnum?>]`: Abilitare l'applicazione SSL o meno quando si connette al server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="1f4de-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="1f4de-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Abilitare il backup Geo-ridondante o meno per il server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="1f4de-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Abilitare l'espansione automatica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1f4de-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="1f4de-177">`[StorageProfileStorageMb <Int32?>]`: Spazio di archiviazione max consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="1f4de-178">`[UserVisibleState <ServerState?>]`: Uno stato di un server visibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="1f4de-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="1f4de-179">`[Version <ServerVersion?>]`: Versione server.</span><span class="sxs-lookup"><span data-stu-id="1f4de-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="1f4de-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f4de-180">RELATED LINKS</span></span>

