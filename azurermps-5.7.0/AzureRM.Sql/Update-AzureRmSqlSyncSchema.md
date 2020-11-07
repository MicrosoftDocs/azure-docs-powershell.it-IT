---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
ms.openlocfilehash: a78e22c66e5099ec3987fb98d1b354906c11a8d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687402"
---
# <span data-ttu-id="30c73-101">Update-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="30c73-101">Update-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="30c73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30c73-102">SYNOPSIS</span></span>
<span data-ttu-id="30c73-103">Aggiornare lo schema di sincronizzazione per un database membro di sincronizzazione o un database dell'hub di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="30c73-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="30c73-104">Otterrà lo schema di database più recente dal database reale e lo userà per aggiornare lo schema memorizzato nella cache dal database dei metadati di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="30c73-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="30c73-105">Se viene specificato "SyncMemberName", lo schema del database membro verrà aggiornato; in caso contrario, aggiornerà lo schema del database hub.</span><span class="sxs-lookup"><span data-stu-id="30c73-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30c73-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30c73-106">SYNTAX</span></span>

```
Update-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30c73-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30c73-107">DESCRIPTION</span></span>
<span data-ttu-id="30c73-108">Il cmdlet **Update-AzureRmSqlSyncSchema** aggiorna lo schema di sincronizzazione per un database membro di sincronizzazione o un database dell'hub di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="30c73-108">The **Update-AzureRmSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="30c73-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30c73-109">EXAMPLES</span></span>

### <span data-ttu-id="30c73-110">Esempio 1: aggiornare lo schema di sincronizzazione per un database hub</span><span class="sxs-lookup"><span data-stu-id="30c73-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="30c73-111">Questo comando Aggiorna lo schema di sincronizzazione per il database hub nel gruppo di sincronizzazione syncGroup01</span><span class="sxs-lookup"><span data-stu-id="30c73-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="30c73-112">Esempio 2: aggiornare lo schema di sincronizzazione per un database di membri</span><span class="sxs-lookup"><span data-stu-id="30c73-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="30c73-113">Questo comando Aggiorna lo schema di sincronizzazione per il database del membro nel syncMember01 membro di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="30c73-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="30c73-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30c73-114">PARAMETERS</span></span>

### <span data-ttu-id="30c73-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30c73-115">-DatabaseName</span></span>
<span data-ttu-id="30c73-116">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="30c73-116">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30c73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c73-117">-DefaultProfile</span></span>
<span data-ttu-id="30c73-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="30c73-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c73-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30c73-119">-PassThru</span></span>
<span data-ttu-id="30c73-120">Definisce se restituire il gruppo di sincronizzazione su cui funziona il cmdlet</span><span class="sxs-lookup"><span data-stu-id="30c73-120">Defines Whether return the sync group this cmdlet works on</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c73-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c73-121">-ResourceGroupName</span></span>
<span data-ttu-id="30c73-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30c73-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30c73-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="30c73-123">-ServerName</span></span>
<span data-ttu-id="30c73-124">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="30c73-124">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30c73-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="30c73-125">-SyncGroupName</span></span>
<span data-ttu-id="30c73-126">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="30c73-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30c73-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="30c73-127">-SyncMemberName</span></span>
<span data-ttu-id="30c73-128">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="30c73-128">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30c73-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30c73-129">-Confirm</span></span>
<span data-ttu-id="30c73-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30c73-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c73-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c73-131">-WhatIf</span></span>
<span data-ttu-id="30c73-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30c73-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30c73-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30c73-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c73-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c73-134">CommonParameters</span></span>
<span data-ttu-id="30c73-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30c73-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c73-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30c73-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c73-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30c73-137">INPUTS</span></span>

### <span data-ttu-id="30c73-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="30c73-138">None</span></span>
<span data-ttu-id="30c73-139">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="30c73-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30c73-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30c73-140">OUTPUTS</span></span>

### <span data-ttu-id="30c73-141">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="30c73-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="30c73-142">Note</span><span class="sxs-lookup"><span data-stu-id="30c73-142">NOTES</span></span>

## <span data-ttu-id="30c73-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30c73-143">RELATED LINKS</span></span>