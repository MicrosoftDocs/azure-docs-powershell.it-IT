---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 040b08e328cb06629e706350fa14752fa6918954
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514052"
---
# <span data-ttu-id="e61f9-101">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="e61f9-101">Start-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="e61f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e61f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e61f9-103">Avvia la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e61f9-103">Starts a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e61f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e61f9-104">SYNTAX</span></span>

```
Start-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e61f9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e61f9-105">DESCRIPTION</span></span>
<span data-ttu-id="e61f9-106">Il cmdlet **Start-AzureRmSqlSyncGroupSync** avvia la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e61f9-106">The **Start-AzureRmSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="e61f9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e61f9-107">EXAMPLES</span></span>

### <span data-ttu-id="e61f9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e61f9-108">Example 1</span></span>
```
PS C:\> Start-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="e61f9-109">Questo comando avvia un ciclo di sincronizzazione per il gruppo di sincronizzazione mysg.</span><span class="sxs-lookup"><span data-stu-id="e61f9-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="e61f9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e61f9-110">PARAMETERS</span></span>

### <span data-ttu-id="e61f9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e61f9-111">-DatabaseName</span></span>
<span data-ttu-id="e61f9-112">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e61f9-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e61f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e61f9-113">-DefaultProfile</span></span>
<span data-ttu-id="e61f9-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e61f9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e61f9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e61f9-115">-PassThru</span></span>
<span data-ttu-id="e61f9-116">Definisce se restituire il gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="e61f9-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="e61f9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e61f9-117">-ResourceGroupName</span></span>
<span data-ttu-id="e61f9-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e61f9-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e61f9-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e61f9-119">-ServerName</span></span>
<span data-ttu-id="e61f9-120">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e61f9-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e61f9-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e61f9-121">-SyncGroupName</span></span>
<span data-ttu-id="e61f9-122">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e61f9-122">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e61f9-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e61f9-123">-Confirm</span></span>
<span data-ttu-id="e61f9-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e61f9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e61f9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e61f9-125">-WhatIf</span></span>
<span data-ttu-id="e61f9-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e61f9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e61f9-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e61f9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e61f9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e61f9-128">CommonParameters</span></span>
<span data-ttu-id="e61f9-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e61f9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e61f9-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e61f9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e61f9-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e61f9-131">INPUTS</span></span>

### <span data-ttu-id="e61f9-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e61f9-132">None</span></span>
<span data-ttu-id="e61f9-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e61f9-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e61f9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e61f9-134">OUTPUTS</span></span>

### <span data-ttu-id="e61f9-135">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="e61f9-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e61f9-136">Note</span><span class="sxs-lookup"><span data-stu-id="e61f9-136">NOTES</span></span>

## <span data-ttu-id="e61f9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e61f9-137">RELATED LINKS</span></span>

[<span data-ttu-id="e61f9-138">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="e61f9-138">Stop-AzureRmSqlSyncGroupSync</span></span>](./Stop-AzureRmSqlSyncGroupSync.md)

