---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: e73409edf07402dd44cb5f29a6e878d29d7bfede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510280"
---
# <span data-ttu-id="a2734-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a2734-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="a2734-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2734-102">SYNOPSIS</span></span>
<span data-ttu-id="a2734-103">Ottiene o elenca la regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2734-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2734-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2734-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2734-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2734-105">DESCRIPTION</span></span>
<span data-ttu-id="a2734-106">Questo comando consente di ottenere una specifica regola di rete virtuale di Azure SQL Server o un elenco di regole di rete virtuale di Azure SQL Server in un server.</span><span class="sxs-lookup"><span data-stu-id="a2734-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="a2734-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2734-107">EXAMPLES</span></span>

### <span data-ttu-id="a2734-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2734-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="a2734-109">Ottiene una singola regola di rete virtuale di Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="a2734-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="a2734-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a2734-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="a2734-111">Ottiene l'elenco delle regole di rete virtuale di Azure SQL Server nel server specificato</span><span class="sxs-lookup"><span data-stu-id="a2734-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="a2734-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2734-112">PARAMETERS</span></span>

### <span data-ttu-id="a2734-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2734-113">-ResourceGroupName</span></span>
<span data-ttu-id="a2734-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a2734-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2734-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a2734-115">-ServerName</span></span>
<span data-ttu-id="a2734-116">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2734-116">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a2734-117">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="a2734-117">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="a2734-118">Nome della regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2734-118">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="a2734-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2734-119">-DefaultProfile</span></span>
<span data-ttu-id="a2734-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2734-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2734-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2734-121">CommonParameters</span></span>
<span data-ttu-id="a2734-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2734-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2734-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2734-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2734-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2734-124">INPUTS</span></span>

### <span data-ttu-id="a2734-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a2734-125">System.String</span></span>

## <span data-ttu-id="a2734-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2734-126">OUTPUTS</span></span>

### <span data-ttu-id="a2734-127">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="a2734-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="a2734-128">Note</span><span class="sxs-lookup"><span data-stu-id="a2734-128">NOTES</span></span>

## <span data-ttu-id="a2734-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2734-129">RELATED LINKS</span></span>
