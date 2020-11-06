---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: b0493433f7419039acacd696748b3c5f9518aef5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512184"
---
# <span data-ttu-id="f773f-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f773f-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="f773f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f773f-102">SYNOPSIS</span></span>
<span data-ttu-id="f773f-103">Imposta le proprietà per un database o sposta un database esistente in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="f773f-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f773f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f773f-104">SYNTAX</span></span>

### <span data-ttu-id="f773f-105">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="f773f-105">Update</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f773f-106">Rinominare</span><span class="sxs-lookup"><span data-stu-id="f773f-106">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f773f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f773f-107">DESCRIPTION</span></span>
<span data-ttu-id="f773f-108">Il cmdlet **set-AzureRmSqlDatabase** imposta le proprietà per un database in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="f773f-108">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="f773f-109">Questo cmdlet può modificare il livello di servizio ( *edizione* ), le prestazioni ( *RequestedServiceObjectiveName* ) e le dimensioni massime di archiviazione ( *MaxSizeBytes* ) per il database.</span><span class="sxs-lookup"><span data-stu-id="f773f-109">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="f773f-110">Inoltre, puoi specificare il parametro *ElasticPoolName* per trasferire un database in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="f773f-110">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="f773f-111">Se un database è già in un pool elastico, è possibile usare il parametro *RequestedServiceObjectiveName* per trasferire il database da un pool elastico e in un livello di prestazioni per i singoli database.</span><span class="sxs-lookup"><span data-stu-id="f773f-111">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="f773f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f773f-112">EXAMPLES</span></span>

### <span data-ttu-id="f773f-113">Esempio 1: aggiornare un database in un database S2 standard</span><span class="sxs-lookup"><span data-stu-id="f773f-113">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="f773f-114">Questo comando aggiorna un database denominato Database01 in un database S2 standard in un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="f773f-114">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="f773f-115">Esempio 2: aggiungere un database a un pool elastico</span><span class="sxs-lookup"><span data-stu-id="f773f-115">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="f773f-116">Questo comando aggiunge un database denominato Database01 al pool elastico denominato ElasticPool01 ospitato nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="f773f-116">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="f773f-117">Esempio 3: modificare le dimensioni massime di archiviazione di un database</span><span class="sxs-lookup"><span data-stu-id="f773f-117">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="f773f-118">Questo comando aggiorna un database denominato Database01 per impostare la dimensione massima su 1 TB.</span><span class="sxs-lookup"><span data-stu-id="f773f-118">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="f773f-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f773f-119">PARAMETERS</span></span>

### <span data-ttu-id="f773f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f773f-120">-AsJob</span></span>
<span data-ttu-id="f773f-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f773f-121">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f773f-122">-DatabaseName</span></span>
<span data-ttu-id="f773f-123">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="f773f-123">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f773f-124">-DefaultProfile</span></span>
<span data-ttu-id="f773f-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f773f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-126">-Edition</span><span class="sxs-lookup"><span data-stu-id="f773f-126">-Edition</span></span>
<span data-ttu-id="f773f-127">Specifica l'edizione per il database.</span><span class="sxs-lookup"><span data-stu-id="f773f-127">Specifies the edition for the database.</span></span>
<span data-ttu-id="f773f-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f773f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f773f-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f773f-129">None</span></span>
- <span data-ttu-id="f773f-130">Premium</span><span class="sxs-lookup"><span data-stu-id="f773f-130">Premium</span></span>
- <span data-ttu-id="f773f-131">Base</span><span class="sxs-lookup"><span data-stu-id="f773f-131">Basic</span></span>
- <span data-ttu-id="f773f-132">Standard</span><span class="sxs-lookup"><span data-stu-id="f773f-132">Standard</span></span>
- <span data-ttu-id="f773f-133">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="f773f-133">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: Update
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-134">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f773f-134">-ElasticPoolName</span></span>
<span data-ttu-id="f773f-135">Specifica il nome del pool elastico in cui trasferire il database.</span><span class="sxs-lookup"><span data-stu-id="f773f-135">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-136">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="f773f-136">-MaxSizeBytes</span></span>
<span data-ttu-id="f773f-137">Dimensione massima del database SQL di Azure in byte.</span><span class="sxs-lookup"><span data-stu-id="f773f-137">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-138">-NewName</span><span class="sxs-lookup"><span data-stu-id="f773f-138">-NewName</span></span>
<span data-ttu-id="f773f-139">Nuovo nome a cui rinominare il database.</span><span class="sxs-lookup"><span data-stu-id="f773f-139">The new name to rename the database to.</span></span>

```yaml
Type: String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-140">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="f773f-140">-ReadScale</span></span>
<span data-ttu-id="f773f-141">Opzione Leggi scala per assegnare al database SQL di Azure. (Abilitato/disabilitato)</span><span class="sxs-lookup"><span data-stu-id="f773f-141">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: Update
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-142">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="f773f-142">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="f773f-143">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="f773f-143">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="f773f-144">Per informazioni sugli obiettivi del servizio, vedere [livelli di servizio database SQL di Azure e livello di prestazioni](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) nella raccolta di Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="f773f-144">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f773f-145">-ResourceGroupName</span></span>
<span data-ttu-id="f773f-146">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="f773f-146">Specifies the name of resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-147">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f773f-147">-ServerName</span></span>
<span data-ttu-id="f773f-148">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="f773f-148">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="f773f-149">-Tags</span></span>
<span data-ttu-id="f773f-150">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f773f-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f773f-151">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="f773f-151">For example:</span></span>

<span data-ttu-id="f773f-152">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f773f-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Update
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-153">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="f773f-153">-ZoneRedundant</span></span>
<span data-ttu-id="f773f-154">Ridondanza della zona da associare al database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="f773f-154">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f773f-155">-Confirm</span></span>
<span data-ttu-id="f773f-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f773f-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f773f-157">-WhatIf</span></span>
<span data-ttu-id="f773f-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f773f-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f773f-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f773f-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f773f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f773f-160">CommonParameters</span></span>
<span data-ttu-id="f773f-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f773f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f773f-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f773f-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f773f-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f773f-163">INPUTS</span></span>

### <span data-ttu-id="f773f-164">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f773f-164">None</span></span>
<span data-ttu-id="f773f-165">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f773f-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f773f-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f773f-166">OUTPUTS</span></span>

### <span data-ttu-id="f773f-167">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f773f-167">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f773f-168">Note</span><span class="sxs-lookup"><span data-stu-id="f773f-168">NOTES</span></span>

## <span data-ttu-id="f773f-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f773f-169">RELATED LINKS</span></span>

[<span data-ttu-id="f773f-170">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f773f-170">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="f773f-171">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f773f-171">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="f773f-172">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f773f-172">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="f773f-173">Curriculum vitae-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f773f-173">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="f773f-174">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f773f-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="f773f-175">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="f773f-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
