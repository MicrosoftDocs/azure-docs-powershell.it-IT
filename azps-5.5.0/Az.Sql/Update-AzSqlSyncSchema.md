---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 571bef6b10420f08e7b1a00bdfddd4415ba0e033
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187935"
---
# <span data-ttu-id="77cc9-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="77cc9-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="77cc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="77cc9-103">Aggiornare lo schema di sincronizzazione per un database dei membri di sincronizzazione o un database hub di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="77cc9-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="77cc9-104">Il database otterrà lo schema di database più recente dal database reale e lo userà per aggiornare lo schema memorizzato nella cache dal database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="77cc9-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="77cc9-105">Se è specificato "SyncMemberName", aggiorna lo schema di database dei membri; in caso contrario, lo schema del database hub verrà aggiornato.</span><span class="sxs-lookup"><span data-stu-id="77cc9-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="77cc9-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77cc9-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77cc9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="77cc9-107">DESCRIPTION</span></span>
<span data-ttu-id="77cc9-108">Il cmdlet **Update-AzSqlSyncSchema** aggiorna lo schema di sincronizzazione per un database dei membri di sincronizzazione o un database dell'hub di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="77cc9-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="77cc9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77cc9-109">EXAMPLES</span></span>

### <span data-ttu-id="77cc9-110">Esempio 1: Aggiornare lo schema di sincronizzazione per un database hub</span><span class="sxs-lookup"><span data-stu-id="77cc9-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="77cc9-111">Questo comando aggiorna lo schema di sincronizzazione per il database hub nel gruppo di sincronizzazione syncGroup01</span><span class="sxs-lookup"><span data-stu-id="77cc9-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="77cc9-112">Esempio 2: Aggiornare lo schema di sincronizzazione per un database membro</span><span class="sxs-lookup"><span data-stu-id="77cc9-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="77cc9-113">Questo comando aggiorna lo schema di sincronizzazione per il database dei membri nel membro di sincronizzazione syncMember01</span><span class="sxs-lookup"><span data-stu-id="77cc9-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="77cc9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77cc9-114">PARAMETERS</span></span>

### <span data-ttu-id="77cc9-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="77cc9-115">-DatabaseName</span></span>
<span data-ttu-id="77cc9-116">Nome del database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="77cc9-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="77cc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77cc9-117">-DefaultProfile</span></span>
<span data-ttu-id="77cc9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="77cc9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77cc9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77cc9-119">-PassThru</span></span>
<span data-ttu-id="77cc9-120">Definisce se restituire il gruppo di sincronizzazione su cui funziona questo cmdlet</span><span class="sxs-lookup"><span data-stu-id="77cc9-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="77cc9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77cc9-121">-ResourceGroupName</span></span>
<span data-ttu-id="77cc9-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="77cc9-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="77cc9-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="77cc9-123">-ServerName</span></span>
<span data-ttu-id="77cc9-124">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="77cc9-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="77cc9-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="77cc9-125">-SyncGroupName</span></span>
<span data-ttu-id="77cc9-126">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="77cc9-126">The sync group name.</span></span>

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

### <span data-ttu-id="77cc9-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="77cc9-127">-SyncMemberName</span></span>
<span data-ttu-id="77cc9-128">Nome del membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="77cc9-128">The sync member name.</span></span>

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

### <span data-ttu-id="77cc9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77cc9-129">-Confirm</span></span>
<span data-ttu-id="77cc9-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77cc9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77cc9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77cc9-131">-WhatIf</span></span>
<span data-ttu-id="77cc9-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77cc9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77cc9-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77cc9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77cc9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77cc9-134">CommonParameters</span></span>
<span data-ttu-id="77cc9-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77cc9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77cc9-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77cc9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77cc9-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="77cc9-137">INPUTS</span></span>

### <span data-ttu-id="77cc9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="77cc9-138">System.String</span></span>

## <span data-ttu-id="77cc9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77cc9-139">OUTPUTS</span></span>

### <span data-ttu-id="77cc9-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="77cc9-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="77cc9-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="77cc9-141">NOTES</span></span>

## <span data-ttu-id="77cc9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77cc9-142">RELATED LINKS</span></span>
