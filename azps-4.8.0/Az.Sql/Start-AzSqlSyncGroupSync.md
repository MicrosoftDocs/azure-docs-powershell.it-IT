---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033689"
---
# <span data-ttu-id="4e9a1-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="4e9a1-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="4e9a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="4e9a1-103">Avvia la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="4e9a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e9a1-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e9a1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e9a1-105">DESCRIPTION</span></span>
<span data-ttu-id="4e9a1-106">Il cmdlet **Start-AzSqlSyncGroupSync** avvia la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="4e9a1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e9a1-107">EXAMPLES</span></span>

### <span data-ttu-id="4e9a1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e9a1-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="4e9a1-109">Questo comando avvia un ciclo di sincronizzazione per il gruppo di sincronizzazione mysg.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="4e9a1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e9a1-110">PARAMETERS</span></span>

### <span data-ttu-id="4e9a1-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e9a1-111">-DatabaseName</span></span>
<span data-ttu-id="4e9a1-112">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4e9a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e9a1-113">-DefaultProfile</span></span>
<span data-ttu-id="4e9a1-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4e9a1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e9a1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e9a1-115">-PassThru</span></span>
<span data-ttu-id="4e9a1-116">Definisce se restituire il gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="4e9a1-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="4e9a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e9a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e9a1-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e9a1-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4e9a1-119">-ServerName</span></span>
<span data-ttu-id="4e9a1-120">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4e9a1-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4e9a1-121">-SyncGroupName</span></span>
<span data-ttu-id="4e9a1-122">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-122">The sync group name.</span></span>

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

### <span data-ttu-id="4e9a1-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e9a1-123">-Confirm</span></span>
<span data-ttu-id="4e9a1-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e9a1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e9a1-125">-WhatIf</span></span>
<span data-ttu-id="4e9a1-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e9a1-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e9a1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e9a1-128">CommonParameters</span></span>
<span data-ttu-id="4e9a1-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e9a1-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e9a1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e9a1-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e9a1-131">INPUTS</span></span>

### <span data-ttu-id="4e9a1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4e9a1-132">System.String</span></span>

## <span data-ttu-id="4e9a1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e9a1-133">OUTPUTS</span></span>

### <span data-ttu-id="4e9a1-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="4e9a1-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="4e9a1-135">Note</span><span class="sxs-lookup"><span data-stu-id="4e9a1-135">NOTES</span></span>

## <span data-ttu-id="4e9a1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e9a1-136">RELATED LINKS</span></span>

[<span data-ttu-id="4e9a1-137">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="4e9a1-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

