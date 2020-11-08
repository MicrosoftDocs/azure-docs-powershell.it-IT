---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033695"
---
# <span data-ttu-id="85a16-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="85a16-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="85a16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85a16-102">SYNOPSIS</span></span>
<span data-ttu-id="85a16-103">Elimina una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="85a16-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="85a16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85a16-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85a16-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85a16-105">DESCRIPTION</span></span>
<span data-ttu-id="85a16-106">Questo comando Elimina una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="85a16-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="85a16-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85a16-107">EXAMPLES</span></span>

### <span data-ttu-id="85a16-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85a16-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="85a16-109">Elimina una regola di rete virtuale di Azure SQL Server esistente</span><span class="sxs-lookup"><span data-stu-id="85a16-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="85a16-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85a16-110">PARAMETERS</span></span>

### <span data-ttu-id="85a16-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85a16-111">-AsJob</span></span>
<span data-ttu-id="85a16-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="85a16-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85a16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a16-113">-DefaultProfile</span></span>
<span data-ttu-id="85a16-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="85a16-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85a16-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a16-115">-ResourceGroupName</span></span>
<span data-ttu-id="85a16-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85a16-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="85a16-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="85a16-117">-ServerName</span></span>
<span data-ttu-id="85a16-118">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="85a16-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="85a16-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="85a16-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="85a16-120">Nome della regola di rete virtuale di Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="85a16-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="85a16-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85a16-121">-Confirm</span></span>
<span data-ttu-id="85a16-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85a16-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a16-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a16-123">-WhatIf</span></span>
<span data-ttu-id="85a16-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85a16-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85a16-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85a16-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85a16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a16-126">CommonParameters</span></span>
<span data-ttu-id="85a16-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85a16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a16-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85a16-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a16-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85a16-129">INPUTS</span></span>

### <span data-ttu-id="85a16-130">System. String</span><span class="sxs-lookup"><span data-stu-id="85a16-130">System.String</span></span>

## <span data-ttu-id="85a16-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85a16-131">OUTPUTS</span></span>

### <span data-ttu-id="85a16-132">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="85a16-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="85a16-133">Note</span><span class="sxs-lookup"><span data-stu-id="85a16-133">NOTES</span></span>

## <span data-ttu-id="85a16-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85a16-134">RELATED LINKS</span></span>
