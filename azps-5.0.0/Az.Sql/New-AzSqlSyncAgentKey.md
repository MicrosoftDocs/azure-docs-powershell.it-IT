---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200114"
---
# <span data-ttu-id="b0726-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="b0726-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="b0726-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0726-102">SYNOPSIS</span></span>
<span data-ttu-id="b0726-103">Crea una chiave di agente di sincronizzazione di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b0726-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="b0726-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0726-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0726-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0726-105">DESCRIPTION</span></span>
<span data-ttu-id="b0726-106">Il cmdlet **New-AzSqlSyncAgentKey** crea una chiave di agente di sincronizzazione di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b0726-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="b0726-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0726-107">EXAMPLES</span></span>

### <span data-ttu-id="b0726-108">Esempio 1: creare una chiave dell'agente di sincronizzazione per un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0726-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="b0726-109">Questo comando crea una chiave dell'agente di sincronizzazione per un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0726-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="b0726-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0726-110">PARAMETERS</span></span>

### <span data-ttu-id="b0726-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0726-111">-DefaultProfile</span></span>
<span data-ttu-id="b0726-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b0726-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0726-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0726-113">-ResourceGroupName</span></span>
<span data-ttu-id="b0726-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0726-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="b0726-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b0726-115">-ServerName</span></span>
<span data-ttu-id="b0726-116">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b0726-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="b0726-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="b0726-117">-SyncAgentName</span></span>
<span data-ttu-id="b0726-118">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b0726-118">The sync agent name.</span></span>

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

### <span data-ttu-id="b0726-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0726-119">-Confirm</span></span>
<span data-ttu-id="b0726-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0726-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0726-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0726-121">-WhatIf</span></span>
<span data-ttu-id="b0726-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0726-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0726-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0726-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0726-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0726-124">CommonParameters</span></span>
<span data-ttu-id="b0726-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0726-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0726-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0726-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0726-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0726-127">INPUTS</span></span>

### <span data-ttu-id="b0726-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b0726-128">System.String</span></span>

## <span data-ttu-id="b0726-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0726-129">OUTPUTS</span></span>

### <span data-ttu-id="b0726-130">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="b0726-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="b0726-131">Note</span><span class="sxs-lookup"><span data-stu-id="b0726-131">NOTES</span></span>

## <span data-ttu-id="b0726-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0726-132">RELATED LINKS</span></span>