---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: f5fc78f3e06150f3283e35c23bf80edce4f47650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519346"
---
# <span data-ttu-id="ee836-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee836-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="ee836-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee836-102">SYNOPSIS</span></span>
<span data-ttu-id="ee836-103">Crea un database o un database elastico.</span><span class="sxs-lookup"><span data-stu-id="ee836-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee836-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee836-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee836-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee836-105">DESCRIPTION</span></span>
<span data-ttu-id="ee836-106">Il cmdlet **New-AzureRmSqlDatabase** crea un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee836-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="ee836-107">Puoi anche creare un database elastico impostando il parametro *ElasticPoolName* su un pool elastico esistente.</span><span class="sxs-lookup"><span data-stu-id="ee836-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="ee836-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee836-108">EXAMPLES</span></span>

### <span data-ttu-id="ee836-109">Esempio 1: creare un database in un server specificato</span><span class="sxs-lookup"><span data-stu-id="ee836-109">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="ee836-110">Questo comando crea un database denominato Database01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="ee836-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="ee836-111">Esempio 2: creare un database elastico in un server specificato</span><span class="sxs-lookup"><span data-stu-id="ee836-111">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="ee836-112">Questo comando crea un database denominato Database01 nel pool elastico denominato ElasticPool01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="ee836-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="ee836-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee836-113">PARAMETERS</span></span>

### <span data-ttu-id="ee836-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee836-114">-AsJob</span></span>
<span data-ttu-id="ee836-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ee836-115">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="ee836-116">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="ee836-116">-CatalogCollation</span></span>
<span data-ttu-id="ee836-117">Specifica il nome delle regole di confronto del catalogo di database SQL.</span><span class="sxs-lookup"><span data-stu-id="ee836-117">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee836-118">-CollationName</span><span class="sxs-lookup"><span data-stu-id="ee836-118">-CollationName</span></span>
<span data-ttu-id="ee836-119">Specifica il nome delle regole di confronto del database SQL.</span><span class="sxs-lookup"><span data-stu-id="ee836-119">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee836-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee836-120">-DatabaseName</span></span>
<span data-ttu-id="ee836-121">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="ee836-121">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee836-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee836-122">-DefaultProfile</span></span>
<span data-ttu-id="ee836-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ee836-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee836-124">-Edition</span><span class="sxs-lookup"><span data-stu-id="ee836-124">-Edition</span></span>
<span data-ttu-id="ee836-125">Specifica l'edizione da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="ee836-125">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="ee836-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee836-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ee836-127">Predefinita</span><span class="sxs-lookup"><span data-stu-id="ee836-127">Default</span></span>
- <span data-ttu-id="ee836-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ee836-128">None</span></span>
- <span data-ttu-id="ee836-129">Premium</span><span class="sxs-lookup"><span data-stu-id="ee836-129">Premium</span></span>
- <span data-ttu-id="ee836-130">Base</span><span class="sxs-lookup"><span data-stu-id="ee836-130">Basic</span></span>
- <span data-ttu-id="ee836-131">Standard</span><span class="sxs-lookup"><span data-stu-id="ee836-131">Standard</span></span>
- <span data-ttu-id="ee836-132">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="ee836-132">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee836-133">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ee836-133">-ElasticPoolName</span></span>
<span data-ttu-id="ee836-134">Specifica il nome del pool elastico in cui inserire il database.</span><span class="sxs-lookup"><span data-stu-id="ee836-134">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee836-135">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="ee836-135">-MaxSizeBytes</span></span>
<span data-ttu-id="ee836-136">Specifica la dimensione massima del database in byte.</span><span class="sxs-lookup"><span data-stu-id="ee836-136">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee836-137">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="ee836-137">-ReadScale</span></span>
<span data-ttu-id="ee836-138">Opzione Leggi scala per assegnare al database SQL di Azure. (Abilitato/disabilitato)</span><span class="sxs-lookup"><span data-stu-id="ee836-138">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee836-139">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ee836-139">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="ee836-140">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="ee836-140">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee836-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee836-141">-ResourceGroupName</span></span>
<span data-ttu-id="ee836-142">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="ee836-142">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ee836-143">-Samplename</span><span class="sxs-lookup"><span data-stu-id="ee836-143">-SampleName</span></span>
<span data-ttu-id="ee836-144">Nome dello schema di esempio da applicare quando si crea questo database.</span><span class="sxs-lookup"><span data-stu-id="ee836-144">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee836-145">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ee836-145">-ServerName</span></span>
<span data-ttu-id="ee836-146">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="ee836-146">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ee836-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee836-147">-Tags</span></span>
<span data-ttu-id="ee836-148">Specifica un dizionario di coppie chiave-valore in forma di tabella hash che questo cmdlet associa al nuovo database.</span><span class="sxs-lookup"><span data-stu-id="ee836-148">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="ee836-149">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="ee836-149">For example:</span></span>

<span data-ttu-id="ee836-150">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ee836-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee836-151">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="ee836-151">-ZoneRedundant</span></span>
<span data-ttu-id="ee836-152">Ridondanza della zona da associare al database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="ee836-152">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="ee836-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee836-153">-Confirm</span></span>
<span data-ttu-id="ee836-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee836-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee836-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee836-155">-WhatIf</span></span>
<span data-ttu-id="ee836-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee836-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee836-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee836-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee836-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee836-158">CommonParameters</span></span>
<span data-ttu-id="ee836-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee836-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee836-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee836-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee836-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee836-161">INPUTS</span></span>

### <span data-ttu-id="ee836-162">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ee836-162">None</span></span>
<span data-ttu-id="ee836-163">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ee836-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee836-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee836-164">OUTPUTS</span></span>

### <span data-ttu-id="ee836-165">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ee836-165">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ee836-166">Note</span><span class="sxs-lookup"><span data-stu-id="ee836-166">NOTES</span></span>

## <span data-ttu-id="ee836-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee836-167">RELATED LINKS</span></span>

[<span data-ttu-id="ee836-168">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee836-168">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="ee836-169">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ee836-169">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ee836-170">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="ee836-170">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="ee836-171">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee836-171">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="ee836-172">Curriculum vitae-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee836-172">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="ee836-173">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee836-173">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="ee836-174">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee836-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="ee836-175">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="ee836-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
