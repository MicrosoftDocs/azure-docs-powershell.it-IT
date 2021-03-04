---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: ad00759bb2babb85c17ab9efe2d7e47025434607
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982030"
---
# <span data-ttu-id="70cb7-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="70cb7-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="70cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="70cb7-103">Ottiene una configurazione di ripristino del sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="70cb7-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="70cb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70cb7-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70cb7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="70cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="70cb7-106">Il cmdlet **Get-AzSqlServerDisasterRecoveryConfiguration** ottiene una SQL di ripristino del sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="70cb7-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="70cb7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70cb7-107">EXAMPLES</span></span>

## <span data-ttu-id="70cb7-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70cb7-108">PARAMETERS</span></span>

### <span data-ttu-id="70cb7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70cb7-109">-DefaultProfile</span></span>
<span data-ttu-id="70cb7-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="70cb7-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70cb7-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70cb7-111">-ResourceGroupName</span></span>
<span data-ttu-id="70cb7-112">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="70cb7-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="70cb7-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="70cb7-113">-ServerName</span></span>
<span data-ttu-id="70cb7-114">Specifica il nome del server SQL database.</span><span class="sxs-lookup"><span data-stu-id="70cb7-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="70cb7-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="70cb7-115">-VirtualEndpointName</span></span>
<span data-ttu-id="70cb7-116">Specifica il nome del punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="70cb7-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70cb7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70cb7-117">-Confirm</span></span>
<span data-ttu-id="70cb7-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70cb7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70cb7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70cb7-119">-WhatIf</span></span>
<span data-ttu-id="70cb7-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70cb7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70cb7-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70cb7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70cb7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70cb7-122">CommonParameters</span></span>
<span data-ttu-id="70cb7-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70cb7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70cb7-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70cb7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70cb7-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="70cb7-125">INPUTS</span></span>

### <span data-ttu-id="70cb7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="70cb7-126">System.String</span></span>

## <span data-ttu-id="70cb7-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70cb7-127">OUTPUTS</span></span>

### <span data-ttu-id="70cb7-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="70cb7-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="70cb7-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="70cb7-129">NOTES</span></span>

## <span data-ttu-id="70cb7-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70cb7-130">RELATED LINKS</span></span>

[<span data-ttu-id="70cb7-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="70cb7-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="70cb7-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="70cb7-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="70cb7-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="70cb7-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="70cb7-134">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="70cb7-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

