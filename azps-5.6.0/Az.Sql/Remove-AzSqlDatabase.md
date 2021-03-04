---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: 2a4142c7d8bb0f48bf75613b214dccd1876c5264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957950"
---
# <span data-ttu-id="410d2-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="410d2-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="410d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="410d2-102">SYNOPSIS</span></span>
<span data-ttu-id="410d2-103">Rimuove un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="410d2-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="410d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="410d2-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="410d2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="410d2-105">DESCRIPTION</span></span>
<span data-ttu-id="410d2-106">Il cmdlet **Remove-AzSqlDatabase** rimuove un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="410d2-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="410d2-107">Questo cmdlet è supportato anche dal servizio SQL Server stretch database in Azure.</span><span class="sxs-lookup"><span data-stu-id="410d2-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="410d2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="410d2-108">EXAMPLES</span></span>

### <span data-ttu-id="410d2-109">Esempio 1: Rimuovere un database da un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="410d2-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="410d2-110">Questo comando rimuove il database denominato Database01 dal server Server01.</span><span class="sxs-lookup"><span data-stu-id="410d2-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="410d2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="410d2-111">PARAMETERS</span></span>

### <span data-ttu-id="410d2-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="410d2-112">-DatabaseName</span></span>
<span data-ttu-id="410d2-113">Specifica il nome del database rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="410d2-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="410d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="410d2-114">-DefaultProfile</span></span>
<span data-ttu-id="410d2-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="410d2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="410d2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="410d2-116">-Force</span></span>
<span data-ttu-id="410d2-117">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="410d2-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="410d2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="410d2-118">-ResourceGroupName</span></span>
<span data-ttu-id="410d2-119">Specifica il nome del gruppo di risorse azure a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="410d2-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="410d2-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="410d2-120">-ServerName</span></span>
<span data-ttu-id="410d2-121">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="410d2-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="410d2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="410d2-122">-Confirm</span></span>
<span data-ttu-id="410d2-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="410d2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="410d2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="410d2-124">-WhatIf</span></span>
<span data-ttu-id="410d2-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="410d2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="410d2-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="410d2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="410d2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410d2-127">CommonParameters</span></span>
<span data-ttu-id="410d2-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="410d2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410d2-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="410d2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410d2-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="410d2-130">INPUTS</span></span>

### <span data-ttu-id="410d2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="410d2-131">System.String</span></span>

## <span data-ttu-id="410d2-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="410d2-132">OUTPUTS</span></span>

### <span data-ttu-id="410d2-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="410d2-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="410d2-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="410d2-134">NOTES</span></span>

## <span data-ttu-id="410d2-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="410d2-135">RELATED LINKS</span></span>

[<span data-ttu-id="410d2-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="410d2-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="410d2-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="410d2-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="410d2-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="410d2-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="410d2-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="410d2-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="410d2-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="410d2-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="410d2-141">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="410d2-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


