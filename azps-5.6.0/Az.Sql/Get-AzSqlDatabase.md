---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: 24e6d0f96114f6843b5af48fafe6d58cc7b49126
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993242"
---
# <span data-ttu-id="bbdc1-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbdc1-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="bbdc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbdc1-102">SYNOPSIS</span></span>
<span data-ttu-id="bbdc1-103">Ottiene uno o più database.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-103">Gets one or more databases.</span></span>

## <span data-ttu-id="bbdc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbdc1-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbdc1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bbdc1-105">DESCRIPTION</span></span>
<span data-ttu-id="bbdc1-106">Il cmdlet **Get-AzSqlDatabase** ottiene uno o più database SQL Azure da un server di database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="bbdc1-107">Questo cmdlet è supportato anche dal servizio SQL Server stretch database in Azure.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bbdc1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbdc1-108">EXAMPLES</span></span>

### <span data-ttu-id="bbdc1-109">Esempio 1: Recuperare tutti i database in un server</span><span class="sxs-lookup"><span data-stu-id="bbdc1-109">Example 1: Get all databases on a server</span></span>
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

<span data-ttu-id="bbdc1-110">Questo comando recupera tutti i database nel server denominato server01.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="bbdc1-111">Esempio 2: Ottenere un database in base al nome in un server</span><span class="sxs-lookup"><span data-stu-id="bbdc1-111">Example 2: Get a database by name on a server</span></span>
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

<span data-ttu-id="bbdc1-112">Questo comando recupera un database denominato Database02 da un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="bbdc1-113">Esempio 3: Recuperare tutti i database in un server usando i filtri</span><span class="sxs-lookup"><span data-stu-id="bbdc1-113">Example 3: Get all databases on a server using filtering</span></span>
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

<span data-ttu-id="bbdc1-114">Questo comando recupera tutti i database nel server denominato server01 che iniziano con "database".</span><span class="sxs-lookup"><span data-stu-id="bbdc1-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="bbdc1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbdc1-115">PARAMETERS</span></span>

### <span data-ttu-id="bbdc1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bbdc1-116">-DatabaseName</span></span>
<span data-ttu-id="bbdc1-117">Specifica il nome del database da recuperare.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-117">Specifies the name of the database to retrieve.</span></span>

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

### <span data-ttu-id="bbdc1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbdc1-118">-DefaultProfile</span></span>
<span data-ttu-id="bbdc1-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bbdc1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbdc1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbdc1-120">-ResourceGroupName</span></span>
<span data-ttu-id="bbdc1-121">Specifica il nome del gruppo di risorse a cui è assegnato il server di database.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="bbdc1-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bbdc1-122">-ServerName</span></span>
<span data-ttu-id="bbdc1-123">Specifica il nome del server a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-123">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="bbdc1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbdc1-124">-Confirm</span></span>
<span data-ttu-id="bbdc1-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbdc1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbdc1-126">-WhatIf</span></span>
<span data-ttu-id="bbdc1-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbdc1-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbdc1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbdc1-129">CommonParameters</span></span>
<span data-ttu-id="bbdc1-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbdc1-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bbdc1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbdc1-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="bbdc1-132">INPUTS</span></span>

### <span data-ttu-id="bbdc1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bbdc1-133">System.String</span></span>

## <span data-ttu-id="bbdc1-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbdc1-134">OUTPUTS</span></span>

### <span data-ttu-id="bbdc1-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bbdc1-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="bbdc1-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="bbdc1-136">NOTES</span></span>

## <span data-ttu-id="bbdc1-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbdc1-137">RELATED LINKS</span></span>

[<span data-ttu-id="bbdc1-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbdc1-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="bbdc1-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbdc1-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="bbdc1-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbdc1-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="bbdc1-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbdc1-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="bbdc1-142">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbdc1-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)


