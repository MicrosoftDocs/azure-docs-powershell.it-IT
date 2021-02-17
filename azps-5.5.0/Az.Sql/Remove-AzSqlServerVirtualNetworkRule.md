---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188015"
---
# <span data-ttu-id="60a6f-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="60a6f-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="60a6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="60a6f-103">Elimina una regola di Rete SQL Server virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="60a6f-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="60a6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60a6f-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60a6f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60a6f-105">DESCRIPTION</span></span>
<span data-ttu-id="60a6f-106">Questo comando elimina una regola di Rete SQL Server virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="60a6f-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="60a6f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60a6f-107">EXAMPLES</span></span>

### <span data-ttu-id="60a6f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60a6f-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="60a6f-109">Elimina una regola di rete virtuale SQL Server azure esistente</span><span class="sxs-lookup"><span data-stu-id="60a6f-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="60a6f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60a6f-110">PARAMETERS</span></span>

### <span data-ttu-id="60a6f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60a6f-111">-AsJob</span></span>
<span data-ttu-id="60a6f-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="60a6f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60a6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a6f-113">-DefaultProfile</span></span>
<span data-ttu-id="60a6f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="60a6f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60a6f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a6f-115">-ResourceGroupName</span></span>
<span data-ttu-id="60a6f-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60a6f-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="60a6f-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="60a6f-117">-ServerName</span></span>
<span data-ttu-id="60a6f-118">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="60a6f-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="60a6f-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="60a6f-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="60a6f-120">Nome della regola per la rete virtuale di Sql Server di Azure</span><span class="sxs-lookup"><span data-stu-id="60a6f-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="60a6f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60a6f-121">-Confirm</span></span>
<span data-ttu-id="60a6f-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a6f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a6f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a6f-123">-WhatIf</span></span>
<span data-ttu-id="60a6f-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60a6f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60a6f-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60a6f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a6f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a6f-126">CommonParameters</span></span>
<span data-ttu-id="60a6f-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a6f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a6f-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60a6f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a6f-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="60a6f-129">INPUTS</span></span>

### <span data-ttu-id="60a6f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="60a6f-130">System.String</span></span>

## <span data-ttu-id="60a6f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60a6f-131">OUTPUTS</span></span>

### <span data-ttu-id="60a6f-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="60a6f-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="60a6f-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="60a6f-133">NOTES</span></span>

## <span data-ttu-id="60a6f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60a6f-134">RELATED LINKS</span></span>
