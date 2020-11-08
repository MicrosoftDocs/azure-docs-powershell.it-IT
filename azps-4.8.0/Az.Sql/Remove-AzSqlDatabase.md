---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189299"
---
# <span data-ttu-id="8e623-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e623-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="8e623-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e623-102">SYNOPSIS</span></span>
<span data-ttu-id="8e623-103">Rimuove un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8e623-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="8e623-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e623-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e623-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e623-105">DESCRIPTION</span></span>
<span data-ttu-id="8e623-106">Il cmdlet **Remove-AzSqlDatabase** rimuove un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8e623-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="8e623-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="8e623-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8e623-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e623-108">EXAMPLES</span></span>

### <span data-ttu-id="8e623-109">Esempio 1: rimuovere un database da un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="8e623-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="8e623-110">Questo comando rimuove il database denominato Database01 da server Server01.</span><span class="sxs-lookup"><span data-stu-id="8e623-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="8e623-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e623-111">PARAMETERS</span></span>

### <span data-ttu-id="8e623-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8e623-112">-DatabaseName</span></span>
<span data-ttu-id="8e623-113">Specifica il nome del database rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e623-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8e623-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e623-114">-DefaultProfile</span></span>
<span data-ttu-id="8e623-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8e623-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e623-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8e623-116">-Force</span></span>
<span data-ttu-id="8e623-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8e623-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e623-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e623-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e623-119">Specifica il nome del gruppo di risorse Azure a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="8e623-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="8e623-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="8e623-120">-ServerName</span></span>
<span data-ttu-id="8e623-121">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="8e623-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="8e623-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8e623-122">-Confirm</span></span>
<span data-ttu-id="8e623-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e623-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e623-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e623-124">-WhatIf</span></span>
<span data-ttu-id="8e623-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e623-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e623-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e623-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e623-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e623-127">CommonParameters</span></span>
<span data-ttu-id="8e623-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e623-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e623-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e623-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e623-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e623-130">INPUTS</span></span>

### <span data-ttu-id="8e623-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8e623-131">System.String</span></span>

## <span data-ttu-id="8e623-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e623-132">OUTPUTS</span></span>

### <span data-ttu-id="8e623-133">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8e623-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8e623-134">Note</span><span class="sxs-lookup"><span data-stu-id="8e623-134">NOTES</span></span>

## <span data-ttu-id="8e623-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e623-135">RELATED LINKS</span></span>

[<span data-ttu-id="8e623-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e623-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="8e623-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e623-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="8e623-138">Curriculum vitae-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e623-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="8e623-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e623-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="8e623-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e623-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="8e623-141">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="8e623-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


