---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: b5a0a09986be3856db4ab65f9dc411e6940ffb64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857657"
---
# <span data-ttu-id="8cb68-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="8cb68-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="8cb68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cb68-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb68-103">Aggiornare lo schema di sincronizzazione per un database membro di sincronizzazione o un database dell'hub di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb68-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="8cb68-104">Otterrà lo schema di database più recente dal database reale e lo userà per aggiornare lo schema memorizzato nella cache dal database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb68-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="8cb68-105">Se viene specificato "SyncMemberName", lo schema del database membro verrà aggiornato; in caso contrario, aggiornerà lo schema del database hub.</span><span class="sxs-lookup"><span data-stu-id="8cb68-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="8cb68-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cb68-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cb68-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cb68-107">DESCRIPTION</span></span>
<span data-ttu-id="8cb68-108">Il cmdlet **Update-AzSqlSyncSchema** aggiorna lo schema di sincronizzazione per un database membro di sincronizzazione o un database dell'hub di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb68-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="8cb68-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cb68-109">EXAMPLES</span></span>

### <span data-ttu-id="8cb68-110">Esempio 1: aggiornare lo schema di sincronizzazione per un database hub</span><span class="sxs-lookup"><span data-stu-id="8cb68-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="8cb68-111">Questo comando Aggiorna lo schema di sincronizzazione per il database hub nel gruppo di sincronizzazione syncGroup01</span><span class="sxs-lookup"><span data-stu-id="8cb68-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="8cb68-112">Esempio 2: aggiornare lo schema di sincronizzazione per un database di membri</span><span class="sxs-lookup"><span data-stu-id="8cb68-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="8cb68-113">Questo comando Aggiorna lo schema di sincronizzazione per il database del membro nel syncMember01 membro di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="8cb68-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="8cb68-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cb68-114">PARAMETERS</span></span>

### <span data-ttu-id="8cb68-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8cb68-115">-DatabaseName</span></span>
<span data-ttu-id="8cb68-116">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cb68-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="8cb68-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb68-117">-DefaultProfile</span></span>
<span data-ttu-id="8cb68-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8cb68-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cb68-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cb68-119">-PassThru</span></span>
<span data-ttu-id="8cb68-120">Definisce se restituire il gruppo di sincronizzazione su cui funziona il cmdlet</span><span class="sxs-lookup"><span data-stu-id="8cb68-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="8cb68-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb68-121">-ResourceGroupName</span></span>
<span data-ttu-id="8cb68-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8cb68-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="8cb68-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="8cb68-123">-ServerName</span></span>
<span data-ttu-id="8cb68-124">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8cb68-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="8cb68-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb68-125">-SyncGroupName</span></span>
<span data-ttu-id="8cb68-126">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb68-126">The sync group name.</span></span>

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

### <span data-ttu-id="8cb68-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="8cb68-127">-SyncMemberName</span></span>
<span data-ttu-id="8cb68-128">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb68-128">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb68-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8cb68-129">-Confirm</span></span>
<span data-ttu-id="8cb68-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cb68-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cb68-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cb68-131">-WhatIf</span></span>
<span data-ttu-id="8cb68-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cb68-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cb68-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cb68-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cb68-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb68-134">CommonParameters</span></span>
<span data-ttu-id="8cb68-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cb68-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb68-136">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cb68-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb68-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cb68-137">INPUTS</span></span>

### <span data-ttu-id="8cb68-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8cb68-138">System.String</span></span>

## <span data-ttu-id="8cb68-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cb68-139">OUTPUTS</span></span>

### <span data-ttu-id="8cb68-140">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="8cb68-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="8cb68-141">Note</span><span class="sxs-lookup"><span data-stu-id="8cb68-141">NOTES</span></span>

## <span data-ttu-id="8cb68-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cb68-142">RELATED LINKS</span></span>
