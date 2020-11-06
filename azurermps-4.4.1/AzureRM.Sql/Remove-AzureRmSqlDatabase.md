---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 1660c92ef4bef4cd832bc60506f7ef24d8927313
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521959"
---
# <span data-ttu-id="ccae9-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccae9-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="ccae9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ccae9-102">SYNOPSIS</span></span>
<span data-ttu-id="ccae9-103">Rimuove un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ccae9-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccae9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ccae9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccae9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccae9-105">DESCRIPTION</span></span>
<span data-ttu-id="ccae9-106">Il cmdlet **Remove-AzureRmSqlDatabase** rimuove un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ccae9-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="ccae9-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="ccae9-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ccae9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ccae9-108">EXAMPLES</span></span>

### <span data-ttu-id="ccae9-109">Esempio 1: rimuovere un database da un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="ccae9-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ccae9-110">Questo comando rimuove il database denominato Database01 da server Server01.</span><span class="sxs-lookup"><span data-stu-id="ccae9-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="ccae9-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ccae9-111">PARAMETERS</span></span>

### <span data-ttu-id="ccae9-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ccae9-112">-DatabaseName</span></span>
<span data-ttu-id="ccae9-113">Specifica il nome del database rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccae9-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccae9-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ccae9-114">-Force</span></span>
<span data-ttu-id="ccae9-115">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ccae9-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ccae9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccae9-116">-ResourceGroupName</span></span>
<span data-ttu-id="ccae9-117">Specifica il nome del gruppo di risorse Azure a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="ccae9-117">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ccae9-118">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ccae9-118">-ServerName</span></span>
<span data-ttu-id="ccae9-119">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="ccae9-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ccae9-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ccae9-120">-Confirm</span></span>
<span data-ttu-id="ccae9-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccae9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccae9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccae9-122">-WhatIf</span></span>
<span data-ttu-id="ccae9-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccae9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccae9-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccae9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccae9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccae9-125">-DefaultProfile</span></span>
<span data-ttu-id="ccae9-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ccae9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccae9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccae9-127">CommonParameters</span></span>
<span data-ttu-id="ccae9-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccae9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccae9-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccae9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccae9-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ccae9-130">INPUTS</span></span>

### <span data-ttu-id="ccae9-131">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ccae9-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ccae9-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ccae9-132">OUTPUTS</span></span>

### <span data-ttu-id="ccae9-133">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ccae9-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ccae9-134">Note</span><span class="sxs-lookup"><span data-stu-id="ccae9-134">NOTES</span></span>

## <span data-ttu-id="ccae9-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ccae9-135">RELATED LINKS</span></span>

[<span data-ttu-id="ccae9-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccae9-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="ccae9-137">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccae9-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="ccae9-138">Curriculum vitae-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccae9-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="ccae9-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccae9-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="ccae9-140">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccae9-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="ccae9-141">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="ccae9-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


