---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 0010dad985755512e97aaccb14540ec16dc47cab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857294"
---
# <span data-ttu-id="5ac88-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5ac88-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="5ac88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ac88-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac88-103">Rimuove un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac88-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5ac88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ac88-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ac88-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ac88-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac88-106">Il cmdlet **Remove-AzSqlSyncGroup** rimuove un gruppo di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac88-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5ac88-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ac88-107">EXAMPLES</span></span>

### <span data-ttu-id="5ac88-108">Esempio 1: rimuovere un gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="5ac88-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="5ac88-109">Questo comando rimuove il gruppo di sincronizzazione di database SQL di Azure denominato syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="5ac88-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="5ac88-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ac88-110">PARAMETERS</span></span>

### <span data-ttu-id="5ac88-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ac88-111">-DatabaseName</span></span>
<span data-ttu-id="5ac88-112">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac88-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5ac88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac88-113">-DefaultProfile</span></span>
<span data-ttu-id="5ac88-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5ac88-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ac88-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5ac88-115">-Force</span></span>
<span data-ttu-id="5ac88-116">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="5ac88-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="5ac88-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ac88-117">-Name</span></span>
<span data-ttu-id="5ac88-118">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5ac88-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac88-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ac88-119">-PassThru</span></span>
<span data-ttu-id="5ac88-120">Definisce se restituire il gruppo di sincronizzazione rimosso</span><span class="sxs-lookup"><span data-stu-id="5ac88-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="5ac88-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac88-121">-ResourceGroupName</span></span>
<span data-ttu-id="5ac88-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5ac88-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="5ac88-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5ac88-123">-ServerName</span></span>
<span data-ttu-id="5ac88-124">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5ac88-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5ac88-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5ac88-125">-Confirm</span></span>
<span data-ttu-id="5ac88-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ac88-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac88-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac88-127">-WhatIf</span></span>
<span data-ttu-id="5ac88-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ac88-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ac88-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ac88-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac88-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac88-130">CommonParameters</span></span>
<span data-ttu-id="5ac88-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac88-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac88-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ac88-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac88-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ac88-133">INPUTS</span></span>

### <span data-ttu-id="5ac88-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5ac88-134">System.String</span></span>

## <span data-ttu-id="5ac88-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ac88-135">OUTPUTS</span></span>

### <span data-ttu-id="5ac88-136">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="5ac88-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="5ac88-137">Note</span><span class="sxs-lookup"><span data-stu-id="5ac88-137">NOTES</span></span>

## <span data-ttu-id="5ac88-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ac88-138">RELATED LINKS</span></span>

[<span data-ttu-id="5ac88-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5ac88-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="5ac88-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5ac88-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="5ac88-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5ac88-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

