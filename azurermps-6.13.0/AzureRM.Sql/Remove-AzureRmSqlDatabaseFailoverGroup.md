---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 426b44b6c01e40a616d834d2768e5d050a2bc1db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518496"
---
# <span data-ttu-id="a4ca2-101">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4ca2-101">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="a4ca2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ca2-103">Rimuove un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-103">Removes an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4ca2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4ca2-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4ca2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4ca2-105">DESCRIPTION</span></span>
<span data-ttu-id="a4ca2-106">Questo comando rimuove il gruppo di failover con il nome specificato, lasciando intatti tutti i database e le relazioni di replica.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="a4ca2-107">L'endpoint del listener verrà annullata la registrazione dal DNS.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="a4ca2-108">Il server principale del gruppo di failover deve essere usato per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="a4ca2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4ca2-109">EXAMPLES</span></span>

### <span data-ttu-id="a4ca2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4ca2-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="a4ca2-111">Rimuovere un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="a4ca2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4ca2-112">PARAMETERS</span></span>

### <span data-ttu-id="a4ca2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ca2-113">-DefaultProfile</span></span>
<span data-ttu-id="a4ca2-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a4ca2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4ca2-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ca2-115">-FailoverGroupName</span></span>
<span data-ttu-id="a4ca2-116">Il nome del gruppo di failover di database SQL di Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="a4ca2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a4ca2-117">-Force</span></span>
<span data-ttu-id="a4ca2-118">Ignorare il messaggio di conferma per l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="a4ca2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ca2-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4ca2-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4ca2-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a4ca2-121">-ServerName</span></span>
<span data-ttu-id="a4ca2-122">Nome del server di database SQL di Azure principale del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="a4ca2-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4ca2-123">-Confirm</span></span>
<span data-ttu-id="a4ca2-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ca2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4ca2-125">-WhatIf</span></span>
<span data-ttu-id="a4ca2-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ca2-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ca2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ca2-128">CommonParameters</span></span>
<span data-ttu-id="a4ca2-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ca2-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ca2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ca2-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4ca2-131">INPUTS</span></span>

### <span data-ttu-id="a4ca2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ca2-132">System.String</span></span>

## <span data-ttu-id="a4ca2-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4ca2-133">OUTPUTS</span></span>

### <span data-ttu-id="a4ca2-134">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="a4ca2-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="a4ca2-135">Note</span><span class="sxs-lookup"><span data-stu-id="a4ca2-135">NOTES</span></span>

## <span data-ttu-id="a4ca2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4ca2-136">RELATED LINKS</span></span>

[<span data-ttu-id="a4ca2-137">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4ca2-137">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4ca2-138">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4ca2-138">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4ca2-139">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4ca2-139">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4ca2-140">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4ca2-140">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="a4ca2-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4ca2-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="a4ca2-142">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a4ca2-142">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a4ca2-143">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="a4ca2-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)