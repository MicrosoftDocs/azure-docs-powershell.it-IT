---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: d0aa42b8b584ade698c3d03848a537350ac342d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686670"
---
# <span data-ttu-id="bd0ae-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="bd0ae-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="bd0ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0ae-103">Annulla l'operazione di aggiornamento asincrono nel database.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd0ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd0ae-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd0ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd0ae-105">DESCRIPTION</span></span>
<span data-ttu-id="bd0ae-106">Il cmdlet **Stop-AzureRmSqlDatabaseActivity** Annulla l'operazione di aggiornamento asincrono nel database.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="bd0ae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd0ae-107">EXAMPLES</span></span>

### <span data-ttu-id="bd0ae-108">Esempio 1: annullare l'operazione di aggiornamento asincrono nel database</span><span class="sxs-lookup"><span data-stu-id="bd0ae-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
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

<span data-ttu-id="bd0ae-109">Questo comando Annulla l'operazione di aggiornamento asincrono nel database.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="bd0ae-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd0ae-110">PARAMETERS</span></span>

### <span data-ttu-id="bd0ae-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd0ae-111">-DatabaseName</span></span>
<span data-ttu-id="bd0ae-112">Specifica il nome del database per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0ae-113">-DefaultProfile</span></span>
<span data-ttu-id="bd0ae-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd0ae-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bd0ae-115">-ElasticPoolName</span></span>
<span data-ttu-id="bd0ae-116">Il nome del pool di Azure SQL elastico.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0ae-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bd0ae-117">-OperationId</span></span>
<span data-ttu-id="bd0ae-118">Specifica l'ID dell'operazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd0ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="bd0ae-120">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-120">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0ae-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="bd0ae-121">-ServerName</span></span>
<span data-ttu-id="bd0ae-122">Specifica il nome di Microsoft SQL Server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd0ae-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bd0ae-123">-Confirm</span></span>
<span data-ttu-id="bd0ae-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd0ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd0ae-125">-WhatIf</span></span>
<span data-ttu-id="bd0ae-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd0ae-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd0ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0ae-128">CommonParameters</span></span>
<span data-ttu-id="bd0ae-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd0ae-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd0ae-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0ae-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd0ae-131">INPUTS</span></span>

### <span data-ttu-id="bd0ae-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd0ae-132">None</span></span>
<span data-ttu-id="bd0ae-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bd0ae-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd0ae-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd0ae-134">OUTPUTS</span></span>

### <span data-ttu-id="bd0ae-135">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="bd0ae-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="bd0ae-136">Note</span><span class="sxs-lookup"><span data-stu-id="bd0ae-136">NOTES</span></span>

## <span data-ttu-id="bd0ae-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd0ae-137">RELATED LINKS</span></span>
