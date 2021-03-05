---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: adc3bc9c8d367da6f031f8847cee7ce48b3f9b43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961389"
---
# <span data-ttu-id="6cd71-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6cd71-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="6cd71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cd71-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd71-103">Rimuove un gruppo di failover SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd71-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="6cd71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cd71-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6cd71-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6cd71-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd71-106">Questo comando rimuove il gruppo di failover con il nome specificato, lasciando inalterati tutti i database e le relazioni di replica.</span><span class="sxs-lookup"><span data-stu-id="6cd71-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="6cd71-107">L'endpoint del listener verrà ne verrà annullata la registrazione dal DNS.</span><span class="sxs-lookup"><span data-stu-id="6cd71-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="6cd71-108">Il server primario del gruppo di failover deve essere usato per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="6cd71-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="6cd71-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cd71-109">EXAMPLES</span></span>

### <span data-ttu-id="6cd71-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6cd71-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="6cd71-111">Rimuovere un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="6cd71-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="6cd71-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cd71-112">PARAMETERS</span></span>

### <span data-ttu-id="6cd71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd71-113">-DefaultProfile</span></span>
<span data-ttu-id="6cd71-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6cd71-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cd71-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd71-115">-FailoverGroupName</span></span>
<span data-ttu-id="6cd71-116">Nome del gruppo di failover del SQL database di Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6cd71-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="6cd71-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6cd71-117">-Force</span></span>
<span data-ttu-id="6cd71-118">Ignorare il messaggio di conferma per l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="6cd71-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd71-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd71-119">-ResourceGroupName</span></span>
<span data-ttu-id="6cd71-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6cd71-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="6cd71-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6cd71-121">-ServerName</span></span>
<span data-ttu-id="6cd71-122">Nome del server di database SQL Azure primario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="6cd71-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="6cd71-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cd71-123">-Confirm</span></span>
<span data-ttu-id="6cd71-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cd71-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cd71-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cd71-125">-WhatIf</span></span>
<span data-ttu-id="6cd71-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cd71-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cd71-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cd71-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cd71-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd71-128">CommonParameters</span></span>
<span data-ttu-id="6cd71-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd71-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd71-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6cd71-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd71-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="6cd71-131">INPUTS</span></span>

### <span data-ttu-id="6cd71-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6cd71-132">System.String</span></span>

## <span data-ttu-id="6cd71-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cd71-133">OUTPUTS</span></span>

### <span data-ttu-id="6cd71-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="6cd71-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="6cd71-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="6cd71-135">NOTES</span></span>

## <span data-ttu-id="6cd71-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cd71-136">RELATED LINKS</span></span>

[<span data-ttu-id="6cd71-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6cd71-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6cd71-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6cd71-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6cd71-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6cd71-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6cd71-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6cd71-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="6cd71-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6cd71-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="6cd71-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6cd71-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6cd71-143">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="6cd71-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
