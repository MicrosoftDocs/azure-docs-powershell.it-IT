---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 3d36c94ebcc1b733559f9fb4075fb20e4ec67144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686139"
---
# <span data-ttu-id="b0db3-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b0db3-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="b0db3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0db3-102">SYNOPSIS</span></span>
<span data-ttu-id="b0db3-103">Imposta le proprietà per un database o sposta un database esistente in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="b0db3-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0db3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0db3-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0db3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0db3-105">DESCRIPTION</span></span>
<span data-ttu-id="b0db3-106">Il cmdlet **set-AzureRmSqlDatabase** imposta le proprietà per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0db3-106">The **Set-AzureRmSqlDatabase** cmdlet sets properties for an Azure SQL database.</span></span>
<span data-ttu-id="b0db3-107">Inoltre, puoi specificare il parametro *ElasticPoolName* per trasferire un database in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="b0db3-107">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span>
<span data-ttu-id="b0db3-108">Se un database è già in un pool elastico, è possibile usare il parametro *RequestedServiceObjectiveName* per assegnare un livello di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b0db3-108">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to assign a performance level.</span></span>

## <span data-ttu-id="b0db3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0db3-109">EXAMPLES</span></span>

### <span data-ttu-id="b0db3-110">Esempio 1: aggiornare un database in un database S2 standard</span><span class="sxs-lookup"><span data-stu-id="b0db3-110">Example 1: Update a database to a Standard S2 database</span></span>
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

<span data-ttu-id="b0db3-111">Questo comando aggiorna un database denominato Database01 in un database S2 standard in un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="b0db3-111">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="b0db3-112">Esempio 2: aggiungere un database a un pool elastico</span><span class="sxs-lookup"><span data-stu-id="b0db3-112">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="b0db3-113">Questo comando aggiunge un database denominato Database01 al pool elastico denominato ElasticPool01 ospitato nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="b0db3-113">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

## <span data-ttu-id="b0db3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0db3-114">PARAMETERS</span></span>

### <span data-ttu-id="b0db3-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0db3-115">-DatabaseName</span></span>
<span data-ttu-id="b0db3-116">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="b0db3-116">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0db3-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="b0db3-117">-Edition</span></span>
<span data-ttu-id="b0db3-118">Specifica l'edizione per il database.</span><span class="sxs-lookup"><span data-stu-id="b0db3-118">Specifies the edition for the database.</span></span>
<span data-ttu-id="b0db3-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0db3-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b0db3-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b0db3-120">None</span></span>
- <span data-ttu-id="b0db3-121">Premium</span><span class="sxs-lookup"><span data-stu-id="b0db3-121">Premium</span></span>
- <span data-ttu-id="b0db3-122">Base</span><span class="sxs-lookup"><span data-stu-id="b0db3-122">Basic</span></span>
- <span data-ttu-id="b0db3-123">Standard</span><span class="sxs-lookup"><span data-stu-id="b0db3-123">Standard</span></span>
- <span data-ttu-id="b0db3-124">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="b0db3-124">DataWarehouse</span></span>
- <span data-ttu-id="b0db3-125">Gratuito</span><span class="sxs-lookup"><span data-stu-id="b0db3-125">Free</span></span>

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

### <span data-ttu-id="b0db3-126">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b0db3-126">-ElasticPoolName</span></span>
<span data-ttu-id="b0db3-127">Specifica il nome del pool elastico in cui trasferire il database.</span><span class="sxs-lookup"><span data-stu-id="b0db3-127">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="b0db3-128">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="b0db3-128">-MaxSizeBytes</span></span>
<span data-ttu-id="b0db3-129">Specifica le nuove dimensioni massime per il database in byte.</span><span class="sxs-lookup"><span data-stu-id="b0db3-129">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="b0db3-130">Puoi specificare questo parametro o *MaxSizeGB*.</span><span class="sxs-lookup"><span data-stu-id="b0db3-130">You can specify either this parameter or *MaxSizeGB*.</span></span>
<span data-ttu-id="b0db3-131">Vedere il parametro *MaxSizeGB* per i valori accettabili per edizione.</span><span class="sxs-lookup"><span data-stu-id="b0db3-131">See the *MaxSizeGB* parameter for acceptable values per edition.</span></span>

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

### <span data-ttu-id="b0db3-132">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="b0db3-132">-ReadScale</span></span>
<span data-ttu-id="b0db3-133">Opzione Leggi scala per assegnare al database SQL di Azure. (Abilitato/disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b0db3-133">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="b0db3-134">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b0db3-134">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="b0db3-135">Specifica il nome dell'obiettivo del servizio da assegnare al database.</span><span class="sxs-lookup"><span data-stu-id="b0db3-135">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="b0db3-136">Per informazioni sugli obiettivi del servizio, vedere [livelli di servizio database SQL di Azure e livello di prestazioni](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) nella raccolta di Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="b0db3-136">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="b0db3-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0db3-137">-ResourceGroupName</span></span>
<span data-ttu-id="b0db3-138">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="b0db3-138">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b0db3-139">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b0db3-139">-ServerName</span></span>
<span data-ttu-id="b0db3-140">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="b0db3-140">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b0db3-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="b0db3-141">-Tags</span></span>
<span data-ttu-id="b0db3-142">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b0db3-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b0db3-143">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="b0db3-143">For example:</span></span>

<span data-ttu-id="b0db3-144">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b0db3-144">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b0db3-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0db3-145">-Confirm</span></span>
<span data-ttu-id="b0db3-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0db3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0db3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0db3-147">-WhatIf</span></span>
<span data-ttu-id="b0db3-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0db3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0db3-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0db3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0db3-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0db3-150">-DefaultProfile</span></span>
<span data-ttu-id="b0db3-151">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0db3-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0db3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0db3-152">CommonParameters</span></span>
<span data-ttu-id="b0db3-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0db3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0db3-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0db3-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0db3-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0db3-155">INPUTS</span></span>

## <span data-ttu-id="b0db3-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0db3-156">OUTPUTS</span></span>

### <span data-ttu-id="b0db3-157">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b0db3-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b0db3-158">Note</span><span class="sxs-lookup"><span data-stu-id="b0db3-158">NOTES</span></span>

## <span data-ttu-id="b0db3-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0db3-159">RELATED LINKS</span></span>

[<span data-ttu-id="b0db3-160">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b0db3-160">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="b0db3-161">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b0db3-161">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="b0db3-162">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b0db3-162">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="b0db3-163">Curriculum vitae-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b0db3-163">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="b0db3-164">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b0db3-164">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="b0db3-165">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="b0db3-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
