---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f4744eee1e93867ea150819a8f4bcadc5ac8a35b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003069"
---
# <span data-ttu-id="8030f-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8030f-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="8030f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8030f-102">SYNOPSIS</span></span>
<span data-ttu-id="8030f-103">Ottiene o elenca una regola per SQL Server rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="8030f-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="8030f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8030f-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8030f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8030f-105">DESCRIPTION</span></span>
<span data-ttu-id="8030f-106">Questo comando ottiene una specifica regola di rete SQL Server virtuale di Azure o un elenco di regole di SQL Server di rete virtuale di Azure in un server.</span><span class="sxs-lookup"><span data-stu-id="8030f-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="8030f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8030f-107">EXAMPLES</span></span>

### <span data-ttu-id="8030f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8030f-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="8030f-109">Ottiene una singola regola di rete virtuale SQL Server Azure</span><span class="sxs-lookup"><span data-stu-id="8030f-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="8030f-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8030f-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="8030f-111">Recupera l'elenco delle regole SQL Server di rete virtuale di Azure nel server specificato</span><span class="sxs-lookup"><span data-stu-id="8030f-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="8030f-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8030f-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="8030f-113">Ottiene l'elenco delle regole SQL Server di rete virtuale di Azure nel server specificato che iniziano con "virtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="8030f-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="8030f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8030f-114">PARAMETERS</span></span>

### <span data-ttu-id="8030f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8030f-115">-DefaultProfile</span></span>
<span data-ttu-id="8030f-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8030f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8030f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8030f-117">-ResourceGroupName</span></span>
<span data-ttu-id="8030f-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8030f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="8030f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8030f-119">-ServerName</span></span>
<span data-ttu-id="8030f-120">Nome del server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8030f-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="8030f-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="8030f-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="8030f-122">Nome della regola della rete virtuale di Sql Server di Azure.</span><span class="sxs-lookup"><span data-stu-id="8030f-122">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="8030f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8030f-123">CommonParameters</span></span>
<span data-ttu-id="8030f-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8030f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8030f-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8030f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8030f-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="8030f-126">INPUTS</span></span>

### <span data-ttu-id="8030f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8030f-127">System.String</span></span>

## <span data-ttu-id="8030f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8030f-128">OUTPUTS</span></span>

### <span data-ttu-id="8030f-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="8030f-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="8030f-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="8030f-130">NOTES</span></span>

## <span data-ttu-id="8030f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8030f-131">RELATED LINKS</span></span>
