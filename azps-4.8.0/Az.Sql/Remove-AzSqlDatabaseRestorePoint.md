---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 2e98f832bd13509a853d85037a413b6fd5895695
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189289"
---
# <span data-ttu-id="89a70-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="89a70-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="89a70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89a70-102">SYNOPSIS</span></span>
<span data-ttu-id="89a70-103">Rimuove il punto di ripristino dato da un database SQL.</span><span class="sxs-lookup"><span data-stu-id="89a70-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="89a70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89a70-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89a70-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89a70-105">DESCRIPTION</span></span>
<span data-ttu-id="89a70-106">Il cmdlet **Remove-AzSqlDatabaseRestorePoint** rimuove il punto di ripristino dato da un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="89a70-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="89a70-107">Questo cmdlet è attualmente supportato dal servizio SQL Server Datawarehouse in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="89a70-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="89a70-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89a70-108">EXAMPLES</span></span>

### <span data-ttu-id="89a70-109">Esempio 1: rimuove un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="89a70-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="89a70-110">Questo comando rimuove un punto di ripristino per il database SQL di Azure Data di creazione.</span><span class="sxs-lookup"><span data-stu-id="89a70-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="89a70-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89a70-111">PARAMETERS</span></span>

### <span data-ttu-id="89a70-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="89a70-112">-DatabaseName</span></span>
<span data-ttu-id="89a70-113">Specifica il nome del database SQL.</span><span class="sxs-lookup"><span data-stu-id="89a70-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89a70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a70-114">-DefaultProfile</span></span>
<span data-ttu-id="89a70-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="89a70-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89a70-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89a70-116">-PassThru</span></span>
<span data-ttu-id="89a70-117">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="89a70-117">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a70-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89a70-118">-ResourceGroupName</span></span>
<span data-ttu-id="89a70-119">Specifica il nome del gruppo di risorse a cui è assegnato il database SQL.</span><span class="sxs-lookup"><span data-stu-id="89a70-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="89a70-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="89a70-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="89a70-121">Specifica la data di creazione del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="89a70-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89a70-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="89a70-122">-ServerName</span></span>
<span data-ttu-id="89a70-123">Specifica il nome del server AzureSQL che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="89a70-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="89a70-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="89a70-124">-Confirm</span></span>
<span data-ttu-id="89a70-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89a70-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89a70-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89a70-126">-WhatIf</span></span>
<span data-ttu-id="89a70-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89a70-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89a70-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89a70-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89a70-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a70-129">CommonParameters</span></span>
<span data-ttu-id="89a70-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89a70-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a70-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89a70-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a70-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89a70-132">INPUTS</span></span>

### <span data-ttu-id="89a70-133">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="89a70-133">System.DateTime</span></span>

### <span data-ttu-id="89a70-134">System. String</span><span class="sxs-lookup"><span data-stu-id="89a70-134">System.String</span></span>

## <span data-ttu-id="89a70-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89a70-135">OUTPUTS</span></span>

### <span data-ttu-id="89a70-136">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="89a70-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="89a70-137">Note</span><span class="sxs-lookup"><span data-stu-id="89a70-137">NOTES</span></span>

## <span data-ttu-id="89a70-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89a70-138">RELATED LINKS</span></span>
