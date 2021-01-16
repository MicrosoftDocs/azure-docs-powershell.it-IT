---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475414"
---
# <span data-ttu-id="a13ac-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a13ac-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="a13ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a13ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a13ac-103">Interrompe la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a13ac-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="a13ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a13ac-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a13ac-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a13ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a13ac-106">Il cmdlet **Stop-AzSqlSyncGroupSync** interrompe la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a13ac-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="a13ac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a13ac-107">EXAMPLES</span></span>

### <span data-ttu-id="a13ac-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a13ac-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="a13ac-109">Questo comando interrompe la sincronizzazione in corso per il gruppo di sincronizzazione mysg.</span><span class="sxs-lookup"><span data-stu-id="a13ac-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="a13ac-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a13ac-110">PARAMETERS</span></span>

### <span data-ttu-id="a13ac-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a13ac-111">-DatabaseName</span></span>
<span data-ttu-id="a13ac-112">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a13ac-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a13ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a13ac-113">-DefaultProfile</span></span>
<span data-ttu-id="a13ac-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a13ac-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a13ac-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a13ac-115">-PassThru</span></span>
<span data-ttu-id="a13ac-116">Definisce se restituire il gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="a13ac-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="a13ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a13ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="a13ac-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a13ac-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a13ac-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a13ac-119">-ServerName</span></span>
<span data-ttu-id="a13ac-120">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a13ac-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a13ac-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a13ac-121">-SyncGroupName</span></span>
<span data-ttu-id="a13ac-122">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a13ac-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a13ac-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a13ac-123">-Confirm</span></span>
<span data-ttu-id="a13ac-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a13ac-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a13ac-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a13ac-125">-WhatIf</span></span>
<span data-ttu-id="a13ac-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a13ac-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a13ac-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a13ac-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a13ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a13ac-128">CommonParameters</span></span>
<span data-ttu-id="a13ac-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a13ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a13ac-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a13ac-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a13ac-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a13ac-131">INPUTS</span></span>

### <span data-ttu-id="a13ac-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a13ac-132">System.String</span></span>

## <span data-ttu-id="a13ac-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a13ac-133">OUTPUTS</span></span>

### <span data-ttu-id="a13ac-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="a13ac-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a13ac-135">Note</span><span class="sxs-lookup"><span data-stu-id="a13ac-135">NOTES</span></span>

## <span data-ttu-id="a13ac-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a13ac-136">RELATED LINKS</span></span>

[<span data-ttu-id="a13ac-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a13ac-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

