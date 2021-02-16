---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178382"
---
# <span data-ttu-id="e0d31-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0d31-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="e0d31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0d31-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d31-103">Crea una configurazione di ripristino del sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="e0d31-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="e0d31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0d31-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0d31-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e0d31-105">DESCRIPTION</span></span>
<span data-ttu-id="e0d31-106">Il cmdlet **New-AzSqlServerDisasterRecoveryConfiguration** crea una SQL di ripristino del sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="e0d31-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e0d31-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0d31-107">EXAMPLES</span></span>

## <span data-ttu-id="e0d31-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0d31-108">PARAMETERS</span></span>

### <span data-ttu-id="e0d31-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0d31-109">-AsJob</span></span>
<span data-ttu-id="e0d31-110">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e0d31-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0d31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d31-111">-DefaultProfile</span></span>
<span data-ttu-id="e0d31-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e0d31-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0d31-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="e0d31-113">-FailoverPolicy</span></span>
<span data-ttu-id="e0d31-114">Specifica i criteri di failover.</span><span class="sxs-lookup"><span data-stu-id="e0d31-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="e0d31-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d31-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="e0d31-116">Specifica il nome del gruppo di risorse partner.</span><span class="sxs-lookup"><span data-stu-id="e0d31-116">Specifies the name of the partner resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d31-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="e0d31-117">-PartnerServerName</span></span>
<span data-ttu-id="e0d31-118">Specifica il nome del server partner.</span><span class="sxs-lookup"><span data-stu-id="e0d31-118">Specifies the name of the partner server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d31-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d31-119">-ResourceGroupName</span></span>
<span data-ttu-id="e0d31-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e0d31-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e0d31-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e0d31-121">-ServerName</span></span>
<span data-ttu-id="e0d31-122">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="e0d31-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e0d31-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="e0d31-123">-VirtualEndpointName</span></span>
<span data-ttu-id="e0d31-124">Specifica il nome del punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0d31-124">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d31-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0d31-125">-Confirm</span></span>
<span data-ttu-id="e0d31-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0d31-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0d31-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0d31-127">-WhatIf</span></span>
<span data-ttu-id="e0d31-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0d31-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0d31-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0d31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0d31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d31-130">CommonParameters</span></span>
<span data-ttu-id="e0d31-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0d31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d31-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e0d31-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d31-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="e0d31-133">INPUTS</span></span>

### <span data-ttu-id="e0d31-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e0d31-134">System.String</span></span>

## <span data-ttu-id="e0d31-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0d31-135">OUTPUTS</span></span>

### <span data-ttu-id="e0d31-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="e0d31-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="e0d31-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e0d31-137">NOTES</span></span>

## <span data-ttu-id="e0d31-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0d31-138">RELATED LINKS</span></span>

[<span data-ttu-id="e0d31-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0d31-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e0d31-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0d31-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e0d31-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0d31-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e0d31-142">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="e0d31-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
