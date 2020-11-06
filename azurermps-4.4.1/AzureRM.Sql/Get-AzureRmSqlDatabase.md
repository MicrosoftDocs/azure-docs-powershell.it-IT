---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
ms.openlocfilehash: 9ae96035a4257826ac92dc6dbae75282debf08a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521517"
---
# <span data-ttu-id="4e3d8-101">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4e3d8-101">Get-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="4e3d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e3d8-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3d8-103">Ottiene uno o più database.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-103">Gets one or more databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e3d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e3d8-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e3d8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e3d8-105">DESCRIPTION</span></span>
<span data-ttu-id="4e3d8-106">Il cmdlet **Get-AzureRmSqlDatabase** ottiene uno o più database SQL di Azure da un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-106">The **Get-AzureRmSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>

<span data-ttu-id="4e3d8-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4e3d8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e3d8-108">EXAMPLES</span></span>

### <span data-ttu-id="4e3d8-109">Esempio 1: ottenere tutti i database in un server</span><span class="sxs-lookup"><span data-stu-id="4e3d8-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

<span data-ttu-id="4e3d8-110">Questo comando consente di ottenere tutti i database nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="4e3d8-111">Esempio 2: ottenere un database per nome in un server</span><span class="sxs-lookup"><span data-stu-id="4e3d8-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
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

<span data-ttu-id="4e3d8-112">Questo comando consente di ottenere un database denominato Database02 da un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-112">This command gets a database named Database02 from a server named Server01.</span></span>

## <span data-ttu-id="4e3d8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e3d8-113">PARAMETERS</span></span>

### <span data-ttu-id="4e3d8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e3d8-114">-DatabaseName</span></span>
<span data-ttu-id="4e3d8-115">Specifica il nome del database da recuperare.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-115">Specifies the name of the database to retrieve.</span></span>

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

### <span data-ttu-id="4e3d8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e3d8-116">-ResourceGroupName</span></span>
<span data-ttu-id="4e3d8-117">Specifica il nome del gruppo di risorse a cui è assegnato il server di database.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-117">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="4e3d8-118">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4e3d8-118">-ServerName</span></span>
<span data-ttu-id="4e3d8-119">Specifica il nome del server a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-119">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="4e3d8-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e3d8-120">-Confirm</span></span>
<span data-ttu-id="4e3d8-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e3d8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e3d8-122">-WhatIf</span></span>
<span data-ttu-id="4e3d8-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e3d8-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e3d8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3d8-125">-DefaultProfile</span></span>
<span data-ttu-id="4e3d8-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e3d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3d8-127">CommonParameters</span></span>
<span data-ttu-id="4e3d8-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3d8-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e3d8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3d8-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e3d8-130">INPUTS</span></span>

## <span data-ttu-id="4e3d8-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e3d8-131">OUTPUTS</span></span>

### <span data-ttu-id="4e3d8-132">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4e3d8-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="4e3d8-133">Note</span><span class="sxs-lookup"><span data-stu-id="4e3d8-133">NOTES</span></span>

## <span data-ttu-id="4e3d8-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e3d8-134">RELATED LINKS</span></span>

[<span data-ttu-id="4e3d8-135">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4e3d8-135">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="4e3d8-136">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4e3d8-136">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="4e3d8-137">Curriculum vitae-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4e3d8-137">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="4e3d8-138">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4e3d8-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="4e3d8-139">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4e3d8-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)


