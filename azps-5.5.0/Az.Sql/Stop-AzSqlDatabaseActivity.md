---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f6beaa0651e406d94e1718bb1b1fdea6ef1c3507
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178302"
---
# <span data-ttu-id="bfb9e-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="bfb9e-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="bfb9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfb9e-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb9e-103">Annulla l'operazione di aggiornamento asincrono sul database.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="bfb9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfb9e-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfb9e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bfb9e-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb9e-106">Il **cmdlet Stop-AzSqlDatabaseActivity** annulla l'operazione di aggiornamento asincrono nel database.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="bfb9e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfb9e-107">EXAMPLES</span></span>

### <span data-ttu-id="bfb9e-108">Esempio 1: Annullare l'operazione di aggiornamento asincrono sul database</span><span class="sxs-lookup"><span data-stu-id="bfb9e-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="bfb9e-109">Questo comando annulla l'operazione di aggiornamento asincrono nel database.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="bfb9e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfb9e-110">PARAMETERS</span></span>

### <span data-ttu-id="bfb9e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bfb9e-111">-DatabaseName</span></span>
<span data-ttu-id="bfb9e-112">Specifica il nome del database per cui il cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="bfb9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb9e-113">-DefaultProfile</span></span>
<span data-ttu-id="bfb9e-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfb9e-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bfb9e-115">-ElasticPoolName</span></span>
<span data-ttu-id="bfb9e-116">Nome del pool di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb9e-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bfb9e-117">-OperationId</span></span>
<span data-ttu-id="bfb9e-118">Specifica l'ID dell'operazione che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb9e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb9e-119">-ResourceGroupName</span></span>
<span data-ttu-id="bfb9e-120">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="bfb9e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bfb9e-121">-ServerName</span></span>
<span data-ttu-id="bfb9e-122">Specifica il nome della cartella di Microsoft SQL Server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="bfb9e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfb9e-123">-Confirm</span></span>
<span data-ttu-id="bfb9e-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfb9e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb9e-125">-WhatIf</span></span>
<span data-ttu-id="bfb9e-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfb9e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfb9e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb9e-128">CommonParameters</span></span>
<span data-ttu-id="bfb9e-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb9e-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bfb9e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb9e-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="bfb9e-131">INPUTS</span></span>

### <span data-ttu-id="bfb9e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="bfb9e-132">System.String</span></span>

### <span data-ttu-id="bfb9e-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bfb9e-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bfb9e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfb9e-134">OUTPUTS</span></span>

### <span data-ttu-id="bfb9e-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="bfb9e-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="bfb9e-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="bfb9e-136">NOTES</span></span>

## <span data-ttu-id="bfb9e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfb9e-137">RELATED LINKS</span></span>
