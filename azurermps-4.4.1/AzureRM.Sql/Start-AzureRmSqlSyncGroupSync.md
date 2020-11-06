---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: e81667523327c9a83497ce4f586f166fe69d0dc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520745"
---
# <span data-ttu-id="71bf4-101">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="71bf4-101">Start-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="71bf4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="71bf4-103">Avvia la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="71bf4-103">Starts a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71bf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71bf4-104">SYNTAX</span></span>

```
Start-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71bf4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="71bf4-106">Il cmdlet **Start-AzureRmSqlSyncGroupSync** avvia la sincronizzazione di un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="71bf4-106">The **Start-AzureRmSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="71bf4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="71bf4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="71bf4-108">Example 1</span></span>
```
PS C:\> Start-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="71bf4-109">Questo comando avvia un ciclo di sincronizzazione per il gruppo di sincronizzazione mysg.</span><span class="sxs-lookup"><span data-stu-id="71bf4-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="71bf4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71bf4-110">PARAMETERS</span></span>

### <span data-ttu-id="71bf4-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71bf4-111">-Confirm</span></span>
<span data-ttu-id="71bf4-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71bf4-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71bf4-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="71bf4-113">-DatabaseName</span></span>
<span data-ttu-id="71bf4-114">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="71bf4-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="71bf4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71bf4-115">-PassThru</span></span>
<span data-ttu-id="71bf4-116">Definisce se restituire il gruppo di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="71bf4-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="71bf4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71bf4-117">-ResourceGroupName</span></span>
<span data-ttu-id="71bf4-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="71bf4-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="71bf4-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="71bf4-119">-ServerName</span></span>
<span data-ttu-id="71bf4-120">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="71bf4-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="71bf4-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="71bf4-121">-SyncGroupName</span></span>
<span data-ttu-id="71bf4-122">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="71bf4-122">The sync group name.</span></span>

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

### <span data-ttu-id="71bf4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71bf4-123">-WhatIf</span></span>
<span data-ttu-id="71bf4-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71bf4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71bf4-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71bf4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71bf4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71bf4-126">-DefaultProfile</span></span>
<span data-ttu-id="71bf4-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71bf4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71bf4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71bf4-128">CommonParameters</span></span>
<span data-ttu-id="71bf4-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71bf4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71bf4-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71bf4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71bf4-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71bf4-131">INPUTS</span></span>

## <span data-ttu-id="71bf4-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71bf4-132">OUTPUTS</span></span>

### <span data-ttu-id="71bf4-133">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="71bf4-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="71bf4-134">Note</span><span class="sxs-lookup"><span data-stu-id="71bf4-134">NOTES</span></span>

## <span data-ttu-id="71bf4-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71bf4-135">RELATED LINKS</span></span>

[<span data-ttu-id="71bf4-136">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="71bf4-136">Stop-AzureRmSqlSyncGroupSync</span></span>](./Stop-AzureRmSqlSyncGroupSync.md)

