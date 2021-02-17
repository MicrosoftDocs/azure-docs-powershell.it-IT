---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196071"
---
# <span data-ttu-id="ea64d-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ea64d-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="ea64d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea64d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea64d-103">Rimuove un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ea64d-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="ea64d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea64d-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea64d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ea64d-105">DESCRIPTION</span></span>
<span data-ttu-id="ea64d-106">Il cmdlet **Remove-AzSqlDatabase** rimuove un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ea64d-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="ea64d-107">Questo cmdlet è supportato anche dal servizio SQL Server di estensione del database in Azure.</span><span class="sxs-lookup"><span data-stu-id="ea64d-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ea64d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea64d-108">EXAMPLES</span></span>

### <span data-ttu-id="ea64d-109">Esempio 1: Rimuovere un database da un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="ea64d-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ea64d-110">Questo comando rimuove il database denominato Database01 dal server Server01.</span><span class="sxs-lookup"><span data-stu-id="ea64d-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="ea64d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea64d-111">PARAMETERS</span></span>

### <span data-ttu-id="ea64d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea64d-112">-DatabaseName</span></span>
<span data-ttu-id="ea64d-113">Specifica il nome del database rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea64d-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea64d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea64d-114">-DefaultProfile</span></span>
<span data-ttu-id="ea64d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="ea64d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea64d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ea64d-116">-Force</span></span>
<span data-ttu-id="ea64d-117">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="ea64d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea64d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea64d-118">-ResourceGroupName</span></span>
<span data-ttu-id="ea64d-119">Specifica il nome del gruppo di risorse azure a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="ea64d-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ea64d-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ea64d-120">-ServerName</span></span>
<span data-ttu-id="ea64d-121">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="ea64d-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ea64d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea64d-122">-Confirm</span></span>
<span data-ttu-id="ea64d-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea64d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea64d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea64d-124">-WhatIf</span></span>
<span data-ttu-id="ea64d-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea64d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea64d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea64d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea64d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea64d-127">CommonParameters</span></span>
<span data-ttu-id="ea64d-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea64d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea64d-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea64d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea64d-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="ea64d-130">INPUTS</span></span>

### <span data-ttu-id="ea64d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ea64d-131">System.String</span></span>

## <span data-ttu-id="ea64d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea64d-132">OUTPUTS</span></span>

### <span data-ttu-id="ea64d-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ea64d-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ea64d-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="ea64d-134">NOTES</span></span>

## <span data-ttu-id="ea64d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea64d-135">RELATED LINKS</span></span>

[<span data-ttu-id="ea64d-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ea64d-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="ea64d-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ea64d-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="ea64d-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ea64d-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="ea64d-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ea64d-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="ea64d-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ea64d-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="ea64d-141">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="ea64d-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


