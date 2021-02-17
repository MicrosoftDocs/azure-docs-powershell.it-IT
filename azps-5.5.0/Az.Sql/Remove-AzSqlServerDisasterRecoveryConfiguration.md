---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207883"
---
# <span data-ttu-id="6b046-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b046-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="6b046-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b046-102">SYNOPSIS</span></span>
<span data-ttu-id="6b046-103">Rimuove una configurazione SQL ripristino del sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="6b046-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="6b046-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b046-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b046-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6b046-105">DESCRIPTION</span></span>
<span data-ttu-id="6b046-106">Il cmdlet **Remove-AzSqlServerDisasterRecoveryConfiguration** rimuove una SQL di ripristino del sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="6b046-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="6b046-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b046-107">EXAMPLES</span></span>

## <span data-ttu-id="6b046-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b046-108">PARAMETERS</span></span>

### <span data-ttu-id="6b046-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b046-109">-DefaultProfile</span></span>
<span data-ttu-id="6b046-110">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="6b046-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b046-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6b046-111">-Force</span></span>
<span data-ttu-id="6b046-112">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="6b046-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6b046-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b046-113">-ResourceGroupName</span></span>
<span data-ttu-id="6b046-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b046-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6b046-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6b046-115">-ServerName</span></span>
<span data-ttu-id="6b046-116">Specifica il nome di un server di database SQL server di database.</span><span class="sxs-lookup"><span data-stu-id="6b046-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="6b046-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="6b046-117">-VirtualEndpointName</span></span>
<span data-ttu-id="6b046-118">Specifica il nome di un punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="6b046-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="6b046-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b046-119">-Confirm</span></span>
<span data-ttu-id="6b046-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b046-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b046-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b046-121">-WhatIf</span></span>
<span data-ttu-id="6b046-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b046-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b046-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b046-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b046-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b046-124">CommonParameters</span></span>
<span data-ttu-id="6b046-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b046-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b046-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6b046-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b046-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="6b046-127">INPUTS</span></span>

### <span data-ttu-id="6b046-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6b046-128">System.String</span></span>

## <span data-ttu-id="6b046-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b046-129">OUTPUTS</span></span>

### <span data-ttu-id="6b046-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="6b046-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="6b046-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="6b046-131">NOTES</span></span>

## <span data-ttu-id="6b046-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b046-132">RELATED LINKS</span></span>

[<span data-ttu-id="6b046-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b046-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6b046-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b046-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6b046-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b046-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6b046-136">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="6b046-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
