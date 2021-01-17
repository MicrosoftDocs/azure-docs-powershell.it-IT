---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345727"
---
# <span data-ttu-id="8bb6c-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="8bb6c-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="8bb6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8bb6c-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb6c-103">Ottiene un database eliminato che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="8bb6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bb6c-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bb6c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bb6c-105">DESCRIPTION</span></span>
<span data-ttu-id="8bb6c-106">Il cmdlet **Get-AzSqlDeletedDatabaseBackup** ottiene un backup di database SQL eliminato specificato che è possibile ripristinare o tutti i backup eliminati che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="8bb6c-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8bb6c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bb6c-108">EXAMPLES</span></span>

### <span data-ttu-id="8bb6c-109">Esempio 1: ottenere tutti i backup di database eliminati in un server</span><span class="sxs-lookup"><span data-stu-id="8bb6c-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="8bb6c-110">Questo comando ottiene tutti i backup del database eliminati in un server.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="8bb6c-111">Esempio 2: ottenere un backup del database eliminato specificato</span><span class="sxs-lookup"><span data-stu-id="8bb6c-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="8bb6c-112">Questo comando ottiene il backup del database eliminato per ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="8bb6c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bb6c-113">PARAMETERS</span></span>

### <span data-ttu-id="8bb6c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8bb6c-114">-DatabaseName</span></span>
<span data-ttu-id="8bb6c-115">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="8bb6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb6c-116">-DefaultProfile</span></span>
<span data-ttu-id="8bb6c-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8bb6c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bb6c-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="8bb6c-118">-DeletionDate</span></span>
<span data-ttu-id="8bb6c-119">Specifica la data, come oggetto **DateTime** , che il database è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="8bb6c-120">Per ottenere un oggetto **DateTime** , usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="8bb6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bb6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8bb6c-122">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8bb6c-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="8bb6c-123">-ServerName</span></span>
<span data-ttu-id="8bb6c-124">Specifica il nome del server di database.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="8bb6c-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8bb6c-125">-Confirm</span></span>
<span data-ttu-id="8bb6c-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bb6c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bb6c-127">-WhatIf</span></span>
<span data-ttu-id="8bb6c-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bb6c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bb6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb6c-130">CommonParameters</span></span>
<span data-ttu-id="8bb6c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb6c-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bb6c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb6c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8bb6c-133">INPUTS</span></span>

### <span data-ttu-id="8bb6c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8bb6c-134">System.String</span></span>

### <span data-ttu-id="8bb6c-135">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8bb6c-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8bb6c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bb6c-136">OUTPUTS</span></span>

### <span data-ttu-id="8bb6c-137">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="8bb6c-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="8bb6c-138">Note</span><span class="sxs-lookup"><span data-stu-id="8bb6c-138">NOTES</span></span>

## <span data-ttu-id="8bb6c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bb6c-139">RELATED LINKS</span></span>

[<span data-ttu-id="8bb6c-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8bb6c-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="8bb6c-141">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="8bb6c-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
