---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: 4b04fe3a27178ce5228f8e3fe2a397728a432b6b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857365"
---
# <span data-ttu-id="2742c-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="2742c-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="2742c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2742c-102">SYNOPSIS</span></span>
<span data-ttu-id="2742c-103">Crea una chiave di agente di sincronizzazione di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2742c-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="2742c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2742c-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2742c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2742c-105">DESCRIPTION</span></span>
<span data-ttu-id="2742c-106">Il cmdlet **New-AzSqlSyncAgentKey** crea una chiave di agente di sincronizzazione di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2742c-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="2742c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2742c-107">EXAMPLES</span></span>

### <span data-ttu-id="2742c-108">Esempio 1: creare una chiave dell'agente di sincronizzazione per un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2742c-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="2742c-109">Questo comando crea una chiave dell'agente di sincronizzazione per un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2742c-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="2742c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2742c-110">PARAMETERS</span></span>

### <span data-ttu-id="2742c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2742c-111">-DefaultProfile</span></span>
<span data-ttu-id="2742c-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2742c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2742c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2742c-113">-ResourceGroupName</span></span>
<span data-ttu-id="2742c-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2742c-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="2742c-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2742c-115">-ServerName</span></span>
<span data-ttu-id="2742c-116">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2742c-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="2742c-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="2742c-117">-SyncAgentName</span></span>
<span data-ttu-id="2742c-118">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2742c-118">The sync agent name.</span></span>

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

### <span data-ttu-id="2742c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2742c-119">-Confirm</span></span>
<span data-ttu-id="2742c-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2742c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2742c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2742c-121">-WhatIf</span></span>
<span data-ttu-id="2742c-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2742c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2742c-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2742c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2742c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2742c-124">CommonParameters</span></span>
<span data-ttu-id="2742c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2742c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2742c-126">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2742c-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2742c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2742c-127">INPUTS</span></span>

### <span data-ttu-id="2742c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2742c-128">System.String</span></span>

## <span data-ttu-id="2742c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2742c-129">OUTPUTS</span></span>

### <span data-ttu-id="2742c-130">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="2742c-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="2742c-131">Note</span><span class="sxs-lookup"><span data-stu-id="2742c-131">NOTES</span></span>

## <span data-ttu-id="2742c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2742c-132">RELATED LINKS</span></span>
