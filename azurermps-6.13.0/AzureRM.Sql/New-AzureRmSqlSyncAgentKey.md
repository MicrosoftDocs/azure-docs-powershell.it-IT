---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: cb4ca947d9f87cd6a0d3b4cdf476cf0176db2c3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509012"
---
# <span data-ttu-id="ed146-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="ed146-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="ed146-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed146-102">SYNOPSIS</span></span>
<span data-ttu-id="ed146-103">Crea una chiave di agente di sincronizzazione di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ed146-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed146-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed146-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed146-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed146-105">DESCRIPTION</span></span>
<span data-ttu-id="ed146-106">Il cmdlet **New-AzureRmSqlSyncAgentKey** crea una chiave di agente di sincronizzazione di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ed146-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="ed146-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed146-107">EXAMPLES</span></span>

### <span data-ttu-id="ed146-108">Esempio 1: creare una chiave dell'agente di sincronizzazione per un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ed146-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="ed146-109">Questo comando crea una chiave dell'agente di sincronizzazione per un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ed146-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="ed146-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed146-110">PARAMETERS</span></span>

### <span data-ttu-id="ed146-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed146-111">-DefaultProfile</span></span>
<span data-ttu-id="ed146-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ed146-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed146-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed146-113">-ResourceGroupName</span></span>
<span data-ttu-id="ed146-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ed146-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="ed146-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ed146-115">-ServerName</span></span>
<span data-ttu-id="ed146-116">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ed146-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="ed146-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="ed146-117">-SyncAgentName</span></span>
<span data-ttu-id="ed146-118">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="ed146-118">The sync agent name.</span></span>

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

### <span data-ttu-id="ed146-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed146-119">-Confirm</span></span>
<span data-ttu-id="ed146-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed146-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed146-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed146-121">-WhatIf</span></span>
<span data-ttu-id="ed146-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed146-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed146-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed146-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed146-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed146-124">CommonParameters</span></span>
<span data-ttu-id="ed146-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed146-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed146-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed146-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed146-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed146-127">INPUTS</span></span>

### <span data-ttu-id="ed146-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ed146-128">System.String</span></span>

## <span data-ttu-id="ed146-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed146-129">OUTPUTS</span></span>

### <span data-ttu-id="ed146-130">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="ed146-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="ed146-131">Note</span><span class="sxs-lookup"><span data-stu-id="ed146-131">NOTES</span></span>

## <span data-ttu-id="ed146-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed146-132">RELATED LINKS</span></span>
