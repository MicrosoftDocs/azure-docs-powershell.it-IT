---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: 4f90d6d0c33874750bf2f32ae7f65bf32457f63c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019532"
---
# <span data-ttu-id="ee9a3-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee9a3-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="ee9a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ee9a3-103">Ottiene uno o più database.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-103">Gets one or more databases.</span></span>

## <span data-ttu-id="ee9a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee9a3-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee9a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee9a3-105">DESCRIPTION</span></span>
<span data-ttu-id="ee9a3-106">Il cmdlet **Get-AzSqlDatabase** ottiene uno o più database SQL di Azure da un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="ee9a3-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ee9a3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee9a3-108">EXAMPLES</span></span>

### <span data-ttu-id="ee9a3-109">Esempio 1: ottenere tutti i database in un server</span><span class="sxs-lookup"><span data-stu-id="ee9a3-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : master
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
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

<span data-ttu-id="ee9a3-110">Questo comando consente di ottenere tutti i database nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="ee9a3-111">Esempio 2: ottenere un database per nome in un server</span><span class="sxs-lookup"><span data-stu-id="ee9a3-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
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

<span data-ttu-id="ee9a3-112">Questo comando consente di ottenere un database denominato Database02 da un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="ee9a3-113">Esempio 3: ottenere tutti i database in un server tramite filtro</span><span class="sxs-lookup"><span data-stu-id="ee9a3-113">Example 3: Get all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database*"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
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

<span data-ttu-id="ee9a3-114">Questo comando consente di ottenere tutti i database nel server di nome Server01 che iniziano con "database".</span><span class="sxs-lookup"><span data-stu-id="ee9a3-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="ee9a3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee9a3-115">PARAMETERS</span></span>

### <span data-ttu-id="ee9a3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee9a3-116">-DatabaseName</span></span>
<span data-ttu-id="ee9a3-117">Specifica il nome del database da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee9a3-118">-DefaultProfile</span></span>
<span data-ttu-id="ee9a3-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ee9a3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9a3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee9a3-120">-ResourceGroupName</span></span>
<span data-ttu-id="ee9a3-121">Specifica il nome del gruppo di risorse a cui è assegnato il server di database.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="ee9a3-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ee9a3-122">-ServerName</span></span>
<span data-ttu-id="ee9a3-123">Specifica il nome del server a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-123">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="ee9a3-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee9a3-124">-Confirm</span></span>
<span data-ttu-id="ee9a3-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee9a3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee9a3-126">-WhatIf</span></span>
<span data-ttu-id="ee9a3-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee9a3-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee9a3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9a3-129">CommonParameters</span></span>
<span data-ttu-id="ee9a3-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee9a3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9a3-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee9a3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9a3-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee9a3-132">INPUTS</span></span>

### <span data-ttu-id="ee9a3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ee9a3-133">System.String</span></span>

## <span data-ttu-id="ee9a3-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee9a3-134">OUTPUTS</span></span>

### <span data-ttu-id="ee9a3-135">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ee9a3-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ee9a3-136">Note</span><span class="sxs-lookup"><span data-stu-id="ee9a3-136">NOTES</span></span>

## <span data-ttu-id="ee9a3-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee9a3-137">RELATED LINKS</span></span>

[<span data-ttu-id="ee9a3-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee9a3-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="ee9a3-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee9a3-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="ee9a3-140">Curriculum vitae-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee9a3-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="ee9a3-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee9a3-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="ee9a3-142">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee9a3-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)


