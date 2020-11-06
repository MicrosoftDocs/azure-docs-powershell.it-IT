---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2373a076e6edd97314e08c9170f9584a904ad902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513387"
---
# <span data-ttu-id="5c5d5-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="5c5d5-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="5c5d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c5d5-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5d5-103">Ottiene un database eliminato che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c5d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c5d5-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c5d5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c5d5-105">DESCRIPTION</span></span>
<span data-ttu-id="5c5d5-106">Il cmdlet **Get-AzureRMSqlDeletedDatabaseBackup** ottiene un backup di database SQL eliminato specificato che è possibile ripristinare o tutti i backup eliminati che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="5c5d5-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5c5d5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c5d5-108">EXAMPLES</span></span>

### <span data-ttu-id="5c5d5-109">Esempio 1: ottenere tutti i backup di database eliminati in un server</span><span class="sxs-lookup"><span data-stu-id="5c5d5-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="5c5d5-110">Questo comando ottiene tutti i backup del database eliminati in un server.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="5c5d5-111">Esempio 2: ottenere un backup del database eliminato specificato</span><span class="sxs-lookup"><span data-stu-id="5c5d5-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="5c5d5-112">Questo comando ottiene il backup del database eliminato per ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="5c5d5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c5d5-113">PARAMETERS</span></span>

### <span data-ttu-id="5c5d5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c5d5-114">-DatabaseName</span></span>
<span data-ttu-id="5c5d5-115">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="5c5d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c5d5-116">-DefaultProfile</span></span>
<span data-ttu-id="5c5d5-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5c5d5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c5d5-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="5c5d5-118">-DeletionDate</span></span>
<span data-ttu-id="5c5d5-119">Specifica la data, come oggetto **DateTime** , che il database è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="5c5d5-120">Per ottenere un oggetto **DateTime** , usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="5c5d5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c5d5-121">-ResourceGroupName</span></span>
<span data-ttu-id="5c5d5-122">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5c5d5-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5c5d5-123">-ServerName</span></span>
<span data-ttu-id="5c5d5-124">Specifica il nome del server di database.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="5c5d5-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5c5d5-125">-Confirm</span></span>
<span data-ttu-id="5c5d5-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c5d5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c5d5-127">-WhatIf</span></span>
<span data-ttu-id="5c5d5-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c5d5-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c5d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5d5-130">CommonParameters</span></span>
<span data-ttu-id="5c5d5-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c5d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5d5-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c5d5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5d5-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c5d5-133">INPUTS</span></span>

### <span data-ttu-id="5c5d5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5c5d5-134">System.String</span></span>

### <span data-ttu-id="5c5d5-135">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5c5d5-135">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="5c5d5-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c5d5-136">OUTPUTS</span></span>

### <span data-ttu-id="5c5d5-137">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="5c5d5-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="5c5d5-138">Note</span><span class="sxs-lookup"><span data-stu-id="5c5d5-138">NOTES</span></span>

## <span data-ttu-id="5c5d5-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c5d5-139">RELATED LINKS</span></span>

[<span data-ttu-id="5c5d5-140">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c5d5-140">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="5c5d5-141">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="5c5d5-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
