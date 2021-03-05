---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 10da2a625eb3858e77343275246d8a142fefc504
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995173"
---
# <span data-ttu-id="b4011-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4011-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="b4011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4011-102">SYNOPSIS</span></span>
<span data-ttu-id="b4011-103">Rimuove una configurazione SQL ripristino del sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="b4011-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="b4011-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4011-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4011-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b4011-105">DESCRIPTION</span></span>
<span data-ttu-id="b4011-106">Il cmdlet **Remove-AzSqlServerDisasterRecoveryConfiguration** rimuove una SQL di ripristino del sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="b4011-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="b4011-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4011-107">EXAMPLES</span></span>

## <span data-ttu-id="b4011-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4011-108">PARAMETERS</span></span>

### <span data-ttu-id="b4011-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4011-109">-DefaultProfile</span></span>
<span data-ttu-id="b4011-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b4011-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4011-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b4011-111">-Force</span></span>
<span data-ttu-id="b4011-112">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="b4011-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4011-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4011-113">-ResourceGroupName</span></span>
<span data-ttu-id="b4011-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4011-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b4011-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4011-115">-ServerName</span></span>
<span data-ttu-id="b4011-116">Specifica il nome di un server di SQL database.</span><span class="sxs-lookup"><span data-stu-id="b4011-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="b4011-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="b4011-117">-VirtualEndpointName</span></span>
<span data-ttu-id="b4011-118">Specifica il nome di un punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="b4011-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="b4011-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4011-119">-Confirm</span></span>
<span data-ttu-id="b4011-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4011-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4011-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4011-121">-WhatIf</span></span>
<span data-ttu-id="b4011-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4011-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4011-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4011-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4011-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4011-124">CommonParameters</span></span>
<span data-ttu-id="b4011-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4011-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4011-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b4011-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4011-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="b4011-127">INPUTS</span></span>

### <span data-ttu-id="b4011-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b4011-128">System.String</span></span>

## <span data-ttu-id="b4011-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4011-129">OUTPUTS</span></span>

### <span data-ttu-id="b4011-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="b4011-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="b4011-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="b4011-131">NOTES</span></span>

## <span data-ttu-id="b4011-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4011-132">RELATED LINKS</span></span>

[<span data-ttu-id="b4011-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4011-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b4011-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4011-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b4011-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4011-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b4011-136">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="b4011-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
