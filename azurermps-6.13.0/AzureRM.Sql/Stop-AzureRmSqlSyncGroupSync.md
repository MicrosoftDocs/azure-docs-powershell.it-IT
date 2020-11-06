---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 9cd213aea4e6211f52b076fca753385aefb1b449
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513311"
---
# <span data-ttu-id="29c1e-101">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="29c1e-101">Stop-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="29c1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="29c1e-103">Interrompe la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="29c1e-103">Stops a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29c1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29c1e-104">SYNTAX</span></span>

```
Stop-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29c1e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29c1e-105">DESCRIPTION</span></span>
<span data-ttu-id="29c1e-106">Il cmdlet **Stop-AzureRmSqlSyncGroupSync** interrompe la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="29c1e-106">The **Stop-AzureRmSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="29c1e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29c1e-107">EXAMPLES</span></span>

### <span data-ttu-id="29c1e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="29c1e-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="29c1e-109">Questo comando interrompe la sincronizzazione in corso per il gruppo di sincronizzazione mysg.</span><span class="sxs-lookup"><span data-stu-id="29c1e-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="29c1e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29c1e-110">PARAMETERS</span></span>

### <span data-ttu-id="29c1e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29c1e-111">-DatabaseName</span></span>
<span data-ttu-id="29c1e-112">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="29c1e-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="29c1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c1e-113">-DefaultProfile</span></span>
<span data-ttu-id="29c1e-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="29c1e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29c1e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29c1e-115">-PassThru</span></span>
<span data-ttu-id="29c1e-116">Definisce se restituire il gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="29c1e-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="29c1e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c1e-117">-ResourceGroupName</span></span>
<span data-ttu-id="29c1e-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="29c1e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="29c1e-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="29c1e-119">-ServerName</span></span>
<span data-ttu-id="29c1e-120">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="29c1e-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="29c1e-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="29c1e-121">-SyncGroupName</span></span>
<span data-ttu-id="29c1e-122">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="29c1e-122">The sync group name.</span></span>

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

### <span data-ttu-id="29c1e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="29c1e-123">-Confirm</span></span>
<span data-ttu-id="29c1e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29c1e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c1e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c1e-125">-WhatIf</span></span>
<span data-ttu-id="29c1e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="29c1e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29c1e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="29c1e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c1e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c1e-128">CommonParameters</span></span>
<span data-ttu-id="29c1e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c1e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c1e-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29c1e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c1e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29c1e-131">INPUTS</span></span>

### <span data-ttu-id="29c1e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="29c1e-132">System.String</span></span>

## <span data-ttu-id="29c1e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29c1e-133">OUTPUTS</span></span>

### <span data-ttu-id="29c1e-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="29c1e-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="29c1e-135">Note</span><span class="sxs-lookup"><span data-stu-id="29c1e-135">NOTES</span></span>

## <span data-ttu-id="29c1e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29c1e-136">RELATED LINKS</span></span>

[<span data-ttu-id="29c1e-137">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="29c1e-137">Start-AzureRmSqlSyncGroupSync</span></span>](./Start-AzureRmSqlSyncGroupSync.md)

