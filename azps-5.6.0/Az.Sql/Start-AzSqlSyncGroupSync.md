---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: 13f58f454fb84a4bcd003afd84761197d41c16ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008493"
---
# <span data-ttu-id="ac044-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="ac044-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="ac044-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac044-102">SYNOPSIS</span></span>
<span data-ttu-id="ac044-103">Avvia la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ac044-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="ac044-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac044-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac044-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ac044-105">DESCRIPTION</span></span>
<span data-ttu-id="ac044-106">Il cmdlet **Start-AzSqlSyncGroupSync avvia** la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ac044-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="ac044-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac044-107">EXAMPLES</span></span>

### <span data-ttu-id="ac044-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac044-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="ac044-109">Questo comando avvia un round di sincronizzazione per il gruppo di sincronizzazione mysg.</span><span class="sxs-lookup"><span data-stu-id="ac044-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="ac044-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac044-110">PARAMETERS</span></span>

### <span data-ttu-id="ac044-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ac044-111">-DatabaseName</span></span>
<span data-ttu-id="ac044-112">Nome del database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ac044-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ac044-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac044-113">-DefaultProfile</span></span>
<span data-ttu-id="ac044-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="ac044-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac044-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac044-115">-PassThru</span></span>
<span data-ttu-id="ac044-116">Definisce se restituire il gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="ac044-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="ac044-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac044-117">-ResourceGroupName</span></span>
<span data-ttu-id="ac044-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac044-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ac044-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ac044-119">-ServerName</span></span>
<span data-ttu-id="ac044-120">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ac044-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ac044-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ac044-121">-SyncGroupName</span></span>
<span data-ttu-id="ac044-122">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ac044-122">The sync group name.</span></span>

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

### <span data-ttu-id="ac044-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac044-123">-Confirm</span></span>
<span data-ttu-id="ac044-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac044-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac044-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac044-125">-WhatIf</span></span>
<span data-ttu-id="ac044-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac044-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac044-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac044-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac044-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac044-128">CommonParameters</span></span>
<span data-ttu-id="ac044-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac044-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac044-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac044-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac044-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="ac044-131">INPUTS</span></span>

### <span data-ttu-id="ac044-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ac044-132">System.String</span></span>

## <span data-ttu-id="ac044-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac044-133">OUTPUTS</span></span>

### <span data-ttu-id="ac044-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="ac044-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="ac044-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="ac044-135">NOTES</span></span>

## <span data-ttu-id="ac044-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac044-136">RELATED LINKS</span></span>

[<span data-ttu-id="ac044-137">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="ac044-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

