---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864944"
---
# <span data-ttu-id="5073e-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="5073e-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="5073e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5073e-102">SYNOPSIS</span></span>
<span data-ttu-id="5073e-103">Avvia la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5073e-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="5073e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5073e-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5073e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5073e-105">DESCRIPTION</span></span>
<span data-ttu-id="5073e-106">Il cmdlet **Start-AzSqlSyncGroupSync** avvia la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5073e-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="5073e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5073e-107">EXAMPLES</span></span>

### <span data-ttu-id="5073e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5073e-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="5073e-109">Questo comando avvia un ciclo di sincronizzazione per il gruppo di sincronizzazione mysg.</span><span class="sxs-lookup"><span data-stu-id="5073e-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="5073e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5073e-110">PARAMETERS</span></span>

### <span data-ttu-id="5073e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5073e-111">-DatabaseName</span></span>
<span data-ttu-id="5073e-112">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5073e-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5073e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5073e-113">-DefaultProfile</span></span>
<span data-ttu-id="5073e-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5073e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5073e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5073e-115">-PassThru</span></span>
<span data-ttu-id="5073e-116">Definisce se restituire il gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="5073e-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="5073e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5073e-117">-ResourceGroupName</span></span>
<span data-ttu-id="5073e-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5073e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="5073e-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5073e-119">-ServerName</span></span>
<span data-ttu-id="5073e-120">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5073e-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5073e-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5073e-121">-SyncGroupName</span></span>
<span data-ttu-id="5073e-122">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5073e-122">The sync group name.</span></span>

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

### <span data-ttu-id="5073e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5073e-123">-Confirm</span></span>
<span data-ttu-id="5073e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5073e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5073e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5073e-125">-WhatIf</span></span>
<span data-ttu-id="5073e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5073e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5073e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5073e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5073e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5073e-128">CommonParameters</span></span>
<span data-ttu-id="5073e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5073e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5073e-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5073e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5073e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5073e-131">INPUTS</span></span>

### <span data-ttu-id="5073e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5073e-132">System.String</span></span>

## <span data-ttu-id="5073e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5073e-133">OUTPUTS</span></span>

### <span data-ttu-id="5073e-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="5073e-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="5073e-135">Note</span><span class="sxs-lookup"><span data-stu-id="5073e-135">NOTES</span></span>

## <span data-ttu-id="5073e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5073e-136">RELATED LINKS</span></span>

[<span data-ttu-id="5073e-137">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="5073e-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

