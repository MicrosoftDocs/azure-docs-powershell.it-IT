---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 3da5093decdaea29d1a225db5c683d2f23f7115f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517859"
---
# <span data-ttu-id="f893d-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f893d-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="f893d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f893d-102">SYNOPSIS</span></span>
<span data-ttu-id="f893d-103">Rimuove un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f893d-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f893d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f893d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f893d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f893d-105">DESCRIPTION</span></span>
<span data-ttu-id="f893d-106">Il cmdlet **Remove-AzureRmSqlDatabase** rimuove un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f893d-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="f893d-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="f893d-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f893d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f893d-108">EXAMPLES</span></span>

### <span data-ttu-id="f893d-109">Esempio 1: rimuovere un database da un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="f893d-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f893d-110">Questo comando rimuove il database denominato Database01 da server Server01.</span><span class="sxs-lookup"><span data-stu-id="f893d-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="f893d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f893d-111">PARAMETERS</span></span>

### <span data-ttu-id="f893d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f893d-112">-DatabaseName</span></span>
<span data-ttu-id="f893d-113">Specifica il nome del database rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f893d-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f893d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f893d-114">-DefaultProfile</span></span>
<span data-ttu-id="f893d-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f893d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f893d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f893d-116">-Force</span></span>
<span data-ttu-id="f893d-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f893d-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f893d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f893d-118">-ResourceGroupName</span></span>
<span data-ttu-id="f893d-119">Specifica il nome del gruppo di risorse Azure a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="f893d-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f893d-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f893d-120">-ServerName</span></span>
<span data-ttu-id="f893d-121">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="f893d-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="f893d-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f893d-122">-Confirm</span></span>
<span data-ttu-id="f893d-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f893d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f893d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f893d-124">-WhatIf</span></span>
<span data-ttu-id="f893d-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f893d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f893d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f893d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f893d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f893d-127">CommonParameters</span></span>
<span data-ttu-id="f893d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f893d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f893d-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f893d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f893d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f893d-130">INPUTS</span></span>

### <span data-ttu-id="f893d-131">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f893d-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f893d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f893d-132">OUTPUTS</span></span>

### <span data-ttu-id="f893d-133">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f893d-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f893d-134">Note</span><span class="sxs-lookup"><span data-stu-id="f893d-134">NOTES</span></span>

## <span data-ttu-id="f893d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f893d-135">RELATED LINKS</span></span>

[<span data-ttu-id="f893d-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f893d-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="f893d-137">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f893d-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="f893d-138">Curriculum vitae-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f893d-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="f893d-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f893d-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="f893d-140">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f893d-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="f893d-141">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="f893d-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

