---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 22b74b3dcd76577d7c864a3779d12c8474c431a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510259"
---
# <span data-ttu-id="4d1cf-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4d1cf-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="4d1cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d1cf-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1cf-103">Crea un database o un database elastico.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d1cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d1cf-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d1cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d1cf-105">DESCRIPTION</span></span>
<span data-ttu-id="4d1cf-106">Il cmdlet **New-AzureRmSqlDatabase** crea un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="4d1cf-107">Puoi anche creare un database elastico impostando il parametro *ElasticPoolName* su un pool elastico esistente.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="4d1cf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d1cf-108">EXAMPLES</span></span>

### <span data-ttu-id="4d1cf-109">Esempio 1: creare un database in un server specificato</span><span class="sxs-lookup"><span data-stu-id="4d1cf-109">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="4d1cf-110">Questo comando crea un database denominato Database01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="4d1cf-111">Esempio 2: creare un database elastico in un server specificato</span><span class="sxs-lookup"><span data-stu-id="4d1cf-111">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="4d1cf-112">Questo comando crea un database denominato Database01 nel pool elastico denominato ElasticPool01 nel server Server01.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="4d1cf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d1cf-113">PARAMETERS</span></span>

### <span data-ttu-id="4d1cf-114">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="4d1cf-114">-CatalogCollation</span></span>
<span data-ttu-id="4d1cf-115">Specifica il nome delle regole di confronto del catalogo di database SQL.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-115">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="4d1cf-116">-CollationName</span><span class="sxs-lookup"><span data-stu-id="4d1cf-116">-CollationName</span></span>
<span data-ttu-id="4d1cf-117">Specifica il nome delle regole di confronto del database SQL.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-117">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="4d1cf-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4d1cf-118">-DatabaseName</span></span>
<span data-ttu-id="4d1cf-119">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-119">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cf-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="4d1cf-120">-Edition</span></span>
<span data-ttu-id="4d1cf-121">Specifica l'edizione da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-121">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="4d1cf-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d1cf-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4d1cf-123">Predefinita</span><span class="sxs-lookup"><span data-stu-id="4d1cf-123">Default</span></span>
- <span data-ttu-id="4d1cf-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4d1cf-124">None</span></span>
- <span data-ttu-id="4d1cf-125">Premium</span><span class="sxs-lookup"><span data-stu-id="4d1cf-125">Premium</span></span>
- <span data-ttu-id="4d1cf-126">Base</span><span class="sxs-lookup"><span data-stu-id="4d1cf-126">Basic</span></span>
- <span data-ttu-id="4d1cf-127">Standard</span><span class="sxs-lookup"><span data-stu-id="4d1cf-127">Standard</span></span>
- <span data-ttu-id="4d1cf-128">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="4d1cf-128">DataWarehouse</span></span>
- <span data-ttu-id="4d1cf-129">Gratuito</span><span class="sxs-lookup"><span data-stu-id="4d1cf-129">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cf-130">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4d1cf-130">-ElasticPoolName</span></span>
<span data-ttu-id="4d1cf-131">Specifica il nome del pool elastico in cui inserire il database.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-131">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="4d1cf-132">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="4d1cf-132">-MaxSizeBytes</span></span>
<span data-ttu-id="4d1cf-133">Specifica la dimensione massima del database in byte.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-133">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cf-134">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="4d1cf-134">-ReadScale</span></span>
<span data-ttu-id="4d1cf-135">Opzione Leggi scala per assegnare al database SQL di Azure. (Abilitato/disabilitato)</span><span class="sxs-lookup"><span data-stu-id="4d1cf-135">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cf-136">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="4d1cf-136">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="4d1cf-137">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-137">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="4d1cf-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d1cf-138">-ResourceGroupName</span></span>
<span data-ttu-id="4d1cf-139">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-139">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cf-140">-Samplename</span><span class="sxs-lookup"><span data-stu-id="4d1cf-140">-SampleName</span></span>
<span data-ttu-id="4d1cf-141">Nome dello schema di esempio da applicare quando si crea questo database.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-141">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cf-142">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4d1cf-142">-ServerName</span></span>
<span data-ttu-id="4d1cf-143">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-143">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cf-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d1cf-144">-Tags</span></span>
<span data-ttu-id="4d1cf-145">Specifica un dizionario di coppie chiave-valore in forma di tabella hash che questo cmdlet associa al nuovo database.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-145">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="4d1cf-146">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="4d1cf-146">For example:</span></span>

<span data-ttu-id="4d1cf-147">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4d1cf-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cf-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d1cf-148">-Confirm</span></span>
<span data-ttu-id="4d1cf-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cf-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d1cf-150">-WhatIf</span></span>
<span data-ttu-id="4d1cf-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d1cf-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cf-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1cf-153">-DefaultProfile</span></span>
<span data-ttu-id="4d1cf-154">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1cf-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1cf-155">CommonParameters</span></span>
<span data-ttu-id="4d1cf-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d1cf-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1cf-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d1cf-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1cf-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d1cf-158">INPUTS</span></span>

## <span data-ttu-id="4d1cf-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d1cf-159">OUTPUTS</span></span>

### <span data-ttu-id="4d1cf-160">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4d1cf-160">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="4d1cf-161">Note</span><span class="sxs-lookup"><span data-stu-id="4d1cf-161">NOTES</span></span>

## <span data-ttu-id="4d1cf-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d1cf-162">RELATED LINKS</span></span>

[<span data-ttu-id="4d1cf-163">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4d1cf-163">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="4d1cf-164">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4d1cf-164">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4d1cf-165">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="4d1cf-165">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="4d1cf-166">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4d1cf-166">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="4d1cf-167">Curriculum vitae-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4d1cf-167">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="4d1cf-168">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4d1cf-168">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="4d1cf-169">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4d1cf-169">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="4d1cf-170">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4d1cf-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
