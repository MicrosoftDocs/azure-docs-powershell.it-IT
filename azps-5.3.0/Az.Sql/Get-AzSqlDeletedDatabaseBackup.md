---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473686"
---
# <span data-ttu-id="7f4f4-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="7f4f4-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="7f4f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f4f4-103">Ottiene un database eliminato che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="7f4f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f4f4-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f4f4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f4f4-105">DESCRIPTION</span></span>
<span data-ttu-id="7f4f4-106">Il cmdlet **Get-AzSqlDeletedDatabaseBackup** ottiene un backup di database SQL eliminato specificato che è possibile ripristinare o tutti i backup eliminati che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="7f4f4-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7f4f4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f4f4-108">EXAMPLES</span></span>

### <span data-ttu-id="7f4f4-109">Esempio 1: ottenere tutti i backup di database eliminati in un server</span><span class="sxs-lookup"><span data-stu-id="7f4f4-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="7f4f4-110">Questo comando ottiene tutti i backup del database eliminati in un server.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="7f4f4-111">Esempio 2: ottenere un backup del database eliminato specificato</span><span class="sxs-lookup"><span data-stu-id="7f4f4-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="7f4f4-112">Questo comando ottiene il backup del database eliminato per ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="7f4f4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f4f4-113">PARAMETERS</span></span>

### <span data-ttu-id="7f4f4-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7f4f4-114">-DatabaseName</span></span>
<span data-ttu-id="7f4f4-115">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4f4-116">-DefaultProfile</span></span>
<span data-ttu-id="7f4f4-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7f4f4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f4f4-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="7f4f4-118">-DeletionDate</span></span>
<span data-ttu-id="7f4f4-119">Specifica la data, come oggetto **DateTime** , che il database è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="7f4f4-120">Per ottenere un oggetto **DateTime** , usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f4f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="7f4f4-122">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7f4f4-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="7f4f4-123">-ServerName</span></span>
<span data-ttu-id="7f4f4-124">Specifica il nome del server di database.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="7f4f4-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f4f4-125">-Confirm</span></span>
<span data-ttu-id="7f4f4-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f4f4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f4f4-127">-WhatIf</span></span>
<span data-ttu-id="7f4f4-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f4f4-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f4f4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4f4-130">CommonParameters</span></span>
<span data-ttu-id="7f4f4-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4f4-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f4f4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4f4-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f4f4-133">INPUTS</span></span>

### <span data-ttu-id="7f4f4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7f4f4-134">System.String</span></span>

### <span data-ttu-id="7f4f4-135">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7f4f4-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7f4f4-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f4f4-136">OUTPUTS</span></span>

### <span data-ttu-id="7f4f4-137">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="7f4f4-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="7f4f4-138">Note</span><span class="sxs-lookup"><span data-stu-id="7f4f4-138">NOTES</span></span>

## <span data-ttu-id="7f4f4-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f4f4-139">RELATED LINKS</span></span>

[<span data-ttu-id="7f4f4-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7f4f4-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="7f4f4-141">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="7f4f4-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
