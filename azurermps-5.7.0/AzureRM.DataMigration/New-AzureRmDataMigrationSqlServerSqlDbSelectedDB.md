---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationsqlserversqldbselecteddb
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
ms.openlocfilehash: 1be43b5d08011a71ec093df2f93c63dd04c6004d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514371"
---
# <span data-ttu-id="401ea-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span><span class="sxs-lookup"><span data-stu-id="401ea-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span></span>

## <span data-ttu-id="401ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="401ea-102">SYNOPSIS</span></span>
<span data-ttu-id="401ea-103">Crea un oggetto MigrateSqlServerSqlDbDatabaseInput che contiene informazioni sui database di origine e di destinazione per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="401ea-103">Creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="401ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="401ea-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSqlServerSqlDbSelectedDB [-Id <String>] [-Name <String>] [-TargetDatabaseName <String>]
 [-MakeSourceDbReadOnly] [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="401ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="401ea-105">DESCRIPTION</span></span>
<span data-ttu-id="401ea-106">Il cmdlet New-AzureRmDataMigrationSqlServerSqlDbSelectedDB crea un oggetto MigrateSqlServerSqlDbDatabaseInput che contiene informazioni sui database di origine e di destinazione, oltre ai mapping delle tabelle, per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="401ea-106">The New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="401ea-107">Questo cmdlet può essere usato come parametro con il cmdlet New-AzureRmDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="401ea-107">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="401ea-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="401ea-108">EXAMPLES</span></span>

### <span data-ttu-id="401ea-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="401ea-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSqlServerSqlDbSelectedDB  -Name AdventuerWorks2016 -TargetDatabaseName AdventureWorks2016
 -MakeSourceDbReadOnly -TableMap $tableMap
```

<span data-ttu-id="401ea-110">L'esempio precedente crea l'oggetto MigrateSqlServerSqlDbDatabaseInput per la migrazione del database **AdventureWorks2016** a un database di SQL Azure con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="401ea-110">The above example creates MigrateSqlServerSqlDbDatabaseInput object for migrating the **AdventureWorks2016** database to a SQL Azure database with the same name.</span></span>

## <span data-ttu-id="401ea-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="401ea-111">PARAMETERS</span></span>

### <span data-ttu-id="401ea-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="401ea-112">-Confirm</span></span>
<span data-ttu-id="401ea-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="401ea-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="401ea-114">-DefaultProfile</span></span>
<span data-ttu-id="401ea-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="401ea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="401ea-116">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="401ea-116">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="401ea-117">Impostare il database in ReadOnly prima della migrazione</span><span class="sxs-lookup"><span data-stu-id="401ea-117">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="401ea-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="401ea-118">-Name</span></span>
<span data-ttu-id="401ea-119">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="401ea-119">The name of the database.</span></span>

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

### <span data-ttu-id="401ea-120">-TableMap</span><span class="sxs-lookup"><span data-stu-id="401ea-120">-TableMap</span></span>
<span data-ttu-id="401ea-121">mapping dell'origine alle tabelle di destinazione</span><span class="sxs-lookup"><span data-stu-id="401ea-121">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401ea-122">-NomeDatabaseDestinazione</span><span class="sxs-lookup"><span data-stu-id="401ea-122">-TargetDatabaseName</span></span>
<span data-ttu-id="401ea-123">Nome del database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="401ea-123">The name of the target Database.</span></span>

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

## <span data-ttu-id="401ea-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="401ea-124">INPUTS</span></span>

### <span data-ttu-id="401ea-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="401ea-125">None</span></span>


## <span data-ttu-id="401ea-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="401ea-126">OUTPUTS</span></span>

### <span data-ttu-id="401ea-127">Microsoft. Azure. Management. DataMigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="401ea-127">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>


## <span data-ttu-id="401ea-128">Note</span><span class="sxs-lookup"><span data-stu-id="401ea-128">NOTES</span></span>

## <span data-ttu-id="401ea-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="401ea-129">RELATED LINKS</span></span>


