---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaserestorepoints
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
ms.openlocfilehash: c1e4c22392087793e6fbfa0e3959a8b92767ad04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686895"
---
# <span data-ttu-id="66b0f-101">Get-AzureRmSqlDatabaseRestorePoints</span><span class="sxs-lookup"><span data-stu-id="66b0f-101">Get-AzureRmSqlDatabaseRestorePoints</span></span>

## <span data-ttu-id="66b0f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="66b0f-103">Recupera i punti di ripristino distinti da cui può essere ripristinato un data warehouse SQL.</span><span class="sxs-lookup"><span data-stu-id="66b0f-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66b0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66b0f-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRestorePoints [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66b0f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66b0f-105">DESCRIPTION</span></span>
<span data-ttu-id="66b0f-106">Il cmdlet **Get-AzureRmSqlDatabaseRestorePoints** recupera i punti di ripristino distinti a cui è possibile ripristinare un data warehouse SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="66b0f-106">The **Get-AzureRmSqlDatabaseRestorePoints** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="66b0f-107">Per un database SQL di Azure, la finestra di ripristino è continua.</span><span class="sxs-lookup"><span data-stu-id="66b0f-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="66b0f-108">Ciò significa che qualsiasi momento nel periodo di conservazione del backup del database può essere usato come punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="66b0f-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="66b0f-109">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="66b0f-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="66b0f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66b0f-110">EXAMPLES</span></span>

### <span data-ttu-id="66b0f-111">Esempio 1: ottenere tutti i punti di ripristino</span><span class="sxs-lookup"><span data-stu-id="66b0f-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRestorePoints -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="66b0f-112">Questo comando restituisce tutti i punti di ripristino disponibili per il database SQL di Azure denominato Database01.</span><span class="sxs-lookup"><span data-stu-id="66b0f-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="66b0f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66b0f-113">PARAMETERS</span></span>

### <span data-ttu-id="66b0f-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66b0f-114">-DatabaseName</span></span>
<span data-ttu-id="66b0f-115">Specifica il nome del database SQL.</span><span class="sxs-lookup"><span data-stu-id="66b0f-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="66b0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b0f-116">-DefaultProfile</span></span>
<span data-ttu-id="66b0f-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="66b0f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66b0f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b0f-118">-ResourceGroupName</span></span>
<span data-ttu-id="66b0f-119">Specifica il nome del gruppo di risorse a cui è assegnato il database SQL.</span><span class="sxs-lookup"><span data-stu-id="66b0f-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="66b0f-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="66b0f-120">-ServerName</span></span>
<span data-ttu-id="66b0f-121">Specifica il nome del server AzureSQL che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="66b0f-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="66b0f-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="66b0f-122">-Confirm</span></span>
<span data-ttu-id="66b0f-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66b0f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b0f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66b0f-124">-WhatIf</span></span>
<span data-ttu-id="66b0f-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66b0f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66b0f-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66b0f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66b0f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b0f-127">CommonParameters</span></span>
<span data-ttu-id="66b0f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b0f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b0f-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b0f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b0f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66b0f-130">INPUTS</span></span>

### <span data-ttu-id="66b0f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="66b0f-131">System.String</span></span>

## <span data-ttu-id="66b0f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66b0f-132">OUTPUTS</span></span>

### <span data-ttu-id="66b0f-133">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="66b0f-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="66b0f-134">Note</span><span class="sxs-lookup"><span data-stu-id="66b0f-134">NOTES</span></span>

## <span data-ttu-id="66b0f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66b0f-135">RELATED LINKS</span></span>
