---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: 254f2def5a1be57840ea195f326534ce883870df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515967"
---
# <span data-ttu-id="8e819-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="8e819-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="8e819-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e819-102">SYNOPSIS</span></span>
<span data-ttu-id="8e819-103">Crea una chiave di agente di sincronizzazione di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8e819-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e819-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e819-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e819-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e819-105">DESCRIPTION</span></span>
<span data-ttu-id="8e819-106">Il cmdlet **New-AzureRmSqlSyncAgentKey** crea una chiave di agente di sincronizzazione di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8e819-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="8e819-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e819-107">EXAMPLES</span></span>

### <span data-ttu-id="8e819-108">Esempio 1: creare una chiave dell'agente di sincronizzazione per un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8e819-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="8e819-109">Questo comando crea una chiave dell'agente di sincronizzazione per un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8e819-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="8e819-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e819-110">PARAMETERS</span></span>

### <span data-ttu-id="8e819-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8e819-111">-Confirm</span></span>
<span data-ttu-id="8e819-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e819-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e819-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e819-113">-ResourceGroupName</span></span>
<span data-ttu-id="8e819-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8e819-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e819-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="8e819-115">-ServerName</span></span>
<span data-ttu-id="8e819-116">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8e819-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="8e819-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="8e819-117">-SyncAgentName</span></span>
<span data-ttu-id="8e819-118">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8e819-118">The sync agent name.</span></span>

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

### <span data-ttu-id="8e819-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e819-119">-WhatIf</span></span>
<span data-ttu-id="8e819-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e819-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e819-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e819-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e819-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e819-122">-DefaultProfile</span></span>
<span data-ttu-id="8e819-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e819-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e819-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e819-124">CommonParameters</span></span>
<span data-ttu-id="8e819-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e819-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e819-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e819-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e819-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e819-127">INPUTS</span></span>

## <span data-ttu-id="8e819-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e819-128">OUTPUTS</span></span>

### <span data-ttu-id="8e819-129">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="8e819-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="8e819-130">Note</span><span class="sxs-lookup"><span data-stu-id="8e819-130">NOTES</span></span>

## <span data-ttu-id="8e819-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e819-131">RELATED LINKS</span></span>

