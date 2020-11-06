---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: af2f10b371eb21558a4b675331ec97f797611d26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513327"
---
# <span data-ttu-id="52fab-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="52fab-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="52fab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52fab-102">SYNOPSIS</span></span>
<span data-ttu-id="52fab-103">Annulla l'operazione di aggiornamento asincrono nel database.</span><span class="sxs-lookup"><span data-stu-id="52fab-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52fab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52fab-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52fab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52fab-105">DESCRIPTION</span></span>
<span data-ttu-id="52fab-106">Il cmdlet **Stop-AzureRmSqlDatabaseActivity** Annulla l'operazione di aggiornamento asincrono nel database.</span><span class="sxs-lookup"><span data-stu-id="52fab-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="52fab-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52fab-107">EXAMPLES</span></span>

### <span data-ttu-id="52fab-108">Esempio 1: annullare l'operazione di aggiornamento asincrono nel database</span><span class="sxs-lookup"><span data-stu-id="52fab-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="52fab-109">Questo comando Annulla l'operazione di aggiornamento asincrono nel database.</span><span class="sxs-lookup"><span data-stu-id="52fab-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="52fab-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52fab-110">PARAMETERS</span></span>

### <span data-ttu-id="52fab-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52fab-111">-DatabaseName</span></span>
<span data-ttu-id="52fab-112">Specifica il nome del database per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="52fab-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="52fab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52fab-113">-DefaultProfile</span></span>
<span data-ttu-id="52fab-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52fab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52fab-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="52fab-115">-ElasticPoolName</span></span>
<span data-ttu-id="52fab-116">Il nome del pool di Azure SQL elastico.</span><span class="sxs-lookup"><span data-stu-id="52fab-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="52fab-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="52fab-117">-OperationId</span></span>
<span data-ttu-id="52fab-118">Specifica l'ID dell'operazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52fab-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="52fab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52fab-119">-ResourceGroupName</span></span>
<span data-ttu-id="52fab-120">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="52fab-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="52fab-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="52fab-121">-ServerName</span></span>
<span data-ttu-id="52fab-122">Specifica il nome di Microsoft SQL Server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="52fab-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="52fab-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52fab-123">-Confirm</span></span>
<span data-ttu-id="52fab-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52fab-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52fab-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52fab-125">-WhatIf</span></span>
<span data-ttu-id="52fab-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52fab-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52fab-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52fab-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52fab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fab-128">CommonParameters</span></span>
<span data-ttu-id="52fab-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52fab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fab-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52fab-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fab-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52fab-131">INPUTS</span></span>

### <span data-ttu-id="52fab-132">System. String</span><span class="sxs-lookup"><span data-stu-id="52fab-132">System.String</span></span>

### <span data-ttu-id="52fab-133">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="52fab-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="52fab-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52fab-134">OUTPUTS</span></span>

### <span data-ttu-id="52fab-135">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="52fab-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="52fab-136">Note</span><span class="sxs-lookup"><span data-stu-id="52fab-136">NOTES</span></span>

## <span data-ttu-id="52fab-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52fab-137">RELATED LINKS</span></span>
