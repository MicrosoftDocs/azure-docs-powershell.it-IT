---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 8fb320c2caa4993b7880ef719a3d9ea0e0e8c811
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956589"
---
# <span data-ttu-id="4e58d-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="4e58d-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="4e58d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e58d-102">SYNOPSIS</span></span>
<span data-ttu-id="4e58d-103">Crea un nuovo punto di ripristino da cui è possibile SQL un database.</span><span class="sxs-lookup"><span data-stu-id="4e58d-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="4e58d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e58d-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e58d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4e58d-105">DESCRIPTION</span></span>
<span data-ttu-id="4e58d-106">Il cmdlet **New-AzSqlDatabaseRestorePoint** crea un nuovo punto di ripristino da cui è possibile ripristinare un data warehouse di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4e58d-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="4e58d-107">Questo cmdlet è attualmente supportato per Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="4e58d-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="4e58d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e58d-108">EXAMPLES</span></span>

### <span data-ttu-id="4e58d-109">Esempio 1: Creare un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="4e58d-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="4e58d-110">Questo comando crea un punto di ripristino per Azure SQL Data Warehouse e restituisce i dettagli del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4e58d-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="4e58d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e58d-111">PARAMETERS</span></span>

### <span data-ttu-id="4e58d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e58d-112">-DatabaseName</span></span>
<span data-ttu-id="4e58d-113">Specifica il nome dell'SQL database.</span><span class="sxs-lookup"><span data-stu-id="4e58d-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="4e58d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e58d-114">-DefaultProfile</span></span>
<span data-ttu-id="4e58d-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4e58d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e58d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e58d-116">-ResourceGroupName</span></span>
<span data-ttu-id="4e58d-117">Specifica il nome del gruppo di risorse a cui è assegnato SQL database.</span><span class="sxs-lookup"><span data-stu-id="4e58d-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="4e58d-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="4e58d-118">-RestorePointLabel</span></span>
<span data-ttu-id="4e58d-119">Specifica l'etichetta del punto di ripristino per facilitane l'identificazione.</span><span class="sxs-lookup"><span data-stu-id="4e58d-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e58d-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e58d-120">-ServerName</span></span>
<span data-ttu-id="4e58d-121">Specifica il nome del server AzureSQL che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="4e58d-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="4e58d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e58d-122">-Confirm</span></span>
<span data-ttu-id="4e58d-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e58d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e58d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e58d-124">-WhatIf</span></span>
<span data-ttu-id="4e58d-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e58d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e58d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e58d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e58d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e58d-127">CommonParameters</span></span>
<span data-ttu-id="4e58d-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e58d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e58d-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4e58d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e58d-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="4e58d-130">INPUTS</span></span>

### <span data-ttu-id="4e58d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4e58d-131">System.String</span></span>

## <span data-ttu-id="4e58d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e58d-132">OUTPUTS</span></span>

### <span data-ttu-id="4e58d-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="4e58d-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="4e58d-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="4e58d-134">NOTES</span></span>

## <span data-ttu-id="4e58d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e58d-135">RELATED LINKS</span></span>
