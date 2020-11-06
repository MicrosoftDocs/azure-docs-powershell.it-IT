---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 9886d2d32dd3bce8841dcf2652cf89054335b112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520583"
---
# <span data-ttu-id="2b6cd-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="2b6cd-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="2b6cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6cd-103">Rimuove un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6cd-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b6cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b6cd-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b6cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b6cd-105">DESCRIPTION</span></span>
<span data-ttu-id="2b6cd-106">Il cmdlet **Remove-AzureRmSqlSyncAgent** rimuove un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6cd-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="2b6cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b6cd-107">EXAMPLES</span></span>

### <span data-ttu-id="2b6cd-108">Esempio 1: rimuovere un agente di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="2b6cd-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="2b6cd-109">Questo comando rimuove l'agente di sincronizzazione di Azure SQL denominato syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="2b6cd-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="2b6cd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b6cd-110">PARAMETERS</span></span>

### <span data-ttu-id="2b6cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6cd-111">-DefaultProfile</span></span>
<span data-ttu-id="2b6cd-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2b6cd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b6cd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2b6cd-113">-Force</span></span>
<span data-ttu-id="2b6cd-114">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="2b6cd-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2b6cd-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b6cd-115">-Name</span></span>
<span data-ttu-id="2b6cd-116">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2b6cd-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b6cd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b6cd-117">-PassThru</span></span>
<span data-ttu-id="2b6cd-118">Definisce se restituire l'agente di sincronizzazione rimosso</span><span class="sxs-lookup"><span data-stu-id="2b6cd-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="2b6cd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b6cd-119">-ResourceGroupName</span></span>
<span data-ttu-id="2b6cd-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b6cd-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b6cd-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2b6cd-121">-ServerName</span></span>
<span data-ttu-id="2b6cd-122">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2b6cd-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="2b6cd-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b6cd-123">-Confirm</span></span>
<span data-ttu-id="2b6cd-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b6cd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b6cd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b6cd-125">-WhatIf</span></span>
<span data-ttu-id="2b6cd-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b6cd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b6cd-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b6cd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b6cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6cd-128">CommonParameters</span></span>
<span data-ttu-id="2b6cd-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b6cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6cd-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b6cd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6cd-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b6cd-131">INPUTS</span></span>

### <span data-ttu-id="2b6cd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2b6cd-132">System.String</span></span>

## <span data-ttu-id="2b6cd-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b6cd-133">OUTPUTS</span></span>

### <span data-ttu-id="2b6cd-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="2b6cd-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="2b6cd-135">Note</span><span class="sxs-lookup"><span data-stu-id="2b6cd-135">NOTES</span></span>

## <span data-ttu-id="2b6cd-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b6cd-136">RELATED LINKS</span></span>

[<span data-ttu-id="2b6cd-137">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="2b6cd-137">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="2b6cd-138">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="2b6cd-138">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

