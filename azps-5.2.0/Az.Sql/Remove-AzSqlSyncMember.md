---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322680"
---
# <span data-ttu-id="e8139-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e8139-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="e8139-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8139-102">SYNOPSIS</span></span>
<span data-ttu-id="e8139-103">Rimuove un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e8139-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e8139-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8139-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8139-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8139-105">DESCRIPTION</span></span>
<span data-ttu-id="e8139-106">Il cmdlet **Remove-AzSqlSyncMember** rimuove un membro di sincronizzazione di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e8139-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e8139-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8139-107">EXAMPLES</span></span>

### <span data-ttu-id="e8139-108">Esempio 1: rimuovere un membro di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="e8139-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="e8139-109">Questo comando rimuove il membro di sincronizzazione di database SQL di Azure denominato syncMember01.</span><span class="sxs-lookup"><span data-stu-id="e8139-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="e8139-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8139-110">PARAMETERS</span></span>

### <span data-ttu-id="e8139-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e8139-111">-DatabaseName</span></span>
<span data-ttu-id="e8139-112">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e8139-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e8139-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8139-113">-DefaultProfile</span></span>
<span data-ttu-id="e8139-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e8139-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8139-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e8139-115">-Force</span></span>
<span data-ttu-id="e8139-116">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="e8139-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e8139-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8139-117">-Name</span></span>
<span data-ttu-id="e8139-118">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e8139-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8139-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8139-119">-PassThru</span></span>
<span data-ttu-id="e8139-120">Definisce se restituire il membro di sincronizzazione rimosso</span><span class="sxs-lookup"><span data-stu-id="e8139-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="e8139-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8139-121">-ResourceGroupName</span></span>
<span data-ttu-id="e8139-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e8139-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="e8139-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e8139-123">-ServerName</span></span>
<span data-ttu-id="e8139-124">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e8139-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e8139-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e8139-125">-SyncGroupName</span></span>
<span data-ttu-id="e8139-126">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e8139-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8139-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8139-127">-Confirm</span></span>
<span data-ttu-id="e8139-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8139-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8139-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8139-129">-WhatIf</span></span>
<span data-ttu-id="e8139-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8139-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8139-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8139-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8139-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8139-132">CommonParameters</span></span>
<span data-ttu-id="e8139-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8139-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8139-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8139-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8139-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8139-135">INPUTS</span></span>

### <span data-ttu-id="e8139-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e8139-136">System.String</span></span>

## <span data-ttu-id="e8139-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8139-137">OUTPUTS</span></span>

### <span data-ttu-id="e8139-138">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="e8139-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="e8139-139">Note</span><span class="sxs-lookup"><span data-stu-id="e8139-139">NOTES</span></span>

## <span data-ttu-id="e8139-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8139-140">RELATED LINKS</span></span>

[<span data-ttu-id="e8139-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e8139-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="e8139-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e8139-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="e8139-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e8139-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

