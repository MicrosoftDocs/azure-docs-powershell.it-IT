---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f4f3b935aa9303ab38888d6f28f0a89bbdeb6c23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676692"
---
# <span data-ttu-id="beaaf-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="beaaf-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="beaaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="beaaf-102">SYNOPSIS</span></span>
<span data-ttu-id="beaaf-103">Annulla l'operazione di aggiornamento asincrono nel database.</span><span class="sxs-lookup"><span data-stu-id="beaaf-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="beaaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="beaaf-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beaaf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="beaaf-105">DESCRIPTION</span></span>
<span data-ttu-id="beaaf-106">Il cmdlet **Stop-AzSqlDatabaseActivity** Annulla l'operazione di aggiornamento asincrono nel database.</span><span class="sxs-lookup"><span data-stu-id="beaaf-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="beaaf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="beaaf-107">EXAMPLES</span></span>

### <span data-ttu-id="beaaf-108">Esempio 1: annullare l'operazione di aggiornamento asincrono nel database</span><span class="sxs-lookup"><span data-stu-id="beaaf-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
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

<span data-ttu-id="beaaf-109">Questo comando Annulla l'operazione di aggiornamento asincrono nel database.</span><span class="sxs-lookup"><span data-stu-id="beaaf-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="beaaf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="beaaf-110">PARAMETERS</span></span>

### <span data-ttu-id="beaaf-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="beaaf-111">-DatabaseName</span></span>
<span data-ttu-id="beaaf-112">Specifica il nome del database per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="beaaf-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="beaaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beaaf-113">-DefaultProfile</span></span>
<span data-ttu-id="beaaf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="beaaf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beaaf-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="beaaf-115">-ElasticPoolName</span></span>
<span data-ttu-id="beaaf-116">Il nome del pool di Azure SQL elastico.</span><span class="sxs-lookup"><span data-stu-id="beaaf-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="beaaf-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="beaaf-117">-OperationId</span></span>
<span data-ttu-id="beaaf-118">Specifica l'ID dell'operazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="beaaf-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="beaaf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beaaf-119">-ResourceGroupName</span></span>
<span data-ttu-id="beaaf-120">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="beaaf-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="beaaf-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="beaaf-121">-ServerName</span></span>
<span data-ttu-id="beaaf-122">Specifica il nome di Microsoft SQL Server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="beaaf-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="beaaf-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="beaaf-123">-Confirm</span></span>
<span data-ttu-id="beaaf-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="beaaf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beaaf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beaaf-125">-WhatIf</span></span>
<span data-ttu-id="beaaf-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="beaaf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beaaf-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="beaaf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beaaf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beaaf-128">CommonParameters</span></span>
<span data-ttu-id="beaaf-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beaaf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beaaf-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="beaaf-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beaaf-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="beaaf-131">INPUTS</span></span>

### <span data-ttu-id="beaaf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="beaaf-132">System.String</span></span>

### <span data-ttu-id="beaaf-133">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="beaaf-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="beaaf-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="beaaf-134">OUTPUTS</span></span>

### <span data-ttu-id="beaaf-135">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="beaaf-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="beaaf-136">Note</span><span class="sxs-lookup"><span data-stu-id="beaaf-136">NOTES</span></span>

## <span data-ttu-id="beaaf-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="beaaf-137">RELATED LINKS</span></span>
