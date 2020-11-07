---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 8a472307c475e093de6f8e6071c137afda5ec1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687667"
---
# <span data-ttu-id="2ee15-101">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="2ee15-101">Stop-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="2ee15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ee15-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee15-103">Interrompe la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2ee15-103">Stops a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ee15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ee15-104">SYNTAX</span></span>

```
Stop-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ee15-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ee15-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee15-106">Il cmdlet **Stop-AzureRmSqlSyncGroupSync** interrompe la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2ee15-106">The **Stop-AzureRmSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="2ee15-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ee15-107">EXAMPLES</span></span>

### <span data-ttu-id="2ee15-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ee15-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="2ee15-109">Questo comando interrompe la sincronizzazione in corso per il gruppo di sincronizzazione mysg.</span><span class="sxs-lookup"><span data-stu-id="2ee15-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="2ee15-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ee15-110">PARAMETERS</span></span>

### <span data-ttu-id="2ee15-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2ee15-111">-Confirm</span></span>
<span data-ttu-id="2ee15-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ee15-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ee15-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2ee15-113">-DatabaseName</span></span>
<span data-ttu-id="2ee15-114">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee15-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="2ee15-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ee15-115">-PassThru</span></span>
<span data-ttu-id="2ee15-116">Definisce se restituire il gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="2ee15-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="2ee15-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee15-117">-ResourceGroupName</span></span>
<span data-ttu-id="2ee15-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2ee15-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="2ee15-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2ee15-119">-ServerName</span></span>
<span data-ttu-id="2ee15-120">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2ee15-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2ee15-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee15-121">-SyncGroupName</span></span>
<span data-ttu-id="2ee15-122">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2ee15-122">The sync group name.</span></span>

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

### <span data-ttu-id="2ee15-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ee15-123">-WhatIf</span></span>
<span data-ttu-id="2ee15-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ee15-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ee15-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ee15-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ee15-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee15-126">-DefaultProfile</span></span>
<span data-ttu-id="2ee15-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee15-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ee15-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee15-128">CommonParameters</span></span>
<span data-ttu-id="2ee15-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee15-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee15-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee15-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee15-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ee15-131">INPUTS</span></span>

## <span data-ttu-id="2ee15-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ee15-132">OUTPUTS</span></span>

### <span data-ttu-id="2ee15-133">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="2ee15-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="2ee15-134">Note</span><span class="sxs-lookup"><span data-stu-id="2ee15-134">NOTES</span></span>

## <span data-ttu-id="2ee15-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ee15-135">RELATED LINKS</span></span>

[<span data-ttu-id="2ee15-136">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="2ee15-136">Start-AzureRmSqlSyncGroupSync</span></span>](./Start-AzureRmSqlSyncGroupSync.md)

