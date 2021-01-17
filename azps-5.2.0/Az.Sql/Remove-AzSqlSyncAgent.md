---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322683"
---
# <span data-ttu-id="12a1d-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="12a1d-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="12a1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="12a1d-103">Rimuove un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="12a1d-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="12a1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12a1d-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12a1d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12a1d-105">DESCRIPTION</span></span>
<span data-ttu-id="12a1d-106">Il cmdlet **Remove-AzSqlSyncAgent** rimuove un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="12a1d-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="12a1d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12a1d-107">EXAMPLES</span></span>

### <span data-ttu-id="12a1d-108">Esempio 1: rimuovere un agente di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="12a1d-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="12a1d-109">Questo comando rimuove l'agente di sincronizzazione di Azure SQL denominato syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="12a1d-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="12a1d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12a1d-110">PARAMETERS</span></span>

### <span data-ttu-id="12a1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a1d-111">-DefaultProfile</span></span>
<span data-ttu-id="12a1d-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="12a1d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12a1d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="12a1d-113">-Force</span></span>
<span data-ttu-id="12a1d-114">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="12a1d-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="12a1d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="12a1d-115">-Name</span></span>
<span data-ttu-id="12a1d-116">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="12a1d-116">The sync agent name.</span></span>

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

### <span data-ttu-id="12a1d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12a1d-117">-PassThru</span></span>
<span data-ttu-id="12a1d-118">Definisce se restituire l'agente di sincronizzazione rimosso</span><span class="sxs-lookup"><span data-stu-id="12a1d-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="12a1d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a1d-119">-ResourceGroupName</span></span>
<span data-ttu-id="12a1d-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12a1d-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="12a1d-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="12a1d-121">-ServerName</span></span>
<span data-ttu-id="12a1d-122">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="12a1d-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="12a1d-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12a1d-123">-Confirm</span></span>
<span data-ttu-id="12a1d-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12a1d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12a1d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12a1d-125">-WhatIf</span></span>
<span data-ttu-id="12a1d-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12a1d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12a1d-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12a1d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12a1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a1d-128">CommonParameters</span></span>
<span data-ttu-id="12a1d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a1d-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12a1d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a1d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12a1d-131">INPUTS</span></span>

### <span data-ttu-id="12a1d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="12a1d-132">System.String</span></span>

## <span data-ttu-id="12a1d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12a1d-133">OUTPUTS</span></span>

### <span data-ttu-id="12a1d-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="12a1d-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="12a1d-135">Note</span><span class="sxs-lookup"><span data-stu-id="12a1d-135">NOTES</span></span>

## <span data-ttu-id="12a1d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12a1d-136">RELATED LINKS</span></span>

[<span data-ttu-id="12a1d-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="12a1d-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="12a1d-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="12a1d-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

