---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 3e9b99a1ab9d3fdce813166e7a0834c14b81b651
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676882"
---
# <span data-ttu-id="c0210-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c0210-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="c0210-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0210-102">SYNOPSIS</span></span>
<span data-ttu-id="c0210-103">Ottiene o elenca la regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c0210-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="c0210-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0210-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0210-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0210-105">DESCRIPTION</span></span>
<span data-ttu-id="c0210-106">Questo comando consente di ottenere una specifica regola di rete virtuale di Azure SQL Server o un elenco di regole di rete virtuale di Azure SQL Server in un server.</span><span class="sxs-lookup"><span data-stu-id="c0210-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="c0210-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0210-107">EXAMPLES</span></span>

### <span data-ttu-id="c0210-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0210-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="c0210-109">Ottiene una singola regola di rete virtuale di Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="c0210-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="c0210-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c0210-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="c0210-111">Ottiene l'elenco delle regole di rete virtuale di Azure SQL Server nel server specificato</span><span class="sxs-lookup"><span data-stu-id="c0210-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="c0210-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c0210-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="c0210-113">Ottiene l'elenco delle regole di rete virtuale di Azure SQL Server nel server specificato che iniziano con "virtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="c0210-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="c0210-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0210-114">PARAMETERS</span></span>

### <span data-ttu-id="c0210-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0210-115">-DefaultProfile</span></span>
<span data-ttu-id="c0210-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c0210-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0210-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0210-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0210-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c0210-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c0210-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c0210-119">-ServerName</span></span>
<span data-ttu-id="c0210-120">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c0210-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c0210-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="c0210-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="c0210-122">Nome della regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c0210-122">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="c0210-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0210-123">CommonParameters</span></span>
<span data-ttu-id="c0210-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0210-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0210-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0210-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0210-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0210-126">INPUTS</span></span>

### <span data-ttu-id="c0210-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c0210-127">System.String</span></span>

## <span data-ttu-id="c0210-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0210-128">OUTPUTS</span></span>

### <span data-ttu-id="c0210-129">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="c0210-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="c0210-130">Note</span><span class="sxs-lookup"><span data-stu-id="c0210-130">NOTES</span></span>

## <span data-ttu-id="c0210-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0210-131">RELATED LINKS</span></span>