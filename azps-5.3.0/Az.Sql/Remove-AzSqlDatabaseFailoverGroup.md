---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474874"
---
# <span data-ttu-id="dc22c-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc22c-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="dc22c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc22c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc22c-103">Rimuove un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="dc22c-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="dc22c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc22c-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc22c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc22c-105">DESCRIPTION</span></span>
<span data-ttu-id="dc22c-106">Questo comando rimuove il gruppo di failover con il nome specificato, lasciando intatti tutti i database e le relazioni di replica.</span><span class="sxs-lookup"><span data-stu-id="dc22c-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="dc22c-107">L'endpoint del listener verrà annullata la registrazione dal DNS.</span><span class="sxs-lookup"><span data-stu-id="dc22c-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="dc22c-108">Il server principale del gruppo di failover deve essere usato per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="dc22c-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="dc22c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc22c-109">EXAMPLES</span></span>

### <span data-ttu-id="dc22c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dc22c-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="dc22c-111">Rimuovere un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="dc22c-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="dc22c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc22c-112">PARAMETERS</span></span>

### <span data-ttu-id="dc22c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc22c-113">-DefaultProfile</span></span>
<span data-ttu-id="dc22c-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dc22c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc22c-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="dc22c-115">-FailoverGroupName</span></span>
<span data-ttu-id="dc22c-116">Il nome del gruppo di failover di database SQL di Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dc22c-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="dc22c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dc22c-117">-Force</span></span>
<span data-ttu-id="dc22c-118">Ignorare il messaggio di conferma per l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="dc22c-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="dc22c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc22c-119">-ResourceGroupName</span></span>
<span data-ttu-id="dc22c-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc22c-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="dc22c-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="dc22c-121">-ServerName</span></span>
<span data-ttu-id="dc22c-122">Nome del server di database SQL di Azure principale del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="dc22c-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="dc22c-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dc22c-123">-Confirm</span></span>
<span data-ttu-id="dc22c-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc22c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc22c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc22c-125">-WhatIf</span></span>
<span data-ttu-id="dc22c-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc22c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc22c-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc22c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc22c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc22c-128">CommonParameters</span></span>
<span data-ttu-id="dc22c-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc22c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc22c-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc22c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc22c-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc22c-131">INPUTS</span></span>

### <span data-ttu-id="dc22c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dc22c-132">System.String</span></span>

## <span data-ttu-id="dc22c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc22c-133">OUTPUTS</span></span>

### <span data-ttu-id="dc22c-134">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="dc22c-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="dc22c-135">Note</span><span class="sxs-lookup"><span data-stu-id="dc22c-135">NOTES</span></span>

## <span data-ttu-id="dc22c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc22c-136">RELATED LINKS</span></span>

[<span data-ttu-id="dc22c-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc22c-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dc22c-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc22c-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dc22c-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc22c-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dc22c-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc22c-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="dc22c-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc22c-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="dc22c-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc22c-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dc22c-143">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="dc22c-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
